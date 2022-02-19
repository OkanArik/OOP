# Encapsulation ilkesinden önce erişim belirteci kavramına bakalım:

![2](https://user-images.githubusercontent.com/89224500/154814945-3bba46cb-63e8-477b-9c7f-adfcb22336fc.png)

# Encapsulation ( Kapsülleme) İlkesi :
- Sarmalama ilkesi, bir sınıfa ait değişkenlerin veya niteliklerin ancak o sınıfa ait metotlar tarafından değiştirilebilmesi ve okunabilmesi ilkesidir. Bu ilke sayesinde nesnelerde oluşacak anlamsızlıkların önüne geçilebilir..
- Ayrıca değişkenlere sınıfların dışından erişim olmaması ve bir sınıf içindeki değişkenlerin nasıl ve ne kadar olacağının da başka kodlardan saklanmış olması anlamına gelir. Böylelikle biz değişkenlerimizi sarmalayarak istenmeyen durumlardan korunacak bir filtre haline dönüştürebiliriz. Bunu bir örnek ile anlamaya çalışalım..

## Encapsuliaton Örneği
- Kitap adında bir sınıfımız olsun ve bu sınıfımıza ait 3 adet değişkenimiz olsun bunlar ; kitapAdi, sayfaSayisi ve yazar. Bu değişkenlerin erişim belirleyicileri public olsun ve her sınıftan erişilsin. Kitap sınıfından oluşturacağımız bir nesne bu niteliklerin hepsini taşısın. Bu yüzden oluşturacağımız Constructor (kurucu) metodunu bu şekilde oluşturalım..

![1](https://user-images.githubusercontent.com/89224500/154815103-21ef4730-6283-48de-864c-f3781ba6ea0b.png)

- Diagram çizimi:

![2](https://user-images.githubusercontent.com/89224500/154815133-58fb8180-7e20-4b78-b6a0-2948c141eec1.png)


- Görüldüğü üzere normal bir sınıfımız ve kurucu metodumuz var. Kitap sınıfından bir nesne oluşturalım.

`Kitap book = new Kitap("Harry Potter", 500, "JK Rowling");`

- Diagram çizimi:Aşağıdaki digram nesne diagramı olarak düşünülebilir.

![3](https://user-images.githubusercontent.com/89224500/154815220-04946d7e-aa84-4234-853b-8998e5648708.png)

- Kitap sınıfından book adlı bir nesne oluşturduk ve bu nesnemizin niteliklerini belirttik. Peki biz bu kurucu metotta sayfa sayısını negatif bir değer girseydik ne olurdu ? Hiç bir kitabın sayfa sayısı negatif bir değer olamayacağı için, nesnemizde bir anlamsızlık olacaktı. Biz bu sorunu constructor (kurucu) metotumuza yazacağımız bir if kontrolü ile çözebiliriz..

![4](https://user-images.githubusercontent.com/89224500/154815285-cdfa9da8-e401-4e73-8e77-21eb1f7e6763.png)

- Constructor metodu görüldüğü gibi modifiye ettik ve nesne oluşturulurken anlamsız verilerin olmasını engelledik. Ama sorunlarımız hala bitmedi , biz nesneye ait niteliklere hala dışarıdan erişebiliyoruz ve book.sayfaSayisi = -10 dersek , nesneye ait sayfa sayısını yine anlamsızlaştırmış oluruz. Bu sorunu çözmek için sınıfa ait değişkenlere dışarıdan erişimi kapatmamız gerekir ve oluşturduğumuz değişkenlerin erişim belirleyicilerini (Access Modifiers) değiştirmemiz gerekli. Tüm public'leri private olarak değiştiriyoruz.

- Sınıfımızın son hali:

![5](https://user-images.githubusercontent.com/89224500/154815363-d649ad8f-cab8-4803-869a-4cdb510527d0.png)
- Diagram çizimi:

![6](https://user-images.githubusercontent.com/89224500/154815516-a210570a-f613-4aeb-87d8-cc8dc0a75d18.png)


- Sınıfa ait değişkenlerimin izinlerini private yaparak bu sorunu çözdük ama, biz book nesnesine ait değişkenlere erişimi tamamen kısıtladık. Yani biz oluşturduğumuz nesneye ait sayfa sayısını ekrana bastıramayız çünkü değişken private olarak tanımlandı. Ya da sayfa sayısı yanlış girilmiş bir nesneyi daha sonrasında düzenleyemeyiz. Bu sorunu çözmek için sınıfa ait değişkenlerimizi sarmalayarak, sınıf içerisinde ki metotlar yardımı ile değişkenlerimizi koruma altına alıyoruz ve kullanıma sunuyoruz. Bu metotlara sonrasında ismini çok duyacağımız Getter ve Setter metotları diyoruz.

![7](https://user-images.githubusercontent.com/89224500/154815711-6b0e05bc-4789-4969-b29c-45d68db5841d.png)

## Getter ve Setter Metotları
### Getter
- Sınıfımıza ait private değişkenler mevcut. Bu değişkenlere dışarıdan erişebilmek için her bir değişkenimiz için Getter metodu yazmalıyız. Nesneye ait bu metot çağrıldığında geriye bir değer döndürmeli ve bu değer bizim istediğimiz private değişken olmalı. sayfaSayisi değişkeni için getter metodu tanımlayalım:

![8](https://user-images.githubusercontent.com/89224500/154815844-85e12627-fab1-4031-a52e-e54ccfd5b18e.png)

- Görüldüğü gibi basit bir metot yardımı ile sınıfa ait private değişkenimize ulaşabildik. Burada dikkat edilmesi gereken noktalar getter metotları geri dönüşü olan metot tipindedir ve isimlendirilmesi ise get ile başlayıp sonra değişken ismi yazılmalıdır. İsimlendirmeyi bu şekilde yapmasak da çalışacaktır lakin kodun okunabilirliği adına bu kurala uyulması gerekir.
### Setter
- Biz getter metodu ile private olan değişkenimize ulaştık.Peki bu değişkenin değerini değiştirmek istediğimizde ne yapmalıyız ? Bir sınıfa ait private bir değişkenin değerini değiştirmek için, setter metodu yazılmalıdır. sayfaSayisi değişkeni için setter metodu yazalım:

![9](https://user-images.githubusercontent.com/89224500/154815945-c07efe29-1738-490a-b79e-ba8dc639078d.png)

-Görüldüğü üzere setter metodu sadece değiştirme işlemi yapacağı için void olarak tanımlandı ve bir adet parametre aldı. Bu parametre bizim yeni değerimi taşıyor olup, sınıfa ait değişkene aktarılmıştır. Ama burada hala bir sorun söz konusudur, bizler setter metodunu kullanarak sayfa sayısını negatif girebiliriz. Bu sorunu aşmak için constructor (kurucu) metotta yaptığımız gibi bir if koşulu ile bu sorunu çözebiliriz.

![10](https://user-images.githubusercontent.com/89224500/154815988-a0676765-4bcd-4aa1-9c81-3774151ad87d.png)


- Setter metodunu modifiye ederek nesnemiz için anlamsız olan durumu ortadan kaldırmış olduk. Setter metodunun genel özellikleri ise , geriye bir değer döndürmeyen metot olması ve isimlendirme yaparken başlangıç olarak set yazıp sonrasında değişken ismini yazmaktır.

- Bu örnekteki sayfaSayisi değişkenini koruma ve anlamsızlaşmasını önlemek için Nesne Yönelimli Programlamanın ilkesi olan Encapsulation (Sarmalama) ilkesinden yararlandık. Bir sınıfa ait değişkenlerimizi Getter ve Setter metotları yardımı ile sarmaladık ve istenilen şartlara göre oluşmasını sağladık.


![11](https://user-images.githubusercontent.com/89224500/154816125-4f08599e-bd9b-4d26-a7d0-9bd3f87c3af2.png)







