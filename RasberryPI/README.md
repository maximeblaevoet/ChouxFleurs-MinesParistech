# Matériel : 

Il faudra une rasberry PI qui fonctionne, ainsi qu'une caméra compatible rasberry PI. Nous avons ici utilisé [cette caméra](https://www.amazon.fr/Raspberry-Pi-1080p-Module-Caméra/dp/B01ER2SKFS/ref=sr_1_3?ie=UTF8&qid=1551220051&sr=8-3&keywords=camera+raspberry+pi).

Il faudra de plus autoriser la caméra à fonctionner sur la rasberry PI utilisée, ouvrir le terminal et taper : 

'''
sudo raspi-config
'''

Une fois dans le menu, rendez-vous dans ** Interfacing Options ** puis dans ** caméra **. Il faut ensuite redemarrer la rasberry PI.

# Librairies : 

Le réseau de neurones a été entrainé avec Keras et Tensorflow. Nous allons donc devoir ici utiliser Keras pour charger notre modèle.
La structure du modèle et les différents poids sont présents dans le fichier * * .zip * * modelDetection. Placer le dans le même emplacement
que le script * * cf_detector.py * *.  

Il va maintenant falloir configurer la rasberry PI pour fonctionner avec différents modules : numpy, keras et openCV notamment. 

On trouvera ici les différentes instructions pour s'en occuper : 

###### Python, Numpy, etc : 

'''
sudo apt install libatlas-base-dev
'''

###### Tensorflow et Keras : 

'''
pip3 install tensorflow
pip3 install keras
'''

###### OpenCV : 

[Installation ici](rasberry PI install python with open cv)

###### Le reste : 

'''
pip3 install imutils
pip3 install numpy
'''

(numpy est normalement déjà installé avec la première ligne de commande)


# Le code : 

A ce stade la, tout peut maintenant fonctionner, il suffit de se placer dans la bonne direction dans un terminal, et de taper : 

'''
python3 cf_detector.py
'''

Une fenêtre avec la vision de la caméra va alors s'ouvrir, et la probabilité de détection devrait alors s'afficher.


