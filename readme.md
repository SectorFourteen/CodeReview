### L'intérêt de l'inspection de code pour l'équipe

Pratiquer l'inspection de code dans notre workflow fournit plusieurs avantages à toute l'équipe:
* Moins de bugs. Les Développeurs continuent à faire des erreurs comme d'habitude, mais l'inspection de code va diminuer le nombre de bugs présent en production.
* Meilleure sécurité. L'inspection de code facilite la recherche de vulnérabilités potentielles et leur correction avant les mises à jour sur nos serveurs.
* Partage de connaissances. Les membres de l'équipe peuvent apprendre les uns des autres en analysant le code de chacun.
* Qualité du Code. Des notions telles que la lisibilité, l'efficacité, et l'entretien du code deviennent partie intégrante du projet et favorisent sa bonne gestion sur le long terme.
* Meilleures performances. L'inspection de code aide à repérer les problèmes de performance et de régressions du code.

### Vue du workflow
1. Les développeurs utilisent des branches pour implémenter les features et corrections de bug.
1. Dès que les branches sont prêtes pour le test, les développeurs soumettent une **pull-request**.
1. Les autres membres de l'équipe font la revue de code des branches.
1. Une liste de problèmes est créée pour chaque revue.
1. Les développeurs commitent  des changements supplémentaires pour corriger les problèmes soulevés.
1. L'inspection de code de la branche est approuvée.
1. La branche est fusionnée (merge) dans la branche staging puis master et envoyée en production.

### Etape 1: Ecrire le code et envoyer une pull-request
#### Créer une branche et continuer à travailler


#### Demander une inspection de code quand la branche est prête à être testé
Juste avant d'envoyer sa branche pour le test, une inspection de code doit être demandé. L'inspection de code avant la phase de test est nécessaire pour s'assurer que les développeurs modifient tranquillement le code en fonction des commentaires qu'ils reçoivent.
Démarrer une inspection très tôt permet de ne pas avancer trop loin dans le code et devoir à le réécrire après que quelqu'un ait fait des suggestions pertinentes. Si le test de la branche a déjà commencé, avant que la phase d'inspection de code ait démarré, toutes modifications introduites vont invalider les résultats du test et la phase de test devra être relancé.

Le développeur qui cré la branche est celui qui demandera l'inspection du code pour la branche. Si plusieurs développeurs travaillent sur la même branche ils désigneront un leader qui demandera l'inspection de code.

Il est important que tous les membres de l'équipe participent aux inspections de code afin de partager leurs connaissances dans l'équipe.

#### Comment préparer une inspection de code?
Il est important de s'assurer que les personnes qui feront l'inspection de la branche auront toutes les informations nécessaires:

Rendre son code explicite avec la quantité adéquate de documents et commentaires.
Inclure des tests unitaires automatiques avec les modifications pour faciliter la validation du code.
Si la branche corrige un bug, inclure les étapes pour reproduire le bug et chaque détails nécessaires à la vérification de la correction.
Lors d'une demande d'inspection de code **(pull-request)**, fournir une description courte et pertinente de ce que la branche implémente.

### Etape 2: Inspecter le code et soumettre un feedback
#### Poster des commentaires sur les lignes de code
Une fois l'inspection de code demandée, chaque participant reçoit un mail leur demandant de commencer l'inspection de code. Le mail contient un résumé de la branche à inspecter.
#### Etablir une liste des problèmes



#### Astuces pour l'inspection de code
Ne pas inspecter plus de 400 lignes de code en une fois et effectuer des sessions d'inspection de moins de 90 minutes.
Vérifier que le correctif ou la fonctionnalité qu'une branche implémente fonctionne vraiment.
Pendant l'inspection il est souhaitable de poster des petits commentaires et bugs (issues) de façon concise et explicite plutôt que de longs commentaires difficiles à lire et indigeste.

### Etape 3: Corriger les bugs et finaliser l'inspection
#### Pousser (push) les mises à jour  sur la branche et marquer les bugs comme résolus.
Une fois que les participants à l'inspection postent leurs premiers commentaires et bugs, le développeur gérant la branche peut commencer à les corriger.

#### Valider la branche
Quand tout le travail est fini, tout le code est inspecté, Tous les bugs corrigés et tous les tests passés, la branche peut être fusionnée (merge). Il est nécessaire de garder l'inspection active durant la phase de test sur la branche staging afin de vérifier tous les correctifs des bugs découvert pendant les test.

### Livrer!
Valider, Fusionner, Déployer et Effacer
Dès que la branche est validée et fusionnée, elle peut être déployé en production. Il est évident d'effacer les branches qui ont été fusionnées déployées après quelques jours afin de garder une gestion et historique des branches propre et rangé.