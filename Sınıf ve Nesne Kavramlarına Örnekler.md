# Sınıf Diyagram Örnekleri

## Sipariş İşlemleri Sınıf Tasarımı

![Ekran görüntüsü 2022-02-19 202212](https://user-images.githubusercontent.com/89224500/154811588-f3989c3c-7b86-47c1-b281-4a729616ca4a.png)

- 0 veya 1 müşterinin (Customer) en az 1 veya daha fazla siparişi (Order) olabilir.
- Siparişin (Order) ürünü (Product) vardır.
- Stoğun (Stock) ürünü (Product) vardır.

## Banka Yönetim Sistemi Sınıf Tasarımı


![Ekran görüntüsü 2022-02-19 202335](https://user-images.githubusercontent.com/89224500/154811675-9d5c71fe-a99b-4ff5-a470-75d28651515b.png)

- Bankanın (Bank) ATM, Müşteri (Customer), Hesap (Account) sınıfları vardır.
- 1 müşterinin (Customer) en az 1 en çok 2 hesabı (Account) olabilir.
- 1 hesap (Account) 0 veya daha fazla ATM işlemi yapabilir.
- Hesap (Account) sınıfına ait iki tane alt sınıf vardır, Ana Hesap (Main Account) ve Birikim Hesabı (Saving Account).

## Şirket Yönetim Sistemi Sınıf Tasarımı

![Ekran görüntüsü 2022-02-19 202428](https://user-images.githubusercontent.com/89224500/154811711-fcd795f3-cbf6-4e7e-874c-73a4ef3277a1.png)

- Şirketin (Company) 1 veya daha fazla departman (Department) ve ofisi (Office) vardır.
- Şirket (Company) olmadan departman (Department) ve ofis (Office) olamaz.
- Bir departmanın (Department) en az bir çalışanı (Employee) olmalıdır.
- Bir departman (Department) bir çalışan (Employee) tarafından yönetilir.
- Ofise (Office) ait bir merkez ofis (Headquarter) olabilir.

## Okul Yönetim Sistemi Sınıf Tasarımı

![image](https://user-images.githubusercontent.com/89224500/154811813-2c44e5e2-11ff-4989-ace5-e50ea5dfeebb.png)

- 1 okulun (School) en az bir veya daha fazla departmanı (Department) olabilir.
- En az 1 veya daha fazla okulun (School) birden fazla öğrencisi (Student) olabilir.
- 0 veya daha fazla öğrenci (Student) , en az 1 veya daha fazla ders (Subject) alabilir.
- En az 1 veya daha fazla dersin (Subject), en az 1 veya daha fazla öğretmeni (Instructor) olabilir.
- Bir departmanın (Department) en az 1 veya daha fazla dersi (Subject) olabilir.
- Bir veya daha fazla departmana (Department), 1 veya daha fazla öğretmen (Instructor) atanabilir.

## Sipariş Yönetim Sistemi Sınıf Tasarımı

![Ekran görüntüsü 2022-02-19 202816](https://user-images.githubusercontent.com/89224500/154811877-6183e544-0cdc-48ce-a14a-09e8da1e6b68.png)

- Bir müşterinin 0 veya daha fazla siparişi olabilir.
- Bir siparişe ait sipariş detayı ve ürünleri olur.
- 1 siparişin birden fazla ödemesi olabilir.
- Nakit , Çek ve Kredi Kartı ödeme yöntemleridir.



