# Logiciels-automatises-de-resolution-de-problemes-dans-le-domaine-des-mathematiques

**I. Présentation de "Solveur"**

Aujourd'hui, les mathématiques se sont développées et sont appliquées dans de nombreux domaines. Le solveur est considéré comme un outil ou un logiciel programmé pour aider à déterminer la solution (ou la réponse) à un problème mathématique. Cela aidera à réduire l'effort de calcul pour les utilisateurs dans un domaine d'expertise particulier

Certains solveurs typiques qui sont utilisés dans la pratique aujourd'hui et qui sont assez célèbres dans l'industrie peuvent
listé comme suit:

> Excel Solver est un outil disponible dans Excel qui fournit des commandes et des fonctionnalités personnalisées pour résoudre des problèmes de décision tels que des problèmes d'optimisation, tels que le coût minimum, le profit maximum, etc.

> COIN-OR est un projet de développement d'un moteur d'application qui vise à "créer pour un logiciel mathématique ce que le document ouvert est pour la théorie mathématique"

> CPLEX Optimizer est un logiciel d'optimisation développé par IBM utilisant des algorithmes parallèles distribués pour utiliser plusieurs ordinateurs afin de résoudre des problèmes difficiles

> Gurobi Optimizer est un logiciel d'optimisation spécialisé pour résoudre les problèmes de programmation linéaire, les problèmes de programmation quadratique, ...

> Matlab est un logiciel qui fournit un environnement de calcul numérique et de programmation, conçu par la société MathWorks

Et de nombreux autres solveurs sont appliqués à chaque domaine spécifique pour cibler l'application des bases des mathématiques et le développement de la programmation afin de fournir des outils utiles spécialisés

Dans le cadre de ce projet, j'ai implémenté un outil Solveur simple capable de prendre en charge le calcul d'expressions arithmétiques (arithmétique) et les opérations de trigonométrie

**II. Exigences particulières**

Dans ce projet, j'ai implémenté un programme qui simule un solveur simple. Le programme recevra les informations d'entrée de l'utilisateur à partir du clavier, y compris les paramètres de configuration pour le calcul à effectuer et la valeur d'entrée du calcul. Ensuite, le programme calculera et imprimera à l'écran les résultats obtenus après le processus de mise en œuvre.

**III. Description du programme**

Les données d'entrée saisies par l'utilisateur seront constituées de plusieurs lignes, dans lesquelles la première ligne est utilisée pour décrire et les lignes suivantes sont les valeurs saisies pour le calcul

La première ligne contient de nombreux paramètres de configuration. Les paramètres sont séparés par un espace. Le format de la première ligne ressemblera à ceci:

                                                   Menu_code <Autres paramètres>

Le paramètre Menu_code est utilisé pour déterminer si le solveur prendra en charge les calculs des trois méthodes de calcul répertoriées, à savoir:

- Si c'est 1 : Trigonométrie

- Si c'est 2 : Opération arithmétique

Si l'entrée (Menu_code) n'est pas valide, imprimez l'écran "Erreur d'identification du solveur" ou imprimez la valeur -1 à l'écran

D'autres paramètres seront différents pour chaque calcul et sont décrits en détail dans les sections IV, V

**IV. Trigonométrie**

1. Des données d'entrée

Lors de la sélection de la trigonométrie, les données d'entrée se composent de 3 lignes. La première ligne de données d'entrée est Menu_code, la deuxième ligne comprendra 3 paramètres de configuration et la troisième ligne est la valeur à calculer. Les données d'entrée ont le format suivant:

                                                1
                                             n  m  p
                                                x

Dans la fonction ci-dessus, les valeurs représentées par:

- n : définir le calcul (sin/cos/tan)

- m : spécifiez l'unité d'entrée (degrés/radians)

- p : précision des résultats de calcul

- x : valeur à calculer. Exemple : sin(x)

*Remarque : Si l'un des paramètres de configuration de la ligne 2 n'est pas valide, le programme imprime -1 et se termine (inutile d'entrer la valeur x)*

Les paramètres et les données d'entrée seront décrits plus en détail ci-dessous

2. Sortie des données à l'écran

La donnée de sortie sera un nombre réel, le résultat après calcul de l'opération trigonométrique et arrondi selon le principe de la section 5

3. Paramètre n

Le paramètre n est un entier spécifiant le calcul correspondant à 1 des 3 valeurs:

- Si c'est 1 : calculer sin(x)

- Si c'est 2 : calculer cos(x)

- Si c'est 3 : calculer tan(x)

Si n prend une valeur différente, c'est une valeur invalide. Le résultat de la saisie d'une valeur non valide est que le programme imprimera -1 et terminera le programme.

*Comment calculer sin(x), cos(x), tan(x) sera décrit en détail dans les sections 7 et 8*

4. Paramètre m

Le paramètre m est un entier spécifiant si l'angle d'entrée est en degrés ou en radians

- Si m vaut 0 : l'angle est en degrés

- Si m vaut 1 : angle en radians

Si m reçoit une valeur autre que les deux valeurs ci-dessus, c'est une valeur invalide, le programme imprimera la valeur -1 et se terminera

5. Paramètre p

Le paramètre p est un nombre entier précisant la précision du résultat du calcul, cette précision est le nombre de décimales prises pour afficher le résultat à l'écran. Le paramètre p n'accepte qu'un seul des trois entiers suivants:

- 2 : les résultats des calculs sont arrondis à 2 décimales

- 4 : les résultats des calculs sont arrondis à 4 décimales

- 7 : les résultats des calculs sont arrondis à 7 décimales

Si p prend une valeur autre que les trois ci-dessus, c'est une valeur invalide. Le résultat de la saisie d'une valeur invalide est que le programme imprimera -1 et terminera le programme

6. Données d'entrée x

L'entrée x est un nombre réel correspondant à l'angle d'entrée pour effectuer des calculs trigonométriques. Pour que l'approximation soit correcte, le programme n'accepte que la vraie valeur de l'angle comme suit:

- Si x est en degrés : 0 <= x <= 180

- Si x est en radians : 0 <= x <= π

Seul le calcul tan(x) aura un cas d'entrée x invalide, ce cas sera décrit dans la section calcul de tan(x)

7. Calcul sinus, cos

La formule d'expansion de Taylor nous donne un polynôme qui se rapproche d'une fonction différentiable à un point donné, le programme utilisera cette formule pour se rapprocher de la valeur de la fonction sinus, cosinus avec un angle d'entrée

La formule d'approximation de Taylor pour les fonctions sinus et cosinus peut être consultée via : https://en.wikipedia.org/wiki/Taylor_series

*Dans cette fonction, les valeurs de r et n sont les mêmes*

Cependant, avec r > 5, les éléments ajoutés ont une valeur plutôt petite, le programme calculera sin, cos selon la formule d'approximation ci-dessus mais uniquement à l'élément r = 5, à savoir

- sin(x) = x - (x^3)/3! + x^5/5! - x^7/7! + x^9/9! - x^11/11!

- cos(x) = 1 - x^2/2! + x^4/4! - x^6/6! + x^8/8! - x^10/10!

                            Remarque sur l'angle x dans la formule de Taylor

L'unité de mesure de l'angle x dans la formule de Taylor est le radian. Par conséquent, si l'angle entré dans le programme est en degrés, il est nécessaire de convertir l'angle à la valeur correspondante en radians avant d'effectuer le calcul selon la formule de Taylor. Formule pour convertir un angle de degrés en radians

                               x (degrés) = x * (π/180) (rad)

Dans lequel, le nombre π est pris approximativement égal à 3,14159

8. Calcul tan

           tan(x)=sin(x)/cos(x)

Avec sin, cos est approximé selon le point 5. Puisqu'il est calculé par la formule d'approximation, l'angle d'entrée x doit également être calculé en radians, si l'angle d'entrée est calculé en degrés, changez-le en radians comme décrit dans la section 5.

                        Remarque sur l'angle invalide lors du calcul 'tan'

tan(x) peut être indéfini lorsque cos(x) est égal à 0. Par conséquent, tan(x) n'est défini que lorsque:

- Si x est en degrés: 𝑥 ≠ 90

- Si x est en radians: 𝑥 ≠ 𝜋/2

Si la valeur de x rend tan(x) indéfini, la valeur est considérée comme invalide et le programme imprime -1

9. Opérations trigonométriques invalides

Rappel de quelques cas de trigonométrie invalide

- Le paramètre n (calcul) n'est pas 1, 2, 3

- Le paramètre m (unité de mesure) n'est pas 0,1

- Le paramètre p (arrondi) n'est pas 2, 4, 7

- Dans le cas n = 1 :

          - Si m = 0, c'est-à-dire en degrés, x  ≠  90
          
          - Si m = 1, en radians, 𝑥 ≠ 𝜋/2

**V. Calcul arithmétique**

1. Des données d'entrée

Lors de la sélection d'opérations arithmétiques, l'entrée se compose de 3 lignes. La première ligne d'entrée est Menu_code, la deuxième ligne comprendra un paramètre de configuration et la troisième ligne est la valeur à calculer. Le format des données d'entrée est le suivant

                                      2
                                      m
                                      x


Dans:

- m : définir les mathématiques (imprimer les diviseurs/facteur premiers)

- x : valeur à calculer

Remarque : Si l'un des paramètres de configuration de la ligne 2 n'est pas valide, le programme imprime -1 et se termine (inutile d'entrer la valeur x)

Les paramètres et les données d'entrée seront décrits plus en détail ci-dessous

2. Des données de sortie

Les données de sortie seront décrites spécifiquement pour chaque opération arithmétique et présentées en détail dans les sections 5 et 6

3. Paramètre m

Le paramètre m est un entier précisant le calcul correspondant à 1 des 2 valeurs suivantes

- Si c'est 1 : Imprimer les diviseurs de x

- Si c'est 2 : décomposer x en un produit de facteurs premiers

Si m prend une valeur différente, c'est une valeur invalide. Le résultat de la saisie d'une valeur invalide est que le programme sera à -1 et terminera le programme

4. Données d'entrée x

L'entrée x est un entier supérieur à 1 correspondant au nombre à calculer arithmétique. Toute entrée x inférieure ou égale à 1 est considérée comme une valeur invalide

5. Imprimer les diviseurs d'un nombre

Le programme effectue l'impression de tous les diviseurs de x (c'est-à-dire les nombres par lesquels x est divisible). Avec les exigences suivantes:

- Les diviseurs sont imprimés du plus petit au plus grand

- Chaque diviseur est séparé par un espace

- Fin de l'impression sans espaces supplémentaires autorisés

- 1 et x sont également calculés comme diviseurs de x

6. Analyse des facteurs premiers

Le programme effectue l'analyse du nombre x en facteurs premiers. Le format de la sortie est décrit comme suit:

              d1^p1*d2^p2*d3^p3...

Dans:

- d1, d2, d3,..., dn : Facteurs premiers

- p1, p2, p3,..., pn : Exposants des facteurs premiers

- ^ : Opérateur exponentiel

- * : Opérateur de multiplication

Quelques remarques :

- Le facteur premier sera imprimé si son exposant est supérieur à 0

- Les facteurs premiers sont imprimés du plus petit au plus grand

- Les facteurs premiers et les exposants sont tous deux des entiers positifs

















