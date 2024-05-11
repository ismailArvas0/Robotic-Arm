# Robotic-Arm
Robot kol ile deneyap renk sensörünün algıladığı kutuların renklerine göre ayrıştırılması.

Bu projemde Arduıno UNO kullanarak ve yerli sensörümüz Deneyap Hareket, Işık, Renk Algilayici, Mesafe Ölçer Sensörünü kullanarak mavi, kırmızı, yeşil renklerini ayıran bir otomasyon sistemi geliştirdim. Bu sistemde bir konveyör bantta bulunan renk sensörümüzün altına renkli kutularımızı koyduktan sonra algılanan renk, bantın robot kolun kutuyu alabileceği mesafeye kadar getirdikten sonra robot kolummuzun, kutu hangi renk ise o rengin yerinin kordinatına kadar kutuyu alıp kutuları renklerine göre ayırmaktadır. 


Bu projeyi yapmak için bir konveyör banta, renkleri algılaması için sensöre, bir tane mikrodenetleyiciye(ben arduıno uno kullandım siz istediğiniz kartı kullanabilirsiniz ancak kod arduıno içindir.) ve son olarak bir robot kola ihtiyacınız olacak robot kolu isterseniz kendiniz tasarlayıp kullanabilirsiniz isterseniz hazır stl dosyası bulup baskısını alabilirsiniz ya da demonte halde satılan kollardan alıp yapabilirsiniz.


ROBOT KOL: Robot kol için 4 tane servo motoruna ben MG90S model servo motorları kullandım ve servo motorların düzgün çalışması için bir Servo motor sürücüsüne ihtiyacınız olacak. Ben PCA9685 Servo Motor Sürücüsünü kullandım.

KONVEYÖR BANT: Konveyör bantı ben kendim tasarladım demir milin iki ucuna 6002 rulman taktım ve bu rulmanlara tahtadan dikdörtgen şeklinde rulmanı tutması için parça kestim. Bundan 2 tane yaptım ve birbirine paralel şekilde zemine taktım. İki milin arasını kumaştan bir bant yaptım ve onu iyice gerip diktim ve bantın dönmesi gerçekleşti. Bir tane milin ucuna 6 V 250 RPM Motor ve Tekerlek Setinin tekerini silikonla yapıştırdım ve motoru tekere takıp mili döndürdüm teker kaplin görevi görmüş oldu bu sayede.(Bu bantın temsili bir 3d çizimini paylaşıcağım lütfen ölçülere dikkat ETMEYİNİZ sadece mantığını anlamanız içindir.)
Bantın bir ucuna kutuları elle koyacağım yerin üstüne renk sensörünü tutturdum ve renk algılanınca bant hareket etti ve robot kolun yanında durdu, robot kolda kutuyu alıp rengine ayırdı. Sistem bu şekilde çalışıyor bu mantıkta ilerleyiniz.
Mili döndürecek motor için L298N motor sürücüsünü kullandım.


RENK SENSÖRÜ: Renk sensörü olarak ben size hem tcs3200 ile yazılmış bir örnek kodu paylaşıcağım ve kendi kullandığım deneyap renk sensörü ile yazılmış kodu paylaşıcağım. Tcs3200 için renk kalibrasyonu etmelisiniz ve kodunuza map() fonksiyonu ile değeri daha aralıklı bir seviyeye değiştirebilirsiniz aynı şekilde deneyap renk sensörü içinde bu geçerli ancak ben ayrı bir şekilde renk kalibrasyonu edip kodun içinde sadece değer vererek çalıştırdım. Renk kalibrasyonu etmezseniz mavi ve yeşil renkler karışabilir yada birbirinden çok farklı renkler kullanıcaksınız örneğin kırmızı, sarı, yeşil gibi ama tavsiye etmem çünkü yine karışıklık olabiliyor. Maalesef deneyap renk sensörünün fazla örnekk kodları olmadığı için yerine tcs3200 ile yapmanızı tavsiye ederim.


KOD: Kodumuzda servo motor sürücüsü için adafruit kütüphanesini kullandım. Renk sensörü için deneyap renk sensörünün kendi kütüphanesini kullandım kütüphaneleri sizlerle paylaşıcağım. 

NOT: Bu projede en büyük eksiğim bir güç dağıtım kartı kullanmamam bu yüzden 2 tane adaptör kullandım adaptörün biri 5v ve pca9685 sürücüye bağlı diğer adaptör 12v ve L298n sürücüsüne bağlı arduıno bu iki adaptörden gelen güçle çalışıyor siz bu projeyi daha da geliştirebilirsiniz benim tavsiyem bir güç dağıtım kartı kullanmanızdır. Ve eğer renk sensörü rengi düzgün algılamıyorsa ışık almasına dikkat ediniz stabil ışıkta en iyi değeri alabilirsiniz.

Robot kol projem şuanlık bu şekilde çalışıyordur. Bu tam bitmiş bir proje değildir, daha çok fazla geliştirmeye açıktır. Projemi bir protatip gibi algılayabilirsiniz.
İYİ ÇALIŞMALAR
