# Programmation à relais de Radialpoint
Nos défis sont groupés autour d’un système de location de vélo.

## Behavior Driven Development
La couverture des tests est une partie importante de tout produit à succès.  Cependant, l’écriture de tels tests est souvent fastidieuse et leur compréhension est difficile pour les membres d’une équipe qui ne sont pas directement impliqués dans le codage du produit.  Le Behavior Driven Development (BDD) vise à faciliter ces tâches.  Dans cet exercice vous devrez écrire un framework simple de BDD qui devra comprendre une version réduite du langage Gherkin, un langage répendu pour l’écriture de tels tests.  Pour faciliter la tâche, vous allez tester une calculatrice simple où il vous suffira d’implémenter les quatres opérations de base: addition, soustraction, multiplication et division.

## Syntaxe des BDD
Voici un exemple de la syntaxe d’un scénario de tests pour notre calculatrice.

```
Scenario: Testing calculator operators
  Given constants:
    | name  | value   |
    | pi    | 3.14159 |
    | e     | 2.71828 |
  When I add 4 to 5
  Then I expect the value 9
  When I multiply -6 by 20
  Then I expect the value -120
  When I subtract $.e to $.pi
  Then I expect the value 0.42331
```

Dans ce scénario, chaque ligne est une action à exécuter par le framework de tests.  L’action `Given` fixe une précondition, l’action When exécute une opération sur la calculatrice et l’action `Then` valide le résultat (post-condition).  Des constantes peuvent être déclarées en utilisant le format de table ci-haut et ces constantes peuvent être utilisées avec le symbole dollar `$`.  Chaque action doit être sur une ligne séparée et les indentations sont optionnelles.  Les valeurs numériques sont seulement à titre d’exemples.  Votre code devra supporter les floats et tous les chaînes de caractères pour les noms de variables.


## Setup
0. (5%) Créez un fichier **readme** incluant des explications claires sur la façon d’invoquer votre programme sur la ligne de commande.   Vous pouvez choisir le **langage de votre choix**.  Votre programme doit accepter en paramètre le chemin vers le fichier contenant le scénario.

0. (5%) Affichez le nom du scénario qui est en cours d’exécution (i.e. le texte après le préfixe `Scenario:`)
    ```
    Executing scenario: Testing calculator addition
    ```

0. (10%) Ajoutez le support pour ce scénario d’addition:
    ```
    Scenario: Testing calculator addition
        When I add 4 to 5
        Then I expect the value 9
    ```
    et affichez un message mentionnant que le test a été exécuté avec succès.
    ```
    Executing [Testing calculator addition]
    -> When I add 4 to 5
    -> Then I expect the value 9 (success)
    Scenario [Testing calculator addition] ended successfully
    ```

0. (10%) Ajoutez le support pour ce scénario couvrant la soustraction, la multiplication et la division:
    ```
    Scenario: Testing calculator sub, mult and div
      When I add 4 to 5
      Then I expect the value 9
      When I multiply -6 by 20
      Then I expect the value -120
      When I subtract 1.5 to 3
      Then I expect the value  1.5
      When I divide 100 by 200
      Then I expect the value 0.5
    ```

    et affichez un message mentionnant que le test a été exécuté avec succès.
    ```
    Executing [Testing calculator sub, mult and div]
    -> When I add 4 to 5
    -> Then I expect the value 9 (success)
    -> When I multiply -6 by 20
    -> Then I expect the value -120 (success)
    -> When I subtract 1.5 to 3
    -> Then I expect the value  1.5 (success)
    -> When I divide 100 by 200
    -> Then I expect the value 0.5 (success)
    Scenario [Testing calculator sub, mult and div] ended successfully
    ```

0. (10%) Ajoutez le support pour les constantes
    ```
    Scenario: Testing operation with constants
      Given constants:
        | name  |  value  |
        | pi    | 3.14159 |
        | e     | 2.71828 |
      When I subtract $.e to $.pi
      Then I expect the value 0.42331
    ```

    et affichez
    ```
    Executing [Testing operation with constants]
    -> When I subtract $.e to $.pi
    -> Then I expect the value 0.42331 (success)
    Scenario [Testing operation with constants] ended successfully
    ```

0. (10%) Ajoutez la détection des erreurs:
    ```
    Scenario: Testing operation with constants
      Given constants:
        | name  |  value  |
        | pi    | 3.14159 |
        | e     | 2.71828 |
      When I subtract $.e to $.pi
      Then I expect the value 999.42331
    ```
    et affichez un message mentionant l’action qui a échoué et la valeur erronée
    ```
    Executing [Testing operation with constants]
    -> When I subtract $.e to $.pi
    -> Then I expect the value 999.42331 but got 0.42331 (failed)
    Scenario [Testing operation with constants] failed
    ```

0. (50%) Assurez-vous que votre code soit robuste:
    - supporte-t-il l’indentation sous toute ses formes?
    - supporte-t-il les valeurs positives et négatives pour toutes les opérations?
    - supporte-t-il les float pour toutes les opérations?
    - affiche-t-il des erreurs explicites pour des valeurs trop grandes ou pour la division par zéro?
    - supporte-t-il les fichiers contenant plusieurs scénarios?

