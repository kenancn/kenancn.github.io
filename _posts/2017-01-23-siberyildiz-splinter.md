---
layout: post
title: Siber yıldız sınavındaki Splinter sorusu
---

Soru şu Şekilde idi.
{% highlight js %}
//Splinter'ın bilgisayarından önemli veriler aldık, bunlarınn ne olduğu bul ve bize bildir.
{% endhighlight %}

Soruda ki pcap dosyaya ulaşmak isterseniz <a href="https://drive.google.com/file/d/0B5oAKQrb3-OhcmRqZTBER0JLZGM/view">buradan</a>
ulaşıp indirebilirsiniz.Pcap dosyasını wiresharkta açtıktan paketlerin usb portundan geldiğini görmekteyiz.Ve bu aygıtın 
fare olduğunu ve farenin konum hareketlerinin olduğunu düşünerek Tshark aracını kullanarak paketlerde ki verileri çekeceğiz.
Tshark aracı wireshark gibi paket analiz aracıdır ve fare konum hareketlerinin verileri çekmemize yarayacak.
{% highlight js %}
tshark -r splinter -T fields -e usb.capdata > data.txt
{% endhighlight %}
bu komutla -r den sonra pcap dosyamız -T ve -e parametrelermizden  sonra ise verilerin olduğu alanları belirlememizi sağlar.'>' parametresinden sonra ise verileri kaydedeceğimiz dosya ismini belirler.

{% highlight js %}
00:ff:01:00
00:fe:00:00
00:fe:00:00
00:fd:00:00
00:fb:00:00
00:fa:ff:00
{% endhighlight %}

Bize bu şekilde veriler döktü.Bu verileri ile x ve y şeklinde konum haline düzeltmem gerekiyor.Burada ise awk veri düzenleme
aracını kullanmamız gerekiyor.
{% highlight js %}
awk -F: 'function comp(v){if(v>127)v-=256;return v}{x+=comp(strtonum("0x"$2));y+=comp(strtonum("0x"$3))}$1=="01"{print x,y}' data2.txt > data3.txt
{% endhighlight %}
Awk aracı sutunlara ayırarak kullanmamızı sağlıyor.Bu komutla -F parametresiyle ':' 'ya göre ayıracağımızı belirttik.Ve
bu ayırdığımız verileri sutun bazında $1,$2,$3 gibi değişkenlere atarak fonksiyonda x ve y değerlerimizi oluşturuyor.
{% highlight js %}
-1084 -79
-1084 -79
-1083 -80
-1083 -86
-1083 -89
-1083 -97
-1083 -97
-1083 -102
{% endhighlight %}
Bu şekilde konum verilerini elde ettik bu konum verilerinden grafik çizdirmemiz gerekiyor.Bunun için ise gnuplot aracını
kullanacağız.
{% highlight js %}
apt-get install gnuplot
{% endhighlight %}
Linux'da bu komutu kullanarak yükleyebilirsiniz.
{% highlight js %}
gnuplot
plot "data2.txt"
{% endhighlight %}
Plotla çizdirdikten sonra çıkan resmin simetrisini aldığımız zaman flag çıkıyor.
<img src="/images/buldum.png"/>
