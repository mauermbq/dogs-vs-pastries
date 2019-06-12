# Hunde oder Gebäck

Einfaches Beispiel für ein convolutional neuronal network für Schüler vereinfacht erklärt.

Es werden die Datensätze aus [ieee8023/deep-learning-datasets](https://github.com/ieee8023/deep-learning-datasets) verwendet.

Die Bilddaten müssen in ein Datenverzeichnis nach Klassen aufgeteilt werden:

/Data
--/Chihuahuas ...alle Hundefotos
--/Muffins ...alle Muffins

und entsprechend der Pfadname der Variablen data_dir zugewiesen werden.

Der Aufbau des neuronalen Netzes erfolgt mit Keras und hat folgende Struktur:

* Convolutional Layer mit 32 Filtern und 5x5 Filterkernel
* Pooling Layer mit 2x2 Pixel
* Dense Layer mit 512 Neuronen, wobei der letzte Dense Layer der Anzahl der Klassen entspricht
* Categorical-Crossentropy als Loss Funktion
* stochhastical gradient descent (SGD) als Optimierungsfunktion
