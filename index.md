## Jakarta

Introduction:

Récemment l'Indonésie envisage de changer de capitale pour s'installer à Kalimantan sur l'ile de Bornéo,la capitale Jakarta est menacé d'être submergé par l'océan.Plus de 10millions d'habitants risquent de devenir des réfugiers climatique. Cette augmentation de la hauteur du niveau de la mer est fortement dû au changement climatique. Notre projet de recherche va se centrer sur le CO2 et son influence sur le niveau de la mer. Nous allons voir si notre temps est compté ou qu'il soit tous simplement trop tard.



### La problématique

L'indonésie est-elle capable de sauver seule sa capitale d'être inondé par l'océan.

### Les méthodes

```markdown
# CO2 -> Température -> Augmentation de la niveau de l'océan
Augmentation de la hauteur du niveau de l’océan si la température augmentait de deltaT:

Volume de l’océan actuellement : 1,4*10¹⁸*m³
Surface de l’océan =3,6*10¹⁴*m²
alpha :	Dilatation thermique de l'eau =1,7*10-⁴°c-¹

deltaV=alphaVodeltaT

deltaV=Surface*Hauteur

Hauteur=deltaV/Surface

sources
[Link](url)
```

```markdown
# L'extraction de données d'une carte topographique

J'ai utilisé la bibliothèque PIL (Python Image Library) pour itérer les pixels d'une image. 
Puis j'ai utilisé une fonction pour passer des valeurs de couleur RGB aux valeurs de hauteur.

Pour optimiser le procès de création d'image, j'ai transféré les valeurs de hauteur pour chaque pixel dans une matrice numpy.
Comme ça je n'ai pas eu besoin de traiter chaque image, c'était particulièrement utile pour créer ces vidéos où j'ai complètement 
submergé la ville entière car il y avait environ 4000-5000 images par video

Pour les submersions d'images satellites, j'ai utilisé une fonction qui effectue les calculs sur l'image de la carte 
topographique, mais qui effectue ensuite la submersion sur une image satellite que j'ai déplacée et recadrée pour avoir la 
même résolution que la carte.
```

```markdown
# Progrès


![Progress](https://user-images.githubusercontent.com/96302110/163871072-ebc1b22d-22fd-4b11-93c6-d2614113558b.mp4)


```

### Les simulations

```markdown

![image](https://user-images.githubusercontent.com/96302110/163873648-548cfb65-8b39-4174-8475-3a957431526b.png)

# RPC 4.5: Scénario intermédiaire

Celui-ci est décrit par le GIEC comme le scénario intermédiaire, Les émissions plafonnent vers 2040, puis diminuent.

La variation probable de la prévision du GIEC pour le RPC 4.5 est une augmentation du niveau des océans de 32 à 63 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *53 cm*.

Selon mon programme, cela va résulter en *25.14 km2* de terres submergées par les eaux, et *8,876 personnes* seront déplacées.


# RPC 8.5: Cas extrême

Celui-ci est le scénario dans lequel les émissions continuent d'augmenter tout au long du 21e siècle.

La variation probable de la prévision du GIEC pour le RPC 8.5 est une augmentation du niveau des océans de 45 à 82 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *74 cm*.

Selon mon programme, cela va résulter en *41.62 km2* de terres submergées par les eaux, et *30,276 personnes* seront déplacées.
```
