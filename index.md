Bu web sayfasında Doktora çalışmam ile ilgili günlük niteliğinde bilgiler/notlar yer almaktadır.

# Doktora Günlüğü (PhDiary)
## 21.05.2021
> Okan Hoca ve Sercan Hoca ile toplantı yaptık. Topic Modeling ile elde edilen sonuçlar
> yorumlanmaya çalışıldı. Deneme sadece **323** kelime üzerinden yapıldığı için pek anlamlı
> yorumlamalar yapılamadı. Tüm bu süreç içerisinde çalışmalarımızı seçtiğimiz alan olan 
> **Biochemistry & Molecular Biology** üzerinden kurgulamıştık. Fakat bu alanda **domain
> expertise** olarak yeterli donanıma sahip olamamamızın dezavantajını yaşayabileceğimizi
> düşündük. Bundan dolayı **Web of Science** üzerinden yeni bir alan için veri seti oluşturmaya
> karar verdik. Bu alan **Computer Science>Artificial Intelligence>Natural Language Processing>**
> olabilir diye düşünüyoruz. 

## 17.05.2021
> **Topic Modeling** ile denemeler yapmaya çalıştım. Üç farklı yöntem denedim **LDA**, **NMF** ve **LSI**.
> **Word Embedding** vektörleri üzerinden word pairler arasındaki benzerliği/yakınlığı ölçmek için de
> **Cosine Distance** ve **Euclidean Distance** yöntemlerini kullandım. Bu Topic Modeling çalışmaları,
> **Cosine Similarity** anlamında şimdilik en iyi sonucu veren **FastText + Single LSTM** modelinde
> elde edilen vektörler üzerinde uygulandı. Görselleme aşamasında ise **pyLDAvis** kullanıldı.

## 13.05.2021
> **ProofReading** firmasından inceleme sonucu geldi. Yapılan düzeltmelerin üzerinden geçilerek 
> derginin deadline olarak vermiş olduğu **17 Mayıs 2021** tarihi öncesinde sisteme makalenin
> yeni hali yüklendi.

## 05.05.2021
> Okan Hoca ve Sercan Hoca ile toplantı yaptık. Uçtan uca bir **pipeline** denemesini
> nihayete erdirmek için **323 kelimelik** set ile ilerlemeye karar verdik. Testlerde
> şimdilik en iyi sonuç veren **"FastText, Single LSTM"** modeli ile tahmin edilen
> sonuçlar kullanılmaya karar verildi. **Görselleme** anlamında karşılaştırma yapabilmek adına 
> **Topic Modeling (LDA vb. gibi)** yöntemleri kullanılmaya karar verildi. 
> **2014 Aralık**, **2017 Aralık Gerçek** ve **2017 Aralık Tahmin** senaryoları için Topic Modeling
> uygulanacak ve buradaki benzerlikler ve değişimler gözlemlenecek. Bu üç durum için
> kullanılacak olan yapı **FastText** word embedding **(300 boyutlu)** temsili üzeriden 
> kelime çiftleri arasındaki **Cosine Distance/Cosine Similarity** şeklinde hesaplanacak.  

## 03.05.2021
> **323 kelimelik** (her ay için en yüksek frekansa sahip kelime) set üzerinden hem **Word2Vec**
> hem de **FastText** word embedding temsilleri üzerinden çeşitli LSTM yöntemleri denendi.
> Denenen LSTM yötemleri
> * Single LSTM
> * Stacked LSTM
> * CNN LSTM
> * Encoder-Decoder LSTM
> * Bi-LSTM

## 19.04.2021
> **Expert Systems with Applications** dergisine düzeltilmiş olarak gönderdiğimiz yayın için
> olumlu bir haber geldi. Resmi olarak kabul edilmeden önce **proofreading** yapılması istendi.
> Makalemizi yazarken **Latex** arayüzü kullanılmıştı. Proofreading yapan firma **Word** formatı
> bekliyor. Bu nedenle önce makaleyi Latex formatından Word formatına çevirdik. Bu çevirim
> sırasında bazı problemler **(Tablo metinleri, Referanslar, satır sonu kelimeleri vb. gibi)**
> yaşanabiliyor. Word hali üzerinden gerekli düzenlemeler yapıldı. Proofreading için
> ilgili firmaya gönderildi.

## 17.04.2021
> Her **aydan** bir kelime seçerek **(bir önceki ayda olmayan ve en yüksek frekansa sahip)** kelime listesini
> oluşturdum. **1991 Ocak** ile **2017 Aralık** aralığı **(324 ay)** için **323** kelime oldu. Sadece **1 ay** 
> için yeni bir kelime bulunamadı. 
> 
> Denemeleri **UHEM'de** yaptım. Bu şekilde **324 ay** için Centrality hesapları **11 saat** sürdü. Centrality 
> değerleri  üzerinden tüm kelimeler için **LSTM** hesaplaması da **40** dakika sürdü.  Oldukça iyi gözüküyor süreler. 
> Centrality  eğitiminde feature sayımız **3** oluyor **(Degree, Betweenness, Closeness)**
> 
> **2014 Aralık ile 2017 Aralık** (Actual ve Predict) aralığındaki Centrality değişimlerini büyükten küçüğe doğru hesaplattım.

## 12.04.2021
> FastText ile de LSTM modeli eğittim ve **2014 Aralık** - **2017 Aralık** arasındaki değişimleri karşılaştırdım
> **(Predict vs. Actual)**. Word2Vec'te olduğu gibi ilk **1000** içerisinde yine **8** tane eşleşme çıkıyor. Bu arada
> **pairler** Word2Vec ile FastText için farklı çıkıyor.
> 
> **Centrality** ile ilgili de inceleme yapmaya çalıştım. **Python** tarafında **networkx** paketi ile oluşturulacak
> **graf** üzerinden centrality hesaplamaları **(Degree, Betweeness, Closness, Eigenvector vb.)** rahat bir şekilde 
> yapılabiliyor. Ben deneme amaçlı ufak bir örnek yaptım ve çalışıyor. Ay bazlı bizim vocabulary setimiz **(5148 kelime)** 
> için graf oluşturmamız gerekiyor öncelikle. **Düğümlerimiz** kelimeler oluyor. **Edge** değerleri de **co-occurence** sayıları.
> Buradaki sıkıntımız pair sayımız oldukça fazla **(~13 Milyon)**
> 
> Tek bir ay için pairler üzerinden Centrality hesapları **9.5** saat sürdü UHEM otrtamında. Oldukça fazla.


## 09.04.2021
> **FastText** modeli ile **1991 Ocak** ile **2017 Aralık** ayları arasında model eğitimi
> **Word2Vec** modelindeki benzer **parametre ayarlamaları** ile tamamlandı. **FastText** modelinde de
> **2017 Aralık** sonunda kelime sayısı **5148** olarak hesaplandı. Bir sonraki adımda **LSTM**
> eğitimleri ile devam edileek.
 
## 07.04.2021
> **UHEM'deki** sunucu ortamı üzerinde **Centrality** hesaplamaları deneme amaçlı **1991 Ocak**
> ayı için yapılmaya çalışıldı. Fakat sunucuda başlatılan proses yaklaşık **1 saat** sonra
> sistem tarafından **TIMEOUT** gerekeçesiyle durduruldu. Bu konu ile ilgili **UHEM** tarafına
> bir danışmak gerekecek. UHEM'deki sistemlerde **9 Nisan - 13 Nisan** arası bakım işlemleri
> yapılacağından daha fazla kullanım şansı şimdilik olmadı.
 
## 03.04.2021
> **Centrality** hesaplamasının nasıl yapılacağı ile ilgili araştırmalar yapıldı.
> Genellikle gördüğüm kadarı ile **Python'da** yer alan **networkx** paketi ile bir **Graf**
> üzerinden centrality hesaplamaları yapılmakta. Grafı oluşturmak için ise **Node**
> ve **Edge** yapılarına ihtiyaç var. Bizim senaryomuzda **Node** yapısı **Word2Vec** modeli
> ile belirlenen **kelimeler** oluyor. **Edge** yapısı ise kelimelerin birlikte ne kadar
> bir arada geçtiğinin **(Co-Occurence)** sayısı olarak değerlendirilebilir.
> 
> Edge yapısını oluşturmak için Python'daki **Dictionary** yapısı kullanılarak 
> kelime pairleri/çiftleri arasındaki birlikte ne kadar kullanıldığı sayısı
> hesaplanabilir.
> 
> **Node** ve **Edge** bilgileri oluşturulduktan sonra **Graf** yapısı kolaylıkla
> oluşturulabiliyor. Graf üzerinden de çeşitli **centrality** skorları
> hesaplanbiliyor: **Degree Centrality, Betweenness Centrality, closeness centrality,
> Eigenvector_centrality**

## 31.03.2021
> Okan Hoca ve Sercan Hoca ile toplantı yaptık. Model çıktılarını daha güçlü ve iyi
> yorumlayabilmek adına **Centrality** hesaplamalarının da modele dahil edilmesinin
> iyi olacağı düşünüldü. Centrality olarak farklı alternatifler yer almakta: 
> **Degree Centrality, In Betweenness Centrality, Closedness Centrality**
> **Ay bazlı** kelimelerle ilgili centrality skorları üzerinden bir LSTM model
> üzerinden eğitim ve tahminler yapılabilir. Bu konuya bakılması gerekecek.
> 
> **Word2Vec** yönteminin yanında **FastText** ve **BERT** ile feature setler de
> oluşturulabilir dedik. İlk olarak **FastText** denemesi yapılacak.
> **Deep Neural Network** açısından da **LSTM'in** yanısıra **CNN-LSTM**, **Attention Network**
> denemeleri yapılabilir.

## 28.03.2021
> LSTM modelinin kurulması, Cosine Similarity hesaplama gibi adımlar seçilen 111 kelime 
> üzerinden test edilmiş oldu. Bundan sonraki aşamada Word2Vec modelin **2017 Aralık**
> sonunda ulaştığı **5148** kelimesi kullanılarak benzer hesaplamalar üzerinde çalışıldı.
> 5148 kelimenin tamamının eğitilmesi ve sonuçların alınması yaklaşık **20 saat** sürüyor.
> Kelime sayımız 5148 olunca pair sayımız da **13248378((5148X5147)/2)** yüksek oluyor
> beklendiği gibi. **Top 1000** içerisinde ortak kelime sayısı **8** oluyor. **Top 100000**
> içerisinde ise bu sayı **8393** oluyor.
> 
> *13248378 çift içerisinden seçilen rastgele 1000 tanesinin en az 8 tanesinin en çok değişen 1000 çift arasında olma ihtimali nedir?*
> **5.600025825700728e-14**

## 23.03.2021
> **2014 Aralık** ile **2017 ARalık** (Actual vs. Predict) arasındaki **Cosine Similarity** 
> değişimlerini incelemeye çalıştım. Değişimin en fazla olduğu **Top N** kelimeler içerisinde 
> Actual ve Predict arasındaki kesişimleri inceledim. Bu denemede Kelime sayımız **111** 
> olduğu için normalde pair sayısı **6105((111X110)/2)** oluyor. Bir tane kelime **2014 Aralık Vocabulary'sinde** 
> olmadığı  için pair sayımız **5995** oldu. **Top 100** içerisinde ortak kelime sayısı **9** oluyor.
> Aşağıdaki gibi olasılık hesapları da yapılmış oldu.
> 
> *Yaptığın deney için 6105 çift içerisinden seçilen rastgele 10 tanesinin hiçbirinin en çok değişen 10 çiftten biri olmama ihtimali nedir?*
> **0.9837282857823166**
> 
> *6105 çift içerisinden seçilen rastgele 100 tanesinin en az 9 tanesinin en çok değişen 100 çift arasında olma ihtimali nedir?*
> **2.8236333183468444e-05**
> 
> **Cosine Similarity** değerlerimiz negatif de olabiliyor. Sanırım bu hali ile **Gephi'de** 
> görüntüleme sıkıntıya yol açabiliyor. Ben de örnek olarak değerleri **0-100** arasında 
> scale ettim. Bu şekilde Actual ve Predict için Gephi grafikleri elde edilebiliyor.

## 21.03.2021
> **2014 Aralık** ayından **2017 Aralık** ayına (hem Actual hem de Predicted için)
> **benzerliği** en çok değişen kelimeleri bulma ile ilgili çalışmalar yaptım.

## 19.03.2021
> Modeldeki sıkıntıyı giderdim. **2014 Aralık** inputundan **2017 Aralık** outputunu
> elde ettim. **Actual** ve **Predicted** Word2Vec vektörlerinden **pair-wise** olarak 
> **Cosine Similarity** hesaplattım. Böylelikle elimizde **Co-Occurence** benzeri 
> matrisler olmuş oldu. Bu matrisleri **Gephi** üzerinde görsellemeye çalıştım, 
> henüz başaramadım.

## 15.03.2021
> Okan Hoca ile konuşurken LSTM modelinin yanlış kurulduğunu fark ettim.
> Model eğitimi ve tahminleri tekrar yapmaya çalışacağım.  

## 13.03.2021
> **%5** stratejisi kullanıldığında **111** kelime belirlenmiş oldu. **LSTM modeli** üzerinden 
> prediction yaptım. Ortalama **2 saat** civarı sürdü gibi. **2017 Aralık** için actual 
> **Word2Vec** değerleri ve predict edilen Word2Vec değerlerini elde ettim. 
> Görselleştirmeyi **(Gephi, Pajek vb.)** nasıl daha iyi yapabiliriz ona da bakmaya çalışıyorum.

## 08.03.2021
> **Pipeline** kurmak amaçlı **Vocabulary** oluşturma denemelerini tamamladım.
> **1991 Ocak** ayından başlayarak her ay **yeni eklenen** kelime sayısının
> **%5** kadarını Vocabulary içerisine dahil etme kararı aldık. Bu şekilde olunca
> **bazı aylar** için hiç kelime eklenmediği oldu. Şimdilik pipeline kurmak 
> amaçlı bu strateji ile ilerlemeye karar verdik.
 
## 03.03.2021
> Okan Hoca ve Sercan Hoca ile toplantı yaptık. Toplantı **verimli** geçti.
> Literatür taraması ile ilgili sonuçlar üzerinde duruldu. Bizim konumuza
> çok yakın bir çalışma gözükmemekte. Literatür taramasını biraz daha
> **derin** incelemek gerekecek özellikle yöntemlerin kullanış şekli anlamında.
> LSTM network ile ilgili tüm kelimeler yerine **ay** bazlı **yeni** dahil olan
> kelimelerin **%5'i** seçilecektir. Yeni dahil olan kelimeler de **frekans**
> sayılarına göre önce sıralanacaktır. **Pipeline** kurulduktan sonra
> farklı, **state of art** kelime temsil yöntemleri de kullanılacaktır
> **(BERT, FastText, XLNet, ELMo)**

## 01.03.2021
> Tezin ikinci kısmı ile lgili çalışmada LSTM network kurulumunu
> **Word2Vec** sözlüğündeki her bir kelime bazında oluşturmayı düşündük.
> **2017 Aralık** ayı sonunda eğitilmiş olan Word2Vec modelindeki
> kelime seti baz alındı. Bu sözlükteki her kelime için **1991 - 2017**
> seneleri arasında ay bazlı **(27 * 12 = 324 ay)** Word2Vec değerleri
> kullanılarak eğitim seti oluşturuldu. Bu eğitim seti üzerinden de
> her kelime için bir LSTM network kuruldu.

## 20.02.2021
> Okan Hoca ve Sercan hoca makale ile ilgili içeriğin
> yeni halini tamamladılar. Makalenin son hali üzerinden
> **inceleme** yapıldı, **referanslar** kontrol edildi. Bir referans
> ile ilgili **Bibtex** olarak **Article** şablonu uygun olmuyordu
> **Volume** ve **Page** bilgileri olmadığı için. **Misc** şablonu
> kullanılarak sorun giderildi. Makalenin gönderileceği
> **Elsevier** arayüzünde **Orcid ID** ile ilişkilendirme sırasında
> sistemsel bir **hata** ile karşılaşıldı. Makale Dergi Editörüne
> e-posta ile ulaştırıldı ve onlar tarafından sisteme kaydedildi.

## 19.02.2021
> Dergiden düzeltme için geri dönen makale ile ilgili
> çalışmalara devam edildi. **Deep Neural Network** ile ilgili
> şekillerde ufak düzeltmeler yapıldı. Litreatür taraması ile
> ilgili bir **tablo** hazırlanması istenmişti. **Okan Hoca** ve **Sercan
> Hoca'nın** oluşturduğu tablo **Latex** formatına dönüştürüldü. 
> Yayındaki çalışmanın temel yapısını anlatan **figür** yeniden oluşturuldu. 
> Son hali ile daha güzel bir anlatım sağlandı. Figür için 
> [Diagrams - Draw.io](https://app.diagrams.net/) uygulaması kullanıldı.

## 02.02.2021
> Devam edilen proje ile ilgili **Feature Map** oluşturma ve **LSTM**
> uygulanması ile ilgili kod geliştirmesi yapıldı.

## 27.01.2021
> Bugün **Tez-2** ilerleme sunumunu yaptım ve **başarılı** sonuçlandı.
> Jüri üyelerinin genel izlenimi **olumlu** oldu. Tezin ikinci kısmı
> ile ilgili çalışmalara son sürat devam edeceğim.

## 19.01.2021
> Üzerinde çalıştığımız yeni konuya ilişkin elde ettiğim
> **literatür** taramasına dair sonuçları hocalarımla paylaştım.
> **27 Ocak Çarşamba** günü gerçekleşecek **Tez-2 İlerleme** Jüri
> toplantısı için **sunum** hazırlamaya başladım.

## 16.01.2021
> Dergi ile ilgili aksiyonlar üzerinde çalışmanın yanı sıra
> üzerinde çalıştığımız yeni konuya da devam ettim. İlk olarak
> ay bazlı oluşturulan **Word2Vec** modellerini kayıt ettim.
> **Literatür** çalışması olarak da farklı **anahtar kelime**
> kombinasyonları ile **Google Scholar** üzerinde
> araştırmalar yaptım.

## 13.01.2021
> Bugün dergiden gelen inceleme sonuçları ile ilgili
> bir **toplantı** yaptık. Aksiyon planı çıkarıldı ve 
> hızlı bir şekilde düzenleme yapılmasına karar verildi.

## 12.01.2021
> Dergiden gelen hakem değerlendirmeleri içerisinde yer alan ve
> tavsiye edilen **4 yayını** inceledim. Değerlendirmelerle ilgili
> hazırladığım cevapları hocalara gönderdim. 

## 10.01.2021
> Dergiden gelen **hakem değerlendirmeleri** ile ilgili çalışmalara başladım.
> İlk olarak istenen şeyleri madde halinde listelemeye çalıştım. Toplam
>  **12 madde** yer almakta. **4 madde** için bir şeyler yaptım. **13 Ocak Çarşamba** 
> günü ayrıca bu konuya dair Okan Hoca ve Sercan Hoca ile birlikte bir
> toplantı yapacağız.

## 09.01.2021
> Word2Vec ile ilgili Vocabulary oluşturma çalışmalarının **üçüncü**
> parçası da tamamlanmış oldu. Öte yandan **Expert Systems with Applications**  
> dergisine gönderdiğimiz makale için **revision** isteği geldi. Makale
> genel anlamda **beğenilmiş** gözükmekte. Review eden hakemlerin
> yorumlarına göre makaleyi geliştirip **6 Şubat** tarihine kadar göndermek
> gerekiyor.

## 07.01.2021
> Word2Vec ile ilgili Vocabulary oluşturma çalışmalarına başladım.
> 1991 - 2017 yılları arasını **3 parça** olacak şekilde bölümledim. 
> (1991 - 2000, 2001 - 2010, 2011 - 2017). İlk parça olan
> **1991 - 2000** arasını tamamladım. Öte yandan **UHEM** ortamında
> basit şekilde ilk **Python** denemesini yaptım bir **virtualenv**
> düzenleyerek. Sunucuya iş verip çalıştırtabildim.

## 05.01.2021
> Word2Vec çalışması ile ilgili **tavsiye** almak için hocalara mail attım.
> **Stop Word** işleminin daha sonradan uygulanabileceğini söylediler.
> 1991 - 2017 arasında **ay** bazlı WordVec modeli oluşturmaya başladım.
> Google Colab üzerinde devam eden çalışma **12 saat** sonrasında
> **2009** yılını işlemeye devam ederken sistem tarafından durduruldu.
> Büyük ihtimalle Google Colab hizmetinin gün içerisinde izin
> verilen **ücretsiz kullanım limiti** aşıldı. Bir sonraki gerçek denemede
> **10'ar** yıllık periyotlar halinde yapılması sanırım daha iyi olacak.
> Danışman hocam ayrıca **convolution layera sahip bir sinir ağıyla
> gözetimli öğrenme modeli** kurulması ile ilgili çalışmalara bakmamı istedi.
> Bir yandan da **Literatür** taraması yapmak gerekecek.

## 04.01.2021
> Tez Jürisine hazırlanan **İlermeme Raporu** gönderildi. Word2Vec temsili için kendi Vocabulary
> setimiz nasıl dahil olabilir onu araştırmaya devam ediyorum.

## 03.01.2021
> Elimizdeki büyük veri için ay bazlı **Word2Vec** temsili yapmaya çalıştım. Model kaydedilip
> her ay için güncellenerek devam ediyor. İlk yıl - 12 ay için bu denemeyi yaptım. **Vocabulary**
> beklendiği gibi her ay sonrasında artıyor. Şu an buradaki tek sıkıntı **Bag of Words/CountVectorizer**
> ile daha önceden oluşturduğumuz **4064** kelimelik set ile nasıl bir ilişki kuracağımız.
> **Phrases/Phraser** yapısı ile **stop word** elemeleri **Bigram** ve **Trigram** yapılarını etkiliyor gözükmekte.

## 01.01.2021
> Co-Occurence matris yerine denemeye karar verdiğimiz **Word2Vec** temsili için
> inceleme ve araştırmalar yaptım. Gördüğüm kadarı ile **CountVectorizer** ya da **TF-IDF**  
> gibi bir **vocabulary** üzerinden temsil inşa etme şansı yok gibi. Ayrıca direkt olarak
> **BiGram** ve **TriGram** seçenekleri de yok. Bunun yerine **Phraser/Phrases** yapıları üzerinden
> çoklu yapılar oluşturuluyor gözükmekte. Elimizdeki büyük veri için Word2Vec temsili
> başarılı olarak oluşturulabilecek mi deneyeceğim.

## 30.12.2020
> [UHEM](https://portal.uhem.itu.edu.tr/index.php) tarafından onaylanan başvuru için 
> kurulum ve basit denemeleri yaptım. [Wiki UHEM](http://wiki.uhem.itu.edu.tr/w/index.php/Ana_Sayfa)  
> sayfası üzerinden yönergeleri izledim. Önce **Open VPN** kurulumu yapıp UHEM sunucusuna bağlandım.
> Sonra **Putty** üzerinden **SSH** ile sunucuya bağlandım ve home dizinimin verilmiş olduğunu
> doğruladım. Grafik arayüz olarak **X2Go Client** ile de sunucuya bağlanabiliyor. **WinSCP**
> ile **FTP/SFTP** bağlantısı da başarılı oldu. Bilgisayar ve İşlemci kapasitesi oldukça
> yüksek gözüküyor. RAM kapasitesi de yine yüksek. 

## 28.12.2020
> Okan Hoca ve Sercan Hoca ile toplantı yaptık. Co-Occurence matris boyutunun dezavantajından 
> kurtulabilmek için neler yapabiliriz onları konuştuk. Co-Occurence matris yerine **Word2Vec** 
> ve **BERT** ile bir temsil yapmaya karar verdik. Bu şekilde bir pipeline oluşturup sonuçlar
> nasıl çıkıyor bakacağız.
>
> Bu arada [İTÜ Süper Bilgisayar](https://portal.uhem.itu.edu.tr/index.php) kullanımı için yaptığım 
> yaptığım Doktora Öğrenci proje başvurusu kabul edildi. İlk fırsatta bu ortamı kullanabilme ilgili testler yapacağım.

## 27.12.2020
> (4064,4064) boyutu ile ilgili bellek hatası almaya devam ediyorum. Bir yandan da **Heatmap** 
> üretmek ile ilgili denemeler yaptım. Python **Seaborn** kütüphanesi ile (100,100) boyutundaki 
> bir figür üzerinde (4064,4064) boyutlu diziyi resmedebildim. Ama birkaç ay sonrası için
> bellek hatası almaya yine devam ettim. Bu durumu aşmak için lokal numpy ya da pandas 
> değişkenlerini del komutu ile kod içerisinde sildim ama maalesef bir etkisi olmadı.
> Bellek ihtiyacının neden giderek arttığını anlamaya çalışıyorum.

## 26.12.2020
> Tez-2 dersi kapsamında Enstitü'nün Doktora öğrencilerinden istediği İlerleme Raporu
> üzerinde çalıştım. İlk olarak, 2020 Bahar ve Yaz aylarında yapmış olduğumuz çalışmalar
> ve hazırladığımız yayın “Social Media-Based Feedback Retrieval for Product Analysis Using Multi-Task Deep Neural
> Networks” ile ilgili bilgiler ekledim. İkinci kısımda ise 2020 Güz döneminde başladığımız "Analysis of Emerging Science 
> Topics and trends" konusu ile ilgili yaptığımız çalışmaları ve hazırlıkları anlattım.

## 24.12.2020
> [Google Colab](https://colab.research.google.com/) ortamında doktora çalışmam ile ilgili 
> Python kodlarımı denedim. İlgilendiğim veri seti **1991 - 2020** yılları aralığında ay bazlı
> toplanmıştır. Ay bazlı **Co-Occurence** kelime matrisi ile **LSTM (Long Short-Term Memory)** 
> modeli denemeye çalışıyorum. Kelime matrsinin boyutu **(4064,4064)**. Bu boyutta bir matristen 
> ay bazlı train (eğitim) seti oluşturmaya çalışırken 1994 yılını işlerken memory (bellek) hatası aldım. 

## 20.12.2020
> Bahçeşehir Üniversitesi Bilgisayar Mühendisliği bölümünde 2017 Güz döneminde
> Doktora programına başladım. Doktora çalışma alanım **Artificial Intelligence**
> (AI - Yapay Zeka). Daha çok **Natural Language Processing** (NLP - Doğal Dil İşleme)
> ve **Deep Learning** (DL - Derin Öğrenme) konuları ile ilgilenmekteyim.
> Tez Danışmanım: [Dr. Öğr. Üyesi C. Okan Şakar](https://akademik.bahcesehir.edu.tr/web/cemalokansakar/tr/index.html)
> Tez ile ilgili uğraştığımız alanlarda bize destek veren diğer hocam: [Dr. Öğr. Üyesi Sercan Özcan](https://www.port.ac.uk/about-us/structure-and-governance/our-people/our-staff/sercan-ozcan)

## 2019
> Tez 1 (Tez Önerisi) dersi tamamlandı.
> 
> Doktora Yeterlilik Sınavı tamamlandı.

## 2018
> Aşağıdaki dersleri tamamladım.
> * Image and Video Processing
> * Statistical Data Analysis and Decision Making
> * Software Design Patterns
> * Artificial Neural Network

## 2017
> Aşağıdaki dersleri tamamladım.
> * Analysis of Algorithms
> * Machine Learning & Pattern Recognition
> * Advanced Topics in AI
> * Computer Networks and Mobile Computing
