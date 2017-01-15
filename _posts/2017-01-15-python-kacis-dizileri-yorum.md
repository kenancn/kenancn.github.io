---
layout: post
title: Pyhtonda kaçış dizileri ve yorum satırları
---

Merhaba arkadaşlar.Pyhton da işimizi kolaylaştıracak kaçış dizileri vardır.
Bunlar:

* '\'
* '\n' 
* '\t'

sola yatık olanlardır.Görevlerini şu şekilde açıklayayım.

### Kaçış Dizileri

1.. si '\n' bu diğer satıra kaydırır.Yani bu diziden sonra ki kısmı alt satıra geçirir.
örnek verecek olursak ;
{% highlight js %}

print ("Merhaba\npython") 

//Merhaba
//python
{% endhighlight %}

bize bu şekilde vermesini sağlayan kaçış dizisidir.

2.. kaçış dizi olan '\t' ise bir tab boyu kadar boşluk bırakmamıza yarar.örnek verecek olursak;
{% highlight js %}

print ("merhaba\tpython") 

//merhaba		python
{% endhighlight %}

\t bu şekilde yani tab kadar boşluk bırakmaya yarayan kaçış dizisidir diyebiliriz.
İkisinide aynı anda kullanabiliriz tabi ki. Örnekle açıklayalım yine.
{% highlight js %}

print ("Merhaba\n\tpython") 

//merhaba
//		python
{% endhighlight %}

Yani ilk önce satır atla (\n) sonra bir tab tuşu kadar boşluk bırak (\t) anlamına gelir.
3..kaçış dizisi olan '\' bu ise bize karışıklığı önlemek adına kullanılır.Örnekle izah edeyim. 
{% highlight js %}

print ("\n \t bir kaçış dizileridir") 

//
//		bir kaçış dizileridir.
{% endhighlight %}

şeklinde çıkar.
bunları kaçış dizisi gibi algılayıp görevlerini yerine getirir.
'\' bunu kullanırsam amacıma ulaşmış olacağım yine örnek vereyim.
{% highlight js %}

print ("\\n \\t bir kaçış dizileridir") 

// \n \t bir kaçış dizileridir
{% endhighlight %}

Yani istediğim şekilde çıktı.Bu karışıklığı önlemenin bir diğer yolu ise tırnak işaretinin soluna r işareti koymaktır.
Başına koyacağımız r işareti oradaki bütün kaçış dizilerini görmezden gelmesi anlamına gelir. örnek verecek olursak:
{% highlight js %}

print (r"\\n \\t bir kaçış dizileridir") 

// \n \t bir kaçış dizileridir
{% endhighlight %}

ve son olarak enbasit ve en zevkli olan ise yorum satırı.

### Yorum Satırı
 '#' bu sembolü koyarsak  bundan sonra yazacağımız hiçbir şey  işleme sokulmaz.
{% highlight js %}

//#yani kafana göre herşey yazabilirsin bu sembolden 
//#satır bitene kadar özgürsün
{% endhighlight %}
