# Références — Formation TinyML / Edge AI

Ressources rassemblées pour la formation : visualisation et fondamentaux du machine learning, frameworks de déploiement sur microcontrôleur, tutoriels, jeux de données et publications. Les liens sont classés par thème, dans l'ordre approximatif de progression de la formation.

## Sommaire

- [Visualiser et comprendre le ML](#visualiser-et-comprendre-le-ml)
- [Fondamentaux du ML en Python](#fondamentaux-du-ml-en-python)
- [Réseaux de neurones, CNN et audio](#réseaux-de-neurones-cnn-et-audio)
- [Cours et parcours TinyML et Edge AI](#cours-et-parcours-tinyml-et-edge-ai)
- [Frameworks de déploiement embarqué](#frameworks-de-déploiement-embarqué)
- [Tutoriels et projets pratiques](#tutoriels-et-projets-pratiques)
- [Jeux de données](#jeux-de-données)
- [Outils](#outils)
- [Publications et recherche](#publications-et-recherche)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Visualiser et comprendre le ML

- [TensorFlow Playground](https://playground.tensorflow.org/) — Entraîner un réseau de neurones dans le navigateur et observer son apprentissage en temps réel.
- [Régression polynomiale (visualize-it)](https://visualize-it.github.io/polynomial_regression/simulation.html) — Démonstration interactive de l'ajustement d'un modèle et du sur-apprentissage.
- [CNN en 3D (Adam Harley)](https://adamharley.com/nn_vis/cnn/3d.html) — Visualisation 3D des couches d'un réseau convolutif appliqué à la reconnaissance de chiffres (MNIST).

## Fondamentaux du ML en Python

- [TensorFlow sans Keras (Kaggle)](https://www.kaggle.com/code/enriqueabad/using-tensorflow-from-scratch-without-keras) — Implémenter un modèle TensorFlow « à la main », sans l'API Keras, pour comprendre les mécanismes sous-jacents.
- [Introduction à scikit-learn (vidéo)](https://www.youtube.com/watch?v=-IvNzmrcyUM) — Prise en main de scikit-learn pour le ML classique.
- [Validation croisée k-fold avec Keras (Kaggle)](https://www.kaggle.com/code/stefanie04736/simple-keras-model-with-k-fold-cross-validation) — Exemple simple de validation croisée k-fold sur un modèle Keras.
- [Cycle de vie d'une figure matplotlib](https://matplotlib.org/stable/tutorials/lifecycle.html#sphx-glr-tutorials-lifecycle-py) — Explication avancée sur le lifecycle d'une figure matplotlib
- [Les forêts aléatoires expliquées (vidéo)](https://www.youtube.com/watch?v=v6VJ2RO66Ag) — Fonctionnement des random forests, avec la notion de coefficient de Gini.
- [Chaine YouTube Machine Learnia](https://www.youtube.com/@MachineLearnia/videos) — Une mine d'or si vous souhaitez comprendre **tout** sur les maths d'un réseau de neurones.
- [Vidéo de Machine Learnia sur cross-validation, KFold, etc.](https://www.youtube.com/watch?v=w_bLGK4Pteo)

## Réseaux de neurones, CNN et audio

- [Cours CNN — FIDLE (CNRS)](https://fidle.cnrs.fr/w3/archives/2023-2024/07-CNN.html) — Support de cours sur les réseaux de neurones convolutifs.
- [Notebooks FIDLE](https://www.gricad-gitlab.univ-grenoble-alpes.fr/karkars/fidle) — Notebooks d'accompagnement du cours FIDLE.
- [Image Kernels (Setosa)](https://setosa.io/ev/image-kernels/) — Démonstration visuelle de l'effet des noyaux de convolution sur une image.
- [Mel-Frequency Cepstrum (Wikipédia)](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum) — Les MFCC, alternative à la FFT pour représenter un signal audio en entrée d'un modèle.

## Cours et parcours TinyML et Edge AI

- [Introduction au TinyML — DigiKey (vidéo)](https://www.youtube.com/watch?v=kZ5uGLfvnwA) — Vidéo d'introduction au domaine.
- [REX IA embarquée (Rtone)](https://rtone.fr/blog/ia-embarquee/) — Retour d'expérience sur un projet d'IA embarquée.
- [MLSysBook (Harvard)](https://mlsysbook.ai/) — Cours et livre en ligne gratuits sur les systèmes de machine learning.
- [MLSysBook — kits TinyML](https://mlsysbook.ai/kits/) — Partie pratique, avec la carte XIAO.
- [Spécialisation Edge AI for MCU (Coursera)](https://www.coursera.org/specializations/edge-ai-mcu) — Parcours sur l'IA embarquée sur microcontrôleur. Aussi en [version YouTube](https://youtube.com/playlist?list=PL7VEa1KauMQqZFj_nWRfsCZNXaBbkuurG) en accès libre.
- [Cours TinyML — ENSEIRB (P. Kadionik)](https://kadionik.enseirb-matmeca.fr/enseirb/e3/IT398/TinyML_enseirb%20v1.0.pdf) — Support de cours, avec son [TP associé](https://kadionik.enseirb-matmeca.fr/enseirb/e3/IT398/tpTinyML_enseirb%20v1.0.pdf). La [page de l'enseignant](https://kadionik.enseirb-matmeca.fr/) est une mine d'or qui recense d'autres cours et projets.
- [makeit1898 (YouTube)](https://www.youtube.com/@makeit1898/videos) — Vidéos sur le TinyML avec l'Arduino Nano 33 BLE Sense (un peu anciennes).

## Frameworks de déploiement embarqué

### emlearn

emlearn permet de créer et d'entraîner un modèle (relativement simple) en Python, puis de le déployer en C adapté à l'embarqué.

- [Dépôt emlearn](https://github.com/emlearn/emlearn) — Bibliothèque principale.
- [Présentation par le créateur (vidéo)](https://www.youtube.com/watch?v=L534ngXv8I8) — Présentation du projet (non technique).
- [PR sur la quantification (#100)](https://github.com/emlearn/emlearn/pull/100) — Discussion sur l'usage d'int16 plutôt que de float.
- [emlearn-micropython — capture de données accéléro](https://github.com/emlearn/emlearn-micropython/blob/master/examples/har_trees/har_record.py) — Enregistrement de données, utilisé par l'exemple « brosse à dents ».
  > Les fichiers `.npy` sérialisent des données NumPy ; ils sont utilisables en MicroPython pour générer un jeu de données.
- [sklearn2c](https://github.com/EmbeddedML/sklearn2c) — Projet concurrent ([page PyPI](https://pypi.org/project/sklearn2c/)).

### TensorFlow Lite Micro / LiteRT for Micro

> Anciennement « TensorFlow Lite Micro », désormais renommé « LiteRT for Micro ».

- [Guide de démarrage LiteRT (microcontrôleurs)](https://ai.google.dev/edge/litert/microcontrollers/get_started) — Documentation officielle.
- [Exemple « hello world »](https://github.com/tensorflow/tflite-micro/tree/main/tensorflow/lite/micro/examples/hello_world) — Premier exemple officiel.
- [Spécification de quantification](https://ai.google.dev/edge/litert/conversion/tensorflow/quantization/quantization_spec) — Référence sur la quantification des modèles.
- [TF for Microcontrollers Experiments (Google)](https://experiments.withgoogle.com/collection/tfliteformicrocontrollers) — Collection de démonstrations.
- [Codelab Magic Wand](https://codelabs.developers.google.com/magicwand?hl=fr#0) — Atelier guidé de reconnaissance de gestes.
- [Déployer un modèle TF Lite sur Arduino — DigiKey](https://www.digikey.com/en/maker/projects/intro-to-tinyml-part-2-deploying-a-tensorflow-lite-model-to-arduino/59bf2d67256f4b40900a3fa670c14330) — Tutoriel de déploiement pas à pas.
- [tflite-micro-arduino-examples (officiel)](https://github.com/tensorflow/tflite-micro-arduino-examples) — Exemples Arduino officiels (non maintenus depuis 2023).
  > La toolchain est difficile à prendre en main avec Arduino. Le [fork de Gostas](https://github.com/Gostas/tflite-micro-arduino-examples) en propose une version plus récente.

### Edge Impulse

- [Edge Impulse](https://www.edgeimpulse.com/) — Plateforme « no-code » très visuelle, reposant sur de vrais outils TensorFlow Lite.
- [Liste de projets (expert network)](https://docs.edgeimpulse.com/projects/expert-network/project-list) — Exemples de projets

### STMicroelectronics

- [Cours ST Edge AI (playlist YouTube)](https://www.youtube.com/playlist?list=PL80kAHvQbh-pT4lCkDT53zT8DKmhE0idB) — Série de vidéos côté ST.
- [ST Edge AI / Cube AI](https://www.st.com/en/development-tools/stedgeai-cubeai.html) — Outil de déploiement de modèles sur STM32.
  > [X-CUBE-AI](https://www.st.com/en/embedded-software/x-cube-ai.html) est l'ancien outil (statut NRND).
- [Créer un projet dans STM32Cube AI Studio](https://wiki.st.com/stm32mcu/wiki/AI:Creating_a_project_in_STM32Cube_AI_Studio) — Guide pas à pas.
- [Opérateurs ONNX supportés](https://stedgeai-dc.st.com/assets/embedded-docs/supported_ops_onnx.html) — Référence des opérateurs pris en charge.

### NXP

- [Premiers pas avec TF Lite Micro sur i.MX (eIQ)](https://community.nxp.com/t5/eIQ-Machine-Learning-Software/Getting-Started-with-TensorFlow-Lite-for-Microcontrollers-on-i/ta-p/1124103) — Guide eIQ, avec un PDF de lab pour VS Code en pièce jointe.

## Tutoriels et projets pratiques

- [TensorFlow Lite sur ESP32 / Arduino (OpenELAB)](https://openelab.io/blogs/learn/tensorflow-lite-on-esp32) — Introduction basique au déploiement sur ESP32.
- [Reconnaissance de gestes — TF Lite + Arduino Nano 33 (UAL)](https://lab.arts.ac.uk/books/physical-computing/page/machine-learning-with-physical-computing-tensorflow-lite-arduino-nano-33) — Tutoriel pas à pas, avec son [notebook Colab](https://colab.research.google.com/github/arduino/ArduinoTensorFlowLiteTutorials/blob/master/GestureToEmoji/arduino_tinyml_workshop.ipynb).
  > Le lien d'origine vers le tutoriel du notebook est cassé.
- [Reconnaissance vocale — XIAO ESP32-S3 + Edge Impulse (MakerGuides)](https://www.makerguides.com/voice-control-with-xiao-esp32-s3-sense-and-edge-impulse/) — Tutoriel de keyword spotting, à jour et très complet.

## Jeux de données

Données MPU6050 (accéléromètre / gyroscope) sur Kaggle :

- [AirDigit — notebook TF Lite / Keras](https://www.kaggle.com/code/rkuo2000/tinyml-airdigit/notebook) — Reconnaissance de chiffres tracés en l'air, avec le [code ESP d'inférence](https://github.com/rkuo2000/Arduino/blob/master/examples/TinyML/TinyML_AirDigit/TinyML_AirDigit.ino).
- [Air-Writing Gestures A–Z et 0–9 (ESP32 + MPU6050)](https://www.kaggle.com/datasets/dinesh9890/air-writing-gestures-a-z-and-0-9-esp32-mpu-6050) — Jeu de données de gestes d'écriture, avec un [script d'augmentation de données](https://github.com/Dinesh99673/gesture-ai/blob/main/src/augment_data.py) intéressant.

## Outils

- [Netron](https://netron.app/) — Visualiseur de modèles (web et application de bureau ; [code source](https://github.com/lutzroeder/netron)).
- [Extension Google Colab pour VS Code](https://marketplace.visualstudio.com/items?itemName=Google.colab) — Utiliser les GPU gratuits de Colab depuis VS Code.
- [Viper IDE](https://viper-ide.org/) — Alternative à Thonny pour MicroPython, directement dans le navigateur.
- [OpenMV](https://openmv.io/) — IDE MicroPython, vision par ordinateur embarquée et carte dédiée ([code source](https://github.com/openmv/openmv)). À tester avec un ESP32-S3 Sense.

## Publications et recherche

- [XIAO ESP32-S3 Sense (arXiv, avril 2026)](https://arxiv.org/abs/2604.22834) — Article de recherche récent.
- [emlearn appliqué au bétail (Virginia Tech)](https://vtechworks.lib.vt.edu/server/api/core/bitstreams/f04738cb-a715-44a7-bc60-57ffdbdbcb00/content) — Article de recherche s'appuyant sur emlearn.
- [Exemple applicatif (PMC)](https://pmc.ncbi.nlm.nih.gov/articles/PMC12031393/#sec1-sensors-25-02496) — Article illustrant un cas d'usage.
- [Github par le créateur d'emlearn](https://github.com/jonnor/embeddedml/tree/master) - Notes sur le TinyML (listes de projets,  d'outils, de cours, etc.)
- Reviews du domaine (articles) :
  - Alharthi, Shahad, Muhammad Rashid, et Malak Aljabri. 2026. « [TinyML in Industrial IoT: A Systematic Review of Applications, System Components, and Methodologies](https://doi.org/10.3390/s26082550) ». Sensors 26 (8): 2550.
  - Capogrosso, Luigi, Federico Cunico, Dong Seon Cheng, Franco Fummi, et Marco Cristani. 2023. « [A Machine Learning-Oriented Survey on Tiny Machine Learning](https://doi.org/10.48550/arXiv.2309.11932) ». Version 2. Prépublication, arXiv. https://doi.org/10.48550/ARXIV.2309.11932.
  - Elhanashi, Abdussalam, Pierpaolo Dini, Sergio Saponara, et Qinghe Zheng. 2024. « [Advancements in TinyML: Applications, Limitations, and Impact on IoT Devices]((https://doi.org/10.3390/electronics13173562)) ». Electronics 13 (17): 3562. https://doi.org/10.3390/electronics13173562.

## Pour aller plus loin

- [IA sur Raspberry Pi (playlist YouTube)](https://www.youtube.com/playlist?list=PLGs0VKk2DiYz9lvgEK4YJSWszqexhLGc1) — Vers l'inférence sur Linux embarqué.
- [PyTorch ExecuTorch](https://github.com/pytorch/executorch/tree/main) — Déploiement de modèles PyTorch sur cibles edge et microcontrôleurs.
