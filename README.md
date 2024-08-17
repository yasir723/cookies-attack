# Cookies Attack

Bir siteye girdiğimizde ve `ağ` kısmına baktığımızda, tarayıcının sunucuya tarayıcı adı, cihazın IP adresi gibi birçok bilgi gönderdiğini görürüz. Bu bilgiler arasında **Cookies** (çerezler) de bulunur. Ziyaret ettiğimizde, tarayıcı cihazımızda kaydedilen bu siteye ait çerezleri sunucuya iletir.


## Talep Yanıt İşlemi

![request and response](https://github.com/yasir723/cookies-attack/assets/111686779/e17101ac-c3aa-4346-affc-0a7eed54eeb4)

İstemci ve sunucu arasındaki her iletişimde, istemci sunucuya bir talep gönderir. Bu talep genellikle çerezleri içerir. Sunucu, yanıt olarak aynı çerezleri döndürebilir veya çerezlerin değerlerini güncelleyerek geri gönderebilir.

Çerezler genellikle şu şekilde görünür: 
```
Cookie1_name=Cookie1_value&Cookie2_name=Cookie2_value
```
Örnek olarak bu şekilde bir çerez dosyası olabilir:
```
PHPSESSID=708813902f8ca46&userName=admin
```

<div align='center' >
  <img src='https://github.com/yasir723/cookies-attack/assets/111686779/312b1392-4330-4d51-9ea8-3b353b3d0b3e'>
</div>

## Kaydetme Şekli

örnek olarak `Yasir` adlı biri `facebook` sitesini ziyaret ettiğinde, facebook Yasir için `yasir@facebook.txt` şeklinde bir dosya oluşturur ve Yasir'in cihazında kaydedeilir. tarayıcı kapatıp geri açtığında facebook Yasir'in daha önce sitesini ziyaret ettiğini cookies dosyasını kullanarak öğrenir.


## Saldırı

Bir önceki Query String Attack saldırısında URL ile gönderilen parametreleri kullanarak hassas bilgileri üzerinde değişiklik yaparak nasıl oturum çalımamızı öğrendik ancak sistem geliştiricisi bu defa hassas biglierli URL ile iletmesini ne kadar tehlikeli olduğunu anlayıp cookies kullanarak iletmeyi tercih etti ancak yine de biz hacker olarak cookies ile iletilen parametreleri değiştirip yine de oturum çalabiliriz.

Örnek olarak kullandığımız web sitede eğer bilgileri URL ile değil cookies ile iletirsek `Hareketlerim` sayfasını bu şekilde göreceğiz:

<div align='center' >
  <img src='https://github.com/yasir723/cookies-attack/assets/111686779/6c01114d-0e2f-440c-bc6f-9124559ec118'>
</div>

Bu fotoğrafta gördüğümüz gibi kullanıcı bilgileri cookies ile gönderdiğimiz için URL'da bulunmuyor ancak eğer `ağ` kısmına bakarsak gönderilen cookies bigilerinde `userName=admin` olarak iletildiğini göreceğiz:

<div align='center' >
  <img src='https://github.com/yasir723/cookies-attack/assets/111686779/9930aa15-47d1-472f-96e6-cd99b4d63d74'>
</div>


Ve biz bunu console kısmından çok kolay bir şekilde değiştirebiliriz:


<div align='center' >
  <img src='https://github.com/yasir723/cookies-attack/assets/111686779/a9bea07e-c609-4d58-88b5-77c020ba807d'>
</div>



