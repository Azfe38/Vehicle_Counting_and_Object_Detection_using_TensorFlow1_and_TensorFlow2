# Vehicle_Counting_and_Object_Detection_using_TensorFlow1_and_TensorFlow2
Vehicle Counting and Object Detection using TensorFlow1 and TensorFlow2 from videos and images


Python yazılım dili kullanılan bu projede TensorFlow 1 ve TensorFlow 2 açık kaynaklı bir yazılım kütüphanelerinin çeşitli hazır modelleri kullanılarak 
Araç Tespiti ve Sayımı üzerine çalışılmıştır.

Kullanılan modeller istenirse yeni ve uyumlu etiketlenmiş veriler ile eğitilerek daha iyi sonuçlar elde edebilirler.

Notlar:


1. Python 3 için uyumlu Anaconda indirilir, kurulur -> https://www.anaconda.com/products/individual

2. Anaconda Promt açılır.

3. Yeni bir environment oluşturulur conda create -n odeco python=3.7
Anaconda python dilinin son sürümünü kurar ancak son sürüm tensorflow ile uyumlu olmayabilir, 
bu nedenle tensorflow ile uyumlu bir patrhon sürümü kurulur.( bu projede environment ismi odeco, python sürümü 3.7)

4. Yeni environment aktif edilir -> conda activate odeco

5. Tensorflow API dosyası zip olarak indirilir ve çalışılıcağı yere arşivden çıkarılır -> https://github.com/tensorflow/models

6. Protobuf  " protoc-3.4.0-win32.zip " dosyası indirilir, bin klasörü içerisindeki " protoc.exe " dosyası, model-master/research klasörünün içerisine atılır.

7. cd ...model-master\research ile konum değiştirilir ve " protoc object_detection/protos/*.proto --python_out=. " komutu girilir 
ve exe dosyası protos dosyası içerisindeki dosyaları kendisi derler.

8. " ...research\object_detection\packages\tf2\ " konumndaki setup.py dosyası kopyalanır ve research klasörü içerisine bırakılır
ve " python -m pip install . " komutu girilir. " setup.py " dosyası gerekli programları kendisi kurar.
pycocotools kurulum hatası ve çözümü için " https://docs.microsoft.com/en-us/answers/questions/136595/error-microsoft-visual-c-140-or-greater-is-require.html " 
adresine gidilir, microsoft dosyaları kurulur ve yeniden başlatılırsa pycocotools hatası düzelmiş olur.
Bu adım tamamlanınca TF2 API Modelleri çalıştırılabilir durumdadır.
