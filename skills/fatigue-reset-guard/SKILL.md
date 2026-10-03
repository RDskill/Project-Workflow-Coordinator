# Fatigue Reset Guard

## But
Détecter les signes de dérive dans une tâche longue et éviter de continuer sur une base devenue confuse ou contradictoire.

## Déclencheurs
Activer ce garde-fou si l’un des signes suivants apparaît :
- contradiction avec une règle déjà établie ;
- confusion entre ancien et nouvel état ;
- répétitions inutiles ;
- multiplication de prompts ou d’actions sans progrès clair ;
- oubli d’un garde-fou obligatoire ;
- erreur de contexte ou de séquencement ;
- réponse manifestement moins fiable qu’au début de la tâche.

## Action obligatoire
Quand le garde-fou se déclenche, commencer la réponse par :

`FATIGUE`

Puis :
1. STOPPER l’action en cours ;
2. ne rien modifier de plus ;
3. reprendre depuis le dernier CURRENT_STATE fiable ;
4. revalider les règles applicables ;
5. identifier une seule prochaine action ;
6. recommencer proprement à partir de ce point.

## Interdictions
- Ne pas masquer une contradiction.
- Ne pas continuer "pour finir" si le contexte est devenu douteux.
- Ne pas inventer l’état manquant.
- Ne pas rejouer inutilement des tests déjà acquis.
- Ne pas multiplier les corrections avant consolidation.

## Principe
`FATIGUE` ne signifie pas une fatigue humaine. C’est un signal opérationnel indiquant une dérive de contexte ou de qualité.
