# Cookies Attack

Her hangi bir siteye girdiğimizde ve `ağ` kısmında baktığımızda tarayıcıdan sunuca kullandığımız tarayıcının adı, kullandığımız cihazın ip'si gibi bir sürü bilgi belege gönderildiğini gözlemleyeceğiz. Gönderilen bu bilgilerin arasında Cookies bilgisi olacaktır. bir siteye ziyaret ettiğimizde tarayıcı bizim cihazımızda bu siteyle ilgili kaydedilen çerezler dosyasını gönderir.

## Talep Yanıt İşlemi


![request and response](https://github.com/yasir723/cookies-attack/assets/111686779/e17101ac-c3aa-4346-affc-0a7eed54eeb4)

istemci ve sunucu arasında her iletişim için istemci, sunuca bir talep gönderir bu talepte çerezieri içeriyor, ardından sunucu yanıt olarak aynı çerezleri döndürür veya onun değerleri güncelleyip döndürebilir vs..
çerezler genelde bu şekilde olmaktadır. "Cookie1_name=Cookie1_value&Cookie2_name=Cookie2_value" ve örnek olarak bu şekilde olabilir "PHPSESSID=708813902f8ca46 & userName=admin.

## Kaydetme Şekli

örnek olarak `Yasir` adlı biri `facebook` sitesini ziyaret ettiğinde, facebook Yasir için yasir@facebook.txt şeklinde bir dosya oluşturur ve Yasir'in cihazında kaydedeilir. tarayıcı kapatıp geri açtığında facebook Yasir'in daha önce sitesini ziyaret ettiğini cookies dosyasını kullanarak öğrenir.

### Saldırı

Bir önceki Query String Attack saldırısında URL ile gönderilen parametreleri kullanarak hassas bilgileri üzerinde değişiklik yaparak nasıl oturum çalımamızı öğrendik ancak sistem geliştiricisi bu defa hassas biglierli URL ile iletmesini ne kadar tehlikeli olduğunu anlayıp cookies kullanarak iletmeyi tercih etti ancak yine de biz hacker olarak cookies ile iletilen parametreleri değiştirip yine de oturum çalabiliriz
