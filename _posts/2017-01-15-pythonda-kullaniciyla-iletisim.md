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

//Diğer bir yolla:

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



Cum sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum. Sed posuere consectetur est at lobortis. Cras mattis consectetur purus sit amet fermentum.

> Curabitur blandit tempus porttitor. Nullam quis risus eget urna mollis ornare vel eu leo. Nullam id dolor id nibh ultricies vehicula ut id elit.

Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum. Aenean lacinia bibendum nulla sed consectetur.

## Inline HTML elements

HTML defines a long list of available inline tags, a complete list of which can be found on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

- **To bold text**, use `<strong>`.
- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Mark otto</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.

Most of these elements are styled by browsers with few modifications on our part.

## Heading

Vivamus sagittis lacus vel augue rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.

### Code

Cum sociis natoque penatibus et magnis dis `code element` montes, nascetur ridiculus mus.

{% highlight js %}
// Example can be run directly in your JavaScript console

// Create a function that takes two arguments and returns the sum of those arguments
var adder = new Function("a", "b", "return a + b");

// Call the function
adder(2, 6);
// > 8
{% endhighlight %}

Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa.

### Lists

Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.

* Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
* Donec id elit non mi porta gravida at eget metus.
* Nulla vitae elit libero, a pharetra augue.

Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue.

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

Cras mattis consectetur purus sit amet fermentum. Sed posuere consectetur est at lobortis.

<dl>
  <dt>HyperText Markup Language (HTML)</dt>
  <dd>The language used to describe and define the content of a Web page</dd>

  <dt>Cascading Style Sheets (CSS)</dt>
  <dd>Used to describe the appearance of Web content</dd>

  <dt>JavaScript (JS)</dt>
  <dd>The programming language used to build advanced Web sites and applications</dd>
</dl>

Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Nullam quis risus eget urna mollis ornare vel eu leo.

### Tables

Aenean lacinia bibendum nulla sed consectetur. Lorem ipsum dolor sit amet, consectetur adipiscing elit.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

Nullam id dolor id nibh ultricies vehicula ut id elit. Sed posuere consectetur est at lobortis. Nullam quis risus eget urna mollis ornare vel eu leo.

-----

Want to see something else added? <a href="https://github.com/poole/poole/issues/new">Open an issue.</a>
