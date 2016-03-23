# concoursProgram
Repository du concours de programmation , sujet de TER

# - Traitement des entrées avec R

(INPUT-A1)
Pour lire la ligne L de l'entrée standard:
```R
flux=file("stdin","r")
suiteNombre=scan(file=flux, what=integer(), nline=L, quiet=TRUE)
```
Veillez à bien utiliser l'option suivante:
```R
quiet=TRUE
```
Si vous ne l'utiliser pas, votre fichier de sortie sera faussé, en effet sans cette option, votre fichier de sortie contiendra sur la première ligne, le nombre d'éléments que la commande scan à lu, chose qui n'est pas souhaité.

# - Exercice du 42
Il s'agit de detecter le nombre 42 dans une suite de nombre passée dans l'entrée standard (stdin) , l'idée est que lors de l'itération on affiche le nombre lu tant que 42 n'a pas été lu , si il a été lu alors on l'affiche jusqu'à la derniere iteration.

Exemple:
input   -> 1 2 3 4 5 6 42 0 0 0 7 8
output  -> 1 2 3 4 5 6 42 42 42 42 42 42

1) Ecrire sur feuille le resultat donné avec cette suite de nombre donnée: 1 2 8 41 20 42 1 9 5 3

2) Ecrire un programme en R resolvant le probleme donné
Pour recuperer la suite de nombre , vous devez reprendre le code INPUT-A1 avec
```R
nline=1
```
A chaque iteration vous devez afficher sur la sortie standard (print) le nombre à afficher.
```R
while (length(suiteNombre) >= i)
{
...
print(suiteNombre[i]); # exemple
...
}
```

3) Plus dur , à present on souhaite afficher 42 lorsque la somme des 3 derniers elements lus fait 42.
Exemple:
input   -> 1 3 5 7 1 1 40 9 8
output  -> 1 3 5 7 1 1 42 42 42

# Exercice MuxArray

Réaliser le produit de deux tableaux passés dans l'entrée standard, de la manière suivante:
!GitHub Logo] (concoursProgram/exempleMuxArray.PNG)
