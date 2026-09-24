# Carnet de bord
Identifiant GitHub : MdAlvin97
# Mes preuves

TP1 
Etape A 1. L'état du fichier ; Le fichier n'est pas visible par Git, il faut le préparer avec Git add pour ensuite pouvoir le commiter.

Etape A

À écrire : que fait add que ne fait pas l'enregistrement dans l'éditeur ?
Git add permet de préparer la version du fichier afin de pouvoir le commiter contrairement à l'enregistrement de l'éditeur

Etape B
Prédiction avant de continuer : si vous commitez maintenant, quelle phrase manque dans le commit ?
Pourquoi ?
Si je commite maintenant, il va manquer la phrase " Inscription sur place." car après avoir enregistrer cette phrase, on n'a pas préparer le fichier à être commiter avec la commande git add.

Etape C 
Explication de l'index :
C'est une étape entre mon fichier modifié et l'historique Git.
Quand je fais git add ça va le préparer pour ensuite enregistrer avec le commit.

Etape D 
Différence entre fichier enregistré, index et commit :
Un fichier enregistré est lorsque qu'on enregistre celui-ci tout simplement dans l'éditeur, il n'est pas considéré par Git.

L'index c'est l'étape entre mon fichier modifié et l'historique Git. Quand je fais git add ça va le préparer pour ensuite enregistrer avec le commit.

Un commit c'est l'enregistrement des fichiers dans l'historique Git, et qui sont prêt à être envoyé (push) vers Github.

Trace individuelle 
Un court extrait du log :
$ git log --oneline
6ae6c92 (HEAD -> main) docs: expliquer le fonctionnement de l index
31d8bd4 chore: ignorer les fichiers locaux
1aa0851 docs: preciser les conditions d acces
3d00d42 docs: presenter le forum ENSUP
...

Expliquez pourquoi préparer seulement une partie peut aider à créer des commits cohérents :
Car cela va permettre d'avoir un bon historique git, permettre de mieux comprendre celui-ci. Cela aide à créer des commits cohérents, c'est-à-dire des commits qui ne concernent qu'une seule modification à la fois. "git add -p" permet de choisir précisément quels changements inclure dans un commit.


Enquête 1 : le fichier disparu du diff ·
1. Pendant 3 min, écrivez votre prédiction avant d'exécuter git diff : Il ne va pas montrer le texte qu'il y a dans acces.md selon moi

2.Pendant 5 min, comparez git status --short, git diff, puis git add acces.md et git diff --cached :

git status --short me permet d'observer l'état du fichier ; journal.md a été modifié mais reste à le préparer et pour acces.md ça dit que le fichier est totalement nouveau, git ne l'avait pas dans son historique.
git diff montre alors que ce qui a été modifier dans journal.md et non pas ce qui a été modifier dans acces.md

Tandis que : git add acces.md prepare l fichier acces.md donc Git le connais maintenant
git diff --cached montre le contenu qui a été modifié dans tous les fichiers


3.Pendant 5 min, expliquez pourquoi un fichier non suivi n'apparaît pas dans le diff ordinaire : git diff compare uniquement les fichiers déjà suivis par Git avec leur dernière version commitée. Un fichier non suivi n'a jamais été ajouté à l'historique Git, il n'a donc rien à comparer, ce qui explique qu'il n'apparaisse pas dans un diff ordinaire.



4.Preuve de git log --oneline -- acces.md et de git show 31ada33 :

git log --oneline -- acces.md
31ada33 (HEAD -> main) docs: ajout d indication d acces

medeu@Alv99 MINGW64 ~/ensup-git-github-2026/rendus/MdAlvin97 (main)
$ git show 31ada33
commit 31ada33aed676aebfd4753c1e185a490ab0392a1 (HEAD -> main)
Author: MdAlvin97 <medeufalvin@gmail.com>
Date:   Wed Sep 23 19:10:43 2026 +0200

    docs: ajout d indication d acces

diff --git a/rendus/MdAlvin97/README.md b/rendus/MdAlvin97/README.md
index 7782e61..5b99922 100644
--- a/rendus/MdAlvin97/README.md
+++ b/rendus/MdAlvin97/README.md
@@ -1,4 +1,6 @@
 # Forum des associations ENSUP
 Un guide pour préparer sa première visite sur le campus.
 Entrée gratuite.
- Inscription sur place.
\ No newline at end of file
+Inscription sur place.
+Horaire : 9h-12h
+Du 01/10/2026 au 10/10/2026
\ No newline at end of file
diff --git a/rendus/MdAlvin97/acces.md b/rendus/MdAlvin97/acces.md
new file mode 100644
index 0000000..a27e318
--- /dev/null
+++ b/rendus/MdAlvin97/acces.md
@@ -0,0 +1,2 @@
+Entrée visiteurs : porte
+principale. Présenter son invitation à l'accueil.
\ No newline at end of file
diff --git a/rendus/MdAlvin97/journal.md b/rendus/MdAlvin97/journal.md
index 80bb094..b7a997f 100644
--- a/rendus/MdAlvin97/journal.md
+++ b/rendus/MdAlvin97/journal.md
@@ -18,4 +18,23 @@ Si je commite maintenant, il va manquer la phrase " Inscription sur place." car
 Etape C
 Explication de l'index :
 C'est une étape entre mon fichier modifié et l'historique Git.
-Quand je fais git add ça va le préparer pour ensuite enregistrer avec le commit.
\ No newline at end of file
+Quand je fais git add ça va le préparer pour ensuite enregistrer avec le commit.
+
+Etape D
+Différence entre fichier enregistré, index et commit :
+Un fichier enregistré est lorsque qu'on enregistre celui-ci tout simplement dans l'éditeur, il n'est pas considéré par Git.
+
+L'index c'est l'étape entre mon fichier modifié et l'historique Git. Quand je fais git add ça va le préparer pour ensuite enregistrer avec le commit.
+
+Un commit c'est l'enregistrement des fichiers dans l'historique Git, et qui sont prêt à être envoyé (push) vers Github.
+
+Trace individuelle
+Un court extrait du log :
+$ git log --oneline
+6ae6c92 (HEAD -> main) docs: expliquer le fonctionnement de l index
+31d8bd4 chore: ignorer les fichiers locaux
+1aa0851 docs: preciser les conditions d acces
+3d00d42 docs: presenter le forum ENSUP
+...
+
+



git log --oneline -- acces.md permet de voir le commit qui a été fait dont le fichier acces.md y figure dedans.
Et de git show 31ada33 montre tous les ajouts et les modifications qui a eu lieu en faisant ce commit.


TP 2

2.Avant de revenir sur main, prédisez quels fichiers seront visibles :
Je pense que tous les fichiers seront visibles y compris le nouveau fichier programme.md

4. Expliquer
sur quelle branche faut-il être pour intégrer une évolution dans main ? Il faut être sur la branche main

Quelle commande prouve que le contenu est présent ? La commande ls prouve bien que le contenue est présent

Dessinez le graphe avant et après :
Avant :
main:                 A------B
                              \
feature/programme               C    (nouveau commit)

Après :
main                 A---B---C


Enquête 2
Comparez avec le fast-forward du TP 2 :
J'ai fait une nouvelle branche avec un nouveau fichier, puis sur le main j'ai fait une modification sur le README.md donc Git a créé un vrai commit de fusion avec deux parents.

$ git show --no-patch --format="%h %p %s" HEAD
02185e0 4a927a1 af035b1 merge: ajouter les indications d accessibilite

Les deux identifiants de parents sont : 4a927a1 (main) et af035b1 (feature/accessibilite).


TP3 
L'URL de ma PR : https://github.com/AbidHamza ensup-git-github-2026/pull/1

Différence entre fork, clone et branche : 
Le fork copie un dépôt vers un autre compte GitHub.

Le clone permet de copier un dépôt vers mon PC, c'est une action qui se fait avec Git (côté PC).

Une branche c'est une ligne de développement à l'intérieur d'un même dépôt (que ce soit en local ou sur GitHub). Elle permet de travailler sur une chose sans toucher à main.