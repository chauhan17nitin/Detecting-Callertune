# Detecting-Callertune
So Regarding the project to identify when the ring starts and stops i have used two approaches in my Assingnment.

1. The first one is the spoon feeding the approah that i was told about i taken the data into the chunks of 3 secoonds in real-time and in that the model seems performing preety well there is around a log of 0.5 seconds in that which seems obvious and i have implemented that in [Using Inaspeechsegmenter](https://colab.research.google.com/drive/1P-om9Hba1TTuU7CXySKunP6CPeLAjtz5) file. This approach is simple and works fine
2. The second one is using Deep Learning. Which is implemented in [Detecting Callertune](https://colab.research.google.com/drive/1i8XcgAR5GADnp_T76rsty_i3oFgxfYRn) So first as the dataset was less so i splitted all the sound files(which have human voices and tring tring voices) in chunks of 3-3 seconds and placed the files in two different classes. After that i created spectogram of each audio file. After that i used transfer leaning using VGG16 to classify that and achieve around 99 percent validation accuracy on the validation set.

The main aim of 2nd approach is to perform a double validation especially to differentiate between music and human sound.

So on the chunk first we will apply our Deep Learning model if it gives the output as 1 means sound of tring tring so we will classify it as ringing but if we receive a human voice it will be classified as human after that second step of checking it will be done either it is music or talking voice using the speech segmenter Library

But the lag in this approach is quite large which creates a problem for real-time implementation.
