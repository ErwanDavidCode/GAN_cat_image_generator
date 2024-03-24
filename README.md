# GAN_cat_image_generator
# Presentation
Ce projet en Python utilise la librairie PyTorch pour générer une image unique de chat grâve à la technologie des GAN.

# Installation
- Installer les librairies Python
```sh
pip install -r requirements.txt
```
Lorsque le programme est executé en local, les fichiers suivants sont téléchargés en local dans le répertoire cloné : 
- dataset.zip
- dataset

Ils représentent les données d'entraintement et de test. Ils ne pèsent pas beaucoup plus que 50Mo chacun. Ils peuvent être supprimés sans problème après l'entrainement.

Je conseil cependant d'exécuter ce code dans Google Colab pour bénéficier de la puissance de calcul de leurs CPU et/ou GPU. De plus, aucun fichier ne sera téléchargé en local si le code est exécuté sur Google Colab.

# Configuration de l'algorithme
Les valeurs internes utilisées pour l'algorithme peuvent être modifiés dans le fichier `TP_GAN_cat_image_generator`.
Pour n'en citer que quelques-unes importantes :

```python
BATCH_SIZE = 64
EPOCHS = 20
lr=2e-4
LATENT_DIM = 100
```

|argument|type|description|
|-|-|-|
|BATCH_SIZE|int|La taille du batch de données utilisé pour l'entrainement|
|EPOCHS|int|Le nombre d'époch utilisé pour entrainer le modèle|
|lr|float|Le learning rate de l'optimizer ("Adam" ici)|
|lr|int|La taille du vecteur latent duquel part le générateur pour initier une génération d'image|


**Remarques** : Toutes les valeurs doivente être modifiées en connaissance de cause. Aucune vérification n'est effectuée sur la cohérence des valeurs.
Le temps d'exécution peut être assez long (il restera bien sûr à moins d'une heure sur Colab pour qqs disaines d'epochs).