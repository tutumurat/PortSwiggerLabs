# Laboratuvar: Oturum açmayı atlamaya izin veren SQL enjeksiyon güvenlik açığı

![resim](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/c89a468b-c797-4cea-b06e-25031b261381)


Bu uygulamada website üzerinde bulunan kullanıcı girişi bölümünde bir "SQL" açığı bulunmakta.

![resim-1-1024x535](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/6723b5ee-9573-4588-9f2e-1947177a4be1)


Laboratuvara eriştikten sonra bizi bir website karşılıyor.

Bu noktada "My Account" kısmına tıklıyoruz ve bizi bir üye giriş ekranı karşılıyor.

Bize verilen ipucuda yönetici kullanıcı adının "Administrator" olduğunu biliyoruz ve bunun üzerine bir deneme gerçekleştiriyoruz.

![resim-2](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/18f6515b-3a5b-401c-a7fd-107b904c3de2)


Kullanıcı adını "administrator" ve şifreyide rastgele giriyoruz.

Bu noktada Burp Suite ile bu giriş isteğini yakalayacağız. 

Log in olmadan önce FoxyProxy'i etkinleştirerek isteği yakayalım.

![resim-3](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/cf9ceab0-0407-4125-8055-239342cd2eeb)


username olan "administrator" kısmının sonuna '-- ekliyoruz. 

Bu sorgunun aşağıdaki görsel gibi olması gerekir.

![resim-5](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/0548f943-d50c-4b74-9e09-7ca5a1b8b93b)


Tırnak işaretinden sonra gelen "--" işareti geriye kalan sorguların yorum satırı olarak kalması için konur ve yalnızca tırnak işaretinden önceki sorgu çalışır.

![resim-6](https://github.com/tutumurat/PortSwiggerLabs/assets/131826005/7713f1da-89be-4052-bb8d-6efedd670315)


Bu görselde görüldüğü gibi yönetici hesabın mail adresini değiştirip ele geçirebiliriz ve yönetici bilgilerine ulaşabiliriz.
