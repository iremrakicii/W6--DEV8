# Çalışan Veritabanı İşlemleri

Bu proje, `employee` tablosu üzerinde temel veri ekleme, güncelleme ve silme işlemlerini içerir. SQL dilinde yazılmış komutlarla çalışan kayıtlarını yönetmeyi hedeflemektedir.

## İçindekiler

1. [Tablo Yapısı](#tablo-yapısı)
2. [Güncelleme İşlemleri](#güncelleme-i̇şlemleri)
3. [Silme İşlemleri](#silme-i̇şlemleri)

### Tablo Yapısı

`employee` tablosu, aşağıdaki yapıya göre oluşturulmuştur:

```sql
CREATE TABLE employee(
    id INTEGER PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    birthday DATE,
    email VARCHAR(100)
);
```
id: Çalışan ID'si, birincil anahtar.
name: Çalışan adı, boş geçilemez.
birthday: Doğum tarihi.
email: Çalışan e-posta adresi.

### Güncelleme İşlemleri
Çalışanların bilgileri güncellenmiştir. Örnek olarak bazı çalışan kayıtları aşağıda verilmiştir:

```sql
UPDATE employee
SET name='Mary',
    email='maryko@gmail.com',
    birthday= '1950-07-17'
WHERE id=40;

UPDATE employee
SET name='Jane',
    email='janeemo@gmail.com',
    birthday= '1960-09-19'
WHERE id=15;
```
Bu işlemler ile id değeri belirli olan çalışanların adı, e-posta adresi ve doğum tarihi güncellenmiştir.

### Silme İşlemleri
Bazı çalışan kayıtları, çalışan id değerine göre silinmiştir:

```sql
DELETE FROM employee WHERE id BETWEEN 25 AND 30;
```
