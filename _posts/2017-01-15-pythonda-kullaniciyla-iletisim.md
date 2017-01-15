---
layout: post
title: Pythonda kullanıcıyla iletişim 
---

Merhaba arkadaşlar. Bu yazı da kullanıcıyla iletişim yani raw_input() ve input() fonksiyonlarını inceleyeceğiz.
Kullanıcıyla iletişim kullanıcıya soru sormaya yarayan fonksiyonlardır.Örneğin kullanıcı adı sormayı yada 
parola sormaya yarayan fonksiyonlardır.Yani soruyu sorup cevabı aldıktan sonra cevabı işleme katmamızı 
sağlayan fonksiyonlardır.raw_input() fonksiyonundan başlayalım.

raw_input() fonksiyonundan çıkan değer string olur.Yani karakter dizisidir sayı dizisi değil.Yani işlem 
yapamazsınız.Örneğin;
{% highlight js %}

raw_input("Lütfen bir sayı giriniz:")

//Lütfen bir sayı giriniz:5

{% endhighlight %}
dersem bana şu şekilde;
'5' diye verecek.String olduğu için ben bunla herhangi bir işlem yapamam.raw_input'a değişken atayabiliriz.
{% highlight js %}

a= raw_input("Adınızı giriniz:") 

//Adınızı giriniz:Python

{% endhighlight %}

Dediğim zaman a ya python değerini atadık ve bunu göstermek istersem:
{% highlight js %}

print a

//Python

{% endhighlight %}
bu şekilde çıkacaktır.Başka bir örnek verirsek:
{% highlight js %}

a = raw_input("Lütfen adınızı giriniz:")

//Adınızı giriniz:Python

print "Parolanız:" , a

//Parolanız: Python
//Diğer bir yolla;

print "Parolanız: %s" %a 

//Parolanız: Python

{% endhighlight %}

Şimdi diğer kullanıcıyla iletişimi sağlayacak ikinci fonksiyonumuz input() fonksiyonuna gelelim.

input() fonksiyonunu integerlarda yani tamsayılarda kullanırız.Yani biz karekter dizisi yazdığımızda
bize hata verecektir.input() tamsayılarda kullandığımız için işlemleri bu fonksiyondan gerçekleştirebiliriz.
{% highlight js %}

a = input("Bir sayı giriniz:")

//Bir sayı giriniz:27 

print a

//27

print a-3

//24
{% endhighlight %}

Bir de b'ye de bir sayı verelim.Şu şekilde:

{% highlight js %}

b = input("Bir sayı giriniz:")

//Bir sayı giriniz:3 

print a+b

//30
{% endhighlight %}
Bunu aynı şekilde raw_inputta yazmış olsaydık.Yani input yerine raw_input olduğunu
düşünürsek ve print a+b dersek bize şu şekilde verir:
273 çünkü raw_input fonksiyonu toplayamıyor birleştiriyor.Yani matematiksel işlemlerde input'u kullanıyoruz.
Karekter dizilerinde raw_input kullanacağız.
Yanlız input'un güvenlik açıkları olduğundan dolayı bunu 
kullanmayacağız.Hem sayılarda hem de karekter dizilerinde raw_inputu kullanacağız.Ona da şöyle bir örnek verebiliriz.
{% highlight js %}

a = raw_input("raw_input")
b = raw_input("Bir sayı giriniz:")

toplam=int(a)+int(b)
print toplam

//Bir sayı giriniz:27
//Bir sayı giriniz:3
//30
{% endhighlight %}
raw_input'u kullanarak sayısal işlemleri de değişkenleri int'e çevirerek yapabildiğimizi gördük.

