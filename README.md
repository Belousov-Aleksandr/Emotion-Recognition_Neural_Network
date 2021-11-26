В данном разделе представлена дипломная работа курса «Data Scientist. ML. Средний уровень (нейронные сети)», которая предполагает разработку pipeline для распознавания эмоций как по статическим изображениям, так и в режиме real-time Video.
Акцент в работе был сделан на две предобученные ML-модели (VGGFace2 и BiT-M r50x1). Применяя различные методы оптимизации, такие как transfer learning, finetuning, augmentation, preprocessing, сегментация по bounding_box, dataset_balancing, multi_face/no_face cleaning, модели были обучены на оптимизированных датасетах с полными фотографиями и на датасетах с обрезанными по bounding_box лицами. Проведены эксперименты с valence-arousal разложением эмоций, когда модель обучается не на самих эмоциях, а на их разложении по этим двум компонентам. Создан скрипт, который работает с веб-камерой и выводит на экран текущую эмоцию. Разработан код генерации и отправки csv-посылки на Kaggle для проверки точности модели по Privat Score. (https://www.kaggle.com/c/skillbox-computer-vision-project)
В качестве инструментов для детектирования лиц при проведении разведочного анализа (EDA) применялись алгоритмы:  - MTCNN (Multi-task Cascaded CNN). Наиболее длительный, но в то же время, наиболее качественный алгоритм детектирования лица на фото по обязательным 7 точкам (углы глаз, углы губ, кончик носа) и необрезанному овалу лица, который включает в себя три подсети: сеть предложений (P-Net), сеть уточнения (R-Net) и сеть вывода (O-Net). - SSD (Single Shot MultiBox Detector aka 'DNN Face Detector from OpenCV'). Данный метод позволяет обнаруживать объекты на изображениях с использованием одной глубокой нейронной сети. - HAAR Cascade. Также этот метод называется методом Виолы-Джонса и является одним из лучших по соотношению показателей эффективность распознавания/скорость работы, обладая при этом низкой вероятностью ложного обнаружения лица.
Дополнительно были исследованы предобученные модели Inception_ResNet_V2, Ganeval-cifar10-convnet, Inception_V3, EfficientNet_B7, Mobilenet_v3, применялись разные типы оптимизаторов (напр.SGD, RMSProp), варьировались входящие размеры изображений, количество эпох и т.п. с целью достижения наивысшего Privte Scor, который в итоге составил 0.54.

Part 1 - https://github.com/Belousov-Aleksandr/Emotion-Recognition_Neural_Network/blob/main/Диплом_Neural_Network%20-%20Part1.%20EDA.ipynb
