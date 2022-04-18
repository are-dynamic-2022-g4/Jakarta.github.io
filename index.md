## Jakarta

Introduction:
Récemment l'Indonésie envisage de changer de capitale pour s'installer à Kalimantan sur l'ile de Bornéo,la capitale Jakarta est menacé d'être submergé par l'océan.Plus de 10millions d'habitants risquent de devenir des réfugiers climatique. Cette augmentation de la hauteur du niveau de la mer est fortement dû au changement climatique. Notre projet de recherche va se centrer sur le CO2 et son influence sur le niveau de la mer. Nous allons voir si notre temps est compté ou qu'il soit tous simplement trop tard.

### La problématique

L'indonésie est-elle capable de sauver seule sa capitale d'être inondé par l'océan.

### Hypothèse

L’Indonésie seule ne peut pas sauver sa capitale  , car l’augmentation de l’océan est un phénomène provoqué par la participation d’un grand nombre de pays. Donc même si l’Indonésie réduit la production de co2 ,  l’augmentation du niveau de l'océan ne sera réduite de pratiquement rien. Donc nous pensons que pour que la capitale de l’Indonésie soit sauvée , il faut que tous les pays réduisent l'émission de co2.

### L'extraction de données d'une carte topographique

J'ai utilisé la bibliothèque PIL (Python Image Library) pour itérer les pixels d'une image. 

### Traitement de données

Puis j'ai utilisé une fonction pour passer des valeurs de couleur RGB aux valeurs de hauteur. 
Pour cette fonction j'ai pris l'aide d'un ami qui étudie les mathématiques à l'université de bologne en italie.

![image](https://user-images.githubusercontent.com/96302110/163887472-d07d8ced-ab0e-4421-92fd-47420436cef4.png)
![image](https://user-images.githubusercontent.com/96302110/163887996-56c67f6a-2a95-4b33-b30b-c715671dedb0.png)
![image](https://user-images.githubusercontent.com/96302110/163890809-a27cfa3b-20b0-421e-a530-cd3b8301f758.png)
![image](https://user-images.githubusercontent.com/96302110/163890926-bfe106cc-2d9f-41a1-9b8a-71ad399d9c16.png)

### L'optimisation

Pour optimiser le procès de création d'image, j'ai transféré les valeurs de hauteur pour chaque pixel dans une matrice numpy.
Comme ça je n'ai pas eu besoin de traiter chaque image, c'était particulièrement utile pour créer ces vidéos où j'ai complètement 
submergé la ville entière car il y avait environ 4000-5000 images par video

### Image finale

Pour les submersions d'images satellites, j'ai utilisé une fonction qui effectue les calculs sur l'image de la carte 
topographique, mais qui effectue ensuite la submersion sur une image satellite que j'ai déplacée et recadrée pour avoir la 
même résolution que la carte.

### Calcul des stats

Pour calculer la surface perdu, j'ai calculé la conversion entre les pixels sur l'image et la distance en réalité avec Google Maps
Et j'ai trouvé que chaque pixel est égale à presque 110m de taille.

![image](https://user-images.githubusercontent.com/96302110/163891172-595738f1-4e6f-4d59-adc4-654e0857214f.png)

Pour calculer le nombre de personnes déplacées j'ai utilisé une carte de la densité de la population de Jakarta.
J'ai créé une fonction qui trouvé le valeur de population pour chaque pixel sur la carte de la population à partir du couleur.
J'ai dû modifier un peu la forme et la taille de la carte pour l'adapter à la carte topographique et à l'image satellite. 

![Jakarta popmap](https://user-images.githubusercontent.com/96302110/163891182-6244a6ed-2f15-4f7e-8dd6-415723627c4f.png)

![image](https://user-images.githubusercontent.com/96302110/163887350-50ddd1b7-76d8-434f-9c65-b5ab3f53e9d3.png)

![image](https://user-images.githubusercontent.com/96302110/163887383-94e6580e-9a2f-42d2-be25-325e9cee8f17.png)


# Les simulations

### Progrès

https://user-images.githubusercontent.com/96302110/163871072-ebc1b22d-22fd-4b11-93c6-d2614113558b.mp4

# Scénarios

![image](https://user-images.githubusercontent.com/96302110/163873648-548cfb65-8b39-4174-8475-3a957431526b.png)

### RPC 4.5: Scénario intermédiaire

Celui-ci est décrit par le GIEC comme le scénario intermédiaire, Les émissions plafonnent vers 2040, puis diminuent.

La variation probable de la prévision du GIEC pour le RPC 4.5 est une augmentation du niveau des océans de 32 à 63 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *53 cm*.

Selon mon programme, cela va résulter en *25.14 km2* de terres submergées par les eaux, et *8,876 personnes* seront déplacées.

### RPC 8.5: Cas extrême

Celui-ci est le scénario dans lequel les émissions continuent d'augmenter tout au long du 21e siècle.

La variation probable de la prévision du GIEC pour le RPC 8.5 est une augmentation du niveau des océans de 45 à 82 centimètres. 
Avec la valeur p de 0.5 (médiane) correspondant à *74 cm*.

Selon mon programme, cela va résulter en *41.62 km2* de terres submergées par les eaux, et *30,276 personnes* seront déplacées.

### EFO 1.0: Régression Linéaire

Nous avons calculé l'augmentation par le régression des données entre 2000 et 2020, 
alors notre prédiction n'est pas complètement en accord avec les prédictions plus fiables du GIEC.

Celui-ci est le scénario dans lequel les émissions continuent linéairement sans aucun change de la trajectoire.

Selon ce scénario, l'eau va augmenter de 4.34m jusqu'à 2100. Et cela va résulter en 719.93 km^2 de terres submergées par les eaux,
et 1,855,484 personnes seront déplacées.

### EFO 2.0: Sans L'Indonésie

Celui-ci est le scénario dans lequel L'Indonésie cesse complètement d'émettre du CO2, dès maintenant.

Selon ce scénario, l'eau va augmenter de 4.28m, une différence de 6 centimètres par rapport à la simulation 1.0. 

Cela va résulter en 713.46 km^2 de terres submergées par les eaux, et 1,826,781 personnes seront déplacées.

Alors indonésie seule peut sauver 6.47 km^2 de terres, et les maisons de 28,703 personnes à Jakarta. Une réduction de 1%.

### Critiques: 

Malgré nos recherches nous n'avons pas pu trouver d’équation liant le taux de CO2 dans l’atmosphère et le niveau d’augmentation de l’eau. Au tout début nous avons utilisé la Formule de Hansen  +/−(20ppmCO2≡1˚C≡20msealevel)  mais en regardant de plus près, à l’époque cette formule était approximativement correcte. Mais depuis l’ère industrielle l’émission de CO2 a tellement augmenté et la formule n’était plus cohérente.
![image](https://user-images.githubusercontent.com/101198713/163886294-3763a231-5ddd-4e75-a8ca-0b421f818b51.png)

Puis nous avons essayé de rentrer plus en détail avec l’augmentation du niveau de l’océan avec la puissance solaire, forçage radiatif, et augmentation du niveau de l’océan avec la température, mais les résultats n’étaient pas satisfaisant.

Nous avons dû nous rabattre sur des régressions avec les résultats et statistique du GIEC. 


### Conclusion:

On se rend compte qu’avec nos simulations, le pire scénario est que la hauteur du niveau de la mer augmente d’environ 1.34 mètres. Ce qui déplace environ 88,229 habitants. Ce qui est théoriquement pas assez grave pour déplacer autant de personnes vers une nouvelle capitale et loin des estimations qu’on peut trouver sur internet par exemple de 50% de la capitale submergée d’ici 2050. En faisant d’autres recherches nous avons remarqué qu'il n’y avait pas que le réchauffement climatique qui influence l'inondation. Il y a aussi le prélèvement d’eau souterraine qui fait plonger Jakarta.C’est la combinaison des deux qui est problématique et cela renforce aussi les innondations par rapport à la pluie. Donc finalement notre hypothèse est fausse car Jakarta peut potentiellement se sauver elle-même de cette situation, si le pays trouvait d'autre solution pour extraire l'eau potable et irrigueur ses plantations

![image](https://user-images.githubusercontent.com/101198713/163886198-0a2effd1-01b2-4163-b416-781d90819f5c.png)
![image](https://user-images.githubusercontent.com/101198713/163886268-56d008d8-c7e6-4143-aa2a-4ca0ae75bb79.png)

### Bibliographie

[Bibliographie.pdf](https://github.com/are-dynamic-2022-g4/Jakarta.github.io/files/8508513/Bibliographie.pdf)
