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


























