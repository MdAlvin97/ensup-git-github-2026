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


