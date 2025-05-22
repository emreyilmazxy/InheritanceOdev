# 👨‍🏫 C# Kalıtım (Inheritance) Ödevi - Özet

## 📌 Amaç:
Base (Temel) bir sınıftan miras alan sınıflar oluşturarak, kalıtım mantığını uygulamalı olarak öğrenmek.

---

## 🧱 Sınıf Yapısı

### ✅ BaseKisi (Temel Sınıf)
**Propertyler:**
- `Ad` (string)
- `Soyad` (string)

**Metot:**
- `Yazdir()` → Ad ve Soyad’ı konsola yazdırır.

---

### 👨‍🎓 Ogrenci (BaseKisi’den türetilmiş sınıf)
**Ek Property:**
- `OgrenciNo` (int)

**Metot:**
- `OgrenciBilgileri()` → Önce `Yazdir()` metodu çağrılır, ardından öğrenci numarası yazdırılır.

---

### 👩‍🏫 Ogretmen (BaseKisi’den türetilmiş sınıf)
**Ek Property:**
- `Maas` (int)

**Metot:**
- `OgretmenBilgileri()` → Önce `Yazdir()` metodu çağrılır, ardından maaş bilgisi yazdırılır.

---

## 💡 Not:
> Sınıflar arası kod tekrarını önlemek için, `Ogretmen` ve `Ogrenci` sınıflarındaki metotlarda `BaseKisi` sınıfının `Yazdir()` metodu kullanılmıştır.  
> Bu, "Bir metot içinde başka bir metot çağırabilirsiniz" uyarısına örnektir.

---

## 🧪 Test / Main Metodu
- Bir `Ogrenci` ve bir `Ogretmen` nesnesi oluşturulmuş, değerleri atanmış ve bilgiler konsola yazdırılmıştır.

```csharp
Ogrenci ogrenci = new Ogrenci();
ogrenci.Ad = "Ali";
ogrenci.Soyad = "Veli";
ogrenci.OgrenciNo = 123;
ogrenci.OgrenciBilgileri();

Ogretmen ogretmen = new Ogretmen();
ogretmen.Ad = "Ayşe";
ogretmen.Soyad = "Yılmaz";
ogretmen.Maas = 5000;
ogretmen.OgretmenBilgileri();
