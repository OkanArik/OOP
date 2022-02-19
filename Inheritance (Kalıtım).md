# Inheritance (Kalıtım):
- Kalıtım, programlama ortamında da gerçek hayattaki tanımına benzer bir işi gerçekleştirir. Bir sınıfın başka bir sınıftan kalıtım yapması demek, kalıtımı yapan sınıfın diğer sınıftaki nitelik ve davranışlarını kendisine alması demektir. Kalıtımı yapan sınıfa alt sınıf, kendisinden kalıtım yapılan sınıfa ata sınıf dersek, ata sınıfta tanımlı olan her şeyin alt sınıf için de tanımlı olduğunu söyleyebiliriz..
- Eğer bir A sınıfın B sınıfından kalıtım yapması isteniyorsa, aşağıda ki şekilde tanımlanır.
![1](https://user-images.githubusercontent.com/89224500/154819131-78c0e633-c727-4501-ac30-c9d0095accef.png)
- C# için aşağıdaki şekilde tanımlanır:

![2](https://user-images.githubusercontent.com/89224500/154819177-809f2fc5-a492-4053-8eae-b7b62f01f614.png)

## Kalıtım Türleri
![3](https://user-images.githubusercontent.com/89224500/154819199-7b64842a-e95d-48d7-b9e4-6d955ca2a2b3.png)
![4](https://user-images.githubusercontent.com/89224500/154819281-b98a71c0-9057-4f30-bfb4-a6a3e4bac165.png)
![5](https://user-images.githubusercontent.com/89224500/154819317-a3e982d8-e822-4dca-9264-4357725b4ac5.png)
![6](https://user-images.githubusercontent.com/89224500/154819379-b1c0ddb2-5bfb-4383-81d2-df44da3ac1f7.png)
![7](https://user-images.githubusercontent.com/89224500/154819445-afcc262c-7c74-45bc-8f66-0196540092e5.png)
## Inheritance Mantığının örnek ile anlatımı:
![8](https://user-images.githubusercontent.com/89224500/154819690-9e7dab86-6ab5-4ea9-b8a8-9622bd43f3c4.png)
![9](https://user-images.githubusercontent.com/89224500/154819703-c7093eb1-3d20-419e-9481-52c2f3307502.png)
![10](https://user-images.githubusercontent.com/89224500/154819761-f3cc7a36-3a46-43a0-a661-0f4b8cb8d291.png)
- Son hali:
![11](https://user-images.githubusercontent.com/89224500/154819890-9e081f97-b3d5-426b-8a37-5d150e1c993e.png)
## Kalıtım'da Constructor Zinciri ve Super Anahtar Sözcüğü
- Bir sınıfa ait nesne oluşturulurken, o sınıfın bir kurucusunun işletildiğini, kurucunun çalışması tamamlandıktan sonra bellekte artık bir nesnenin oluştuğunu biliyoruz. Kurucuları da nesneleri ilk oluşturuldukları anda anlamlı durumlara taşıyabilmek için kullanıyoruz. Bu durumda, eğer nesnesi oluşturulacak sınıf başka bir sınıfın alt sınıfıysa, önce ataya ait iç nesnesinin oluşturulması ve bu nesnenin niteliklerinin ilk değerlerinin verilmesi gerektiğini söyleyebiliriz..
- İç içe nesnelerin oluşabilmesi için nesnelerin içten dışa doğru oluşması gerekir. İç-nesnenin oluşabilmesi için, nesnesi oluşturulacak sınıfa ait kurucu işletilmeye başladığı zaman ilk iş olarak ata sınıfa ait kurucu çağrılır. Eğer ata sınıf da başka bir sınıfın alt sınıfıysa, bu kez o sınıfın kurucusu çağrılır. Kurucu zinciri alt sınıftan ata sınıfa doğru bu şekilde ilerler. En üstte, kalıtım ağacının tepesindeki sınıfın kurucusunun çalışması sonlandıktan sonra sırası ile alt sınıfların kurucularının çalışması sonlanacaktır. Böylece iç içe nesneler sıra ile oluşturularak en son en dıştaki nesne oluşturulmuş olur ve kurucu zinciri tamamlanır.
## Super Kullanımı
- Eğer ata sınıfta varsayılan kurucu yoksa ve programcı alt sınıftaki kurucunun içinde ata sınıfın hangi kurucusunun çağrılacağını belirtmezse derleme hatası alınacaktır. Çünkü derleyici aksi belirtilmedikçe ata sınıfın varsayılan kurucusunu çağıran super() kodunu üretecektir. Ata sınıfın hangi kurucusunun çağrılacağı, super anahtar sözcüğü ile birlikte verilen parametrelere göre belirlenir. Nasıl ki new işleci ile birlikte kullandığımız parametreler hangi kurucunun çağrılacağını belirliyorsa, super anahtar sözcüğü ile birlikte kullanılan parametreler de aynı şekilde ata sınıfın hangi kurucusunun işletileceğini belirler.




