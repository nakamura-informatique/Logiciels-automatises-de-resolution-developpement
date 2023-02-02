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

































