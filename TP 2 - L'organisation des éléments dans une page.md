

## Une petite astuce de l'éditeur

Si vous utilisez un éditeur intelligent. Vous avez accès directement à une vision résumée de l'arbre des widgets. (Sur VS Code, le module flutter ajoute un onglet sur la barre de gauche ).

![[Capture d’écran 2023-03-10 à 11.27.35.png | 600]]

Depuis cet arbre, on peut effectuer des actions pour modifier directement l'arbre. On peut 'Wrap with ... ' et déplacer les widgets vers le haut ou le bas. 
Cliquer sur un widget nous emmène aussi directement à l'endroit du code associé. 


## Layout de base : Les widgets Row et Column


Les widgets Row et Column sont beaucoup utilisés en Flutter. Nous allons construire deux morceaux d'interface qui les utilisent. 


Nous allons essayer de reproduire ceci : 

![[Capture d’écran 2023-03-08 à 17.07.24.png]]

1. Voyez-vous comment les widgets Row et Column vont nous servir ici ? 

2. Comment construiriez-vous l'arbre de Widget pour réaliser cette barre de 3 icones ? 
	Dessiner l'arbre sur une feuille ( ou sur paint ). 

En pratique, pour customiser un widget Text ou Icon, on utilise un widget Container ( l'équivalent d'un div en html ). Un Container permet d'ajouter du padding, des marges, des bordures, ou une couleur de fond. 

3. En plus des composants que vous avez repérés, on entourera donc chaque Text d'un Container et le Row également, pour ajouter du padding. Ce qui devrait vous faire 14 widgets pour cette barre. 
		Les icones sont les suivantes: 
			Icons.local_phone
			Icons.near_me
			Icons.share

4. Implémentez cette barre dans une application vide. 

Vous pourrez vous baser sur l'exemple suivant : 
```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceAround,
  children: [
    Icon(
      Icons.favorite,
      color: Colors.pink,
      size: 24.0,
      semanticLabel: 'Texte pour les modes d\'accessibilité',
    ),
    Icon(
      Icons.audiotrack,
      color: Colors.green,
      size: 30.0,
    ),
    Icon(
      Icons.beach_access,
      color: Colors.blue,
      size: 36.0,
    ),
  ],
)
```
Le code produit ce résultat : 
![[Capture d’écran 2023-03-10 à 10.57.01.png]]


## Un peu plus de composants.


Construisez un arbre de widget pour le design ci-dessous: 

![[Capture d’écran 2023-03-08 à 17.38.24.png]]

Ensuite, implémentez-le dans une appli Flutter. 
Pensez aux espaces verticaux ( entre PREP: et 25 min par exemple )
Les codes d'icones sont 
Icons.star
Icons.kitchen
Icons.timer
Icons.restaurant



## La librairie Material 

La librairie Material est un ensemble de composants fournis par Google pour faciliter la construction d'applications. 

Dans Flutter, on peut distinguer les widgets en deux catégories:
- La librairie de widget standard
- La librairie Material. 

Dans notre dernier projet, nous avions importé la librairie Material pour pouvoir utiliser les widgets `Scaffold` et `Card`. 


Le widget Scaffold fait partie de Material, vous trouverez sur ce lien [Material Components widgets | Flutter](https://docs.flutter.dev/development/ui/widgets/material) les différents widgets Material disponibles. ( Vous y retrouverez les icones et le premier exemple que je vous ai donné ).

Implémenter une boite de dialogue ( que vous trouverez dans le catalogue ) qui s'ouvrira lorsqu'on cliquera sur le téléphone de la première application ci-dessus. Elle indiquera un numéro de téléphone et des horaires d'ouverture. 
	Pour cela, vous aurez besoin du widget GestureDetector, vous trouverez un exemple ici : [GestureDetector class - widgets library - Dart API](https://api.flutter.dev/flutter/widgets/GestureDetector-class.html)

Ajoutez également une SnackBar lorsqu'on clique sur Route pour afficher le message "Cette fonctionnalité sera disponible prochainement".

Lorsqu'on cliquera sur Share, vous ouvrirez une BottomSheet pour proposer plusieurs réseaux sociaux. 
