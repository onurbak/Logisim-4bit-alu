# 4-Bit ALU (Aritmetik Mantık Birimi) Tasarımı

Bu depo, **Logisim-evolution** kullanılarak tasarlanmış 4 bitlik bir Aritmetik Mantık Birimini (ALU) içerir. Devre, iki adet 4 bitlik girişi (A ve B) alır ve seçilen fonksiyona (FS) göre aritmetik veya mantıksal işlemler gerçekleştirir.


## Özellikler

* **4-Bit Mimari:** 4 bitlik veri yolları üzerinde işlem yapar.
* **Çoklu İşlevsellik:** 3 bitlik Fonksiyon Seçici (FS) girişi sayesinde 8 farklı işlem tanımlanabilir.
* **Taşma Göstergesi:** İşlem sonucunda oluşan eldeyi (Carry Out) gösteren `cout` çıkışı bulunur.
* **Modüler Tasarım:** Logisim-evolution v4.0.0 ile uyumludur.

## Kullanılan Teknolojiler

* **Yazılım:** [Logisim-evolution v4.0.0](https://github.com/logisim-evolution/logisim-evolution)
* **Bileşenler:** MUX (Multiplexer), Mantık Kapıları, Toplayıcılar.

## Pin Açıklamaları

| Pin Adı | Tür | Bit Boyutu | Açıklama |
| :--- | :--- | :--- | :--- |
| **A** | Giriş | 4-bit | Birinci işlenen sayı. |
| **B** | Giriş | 4-bit | İkinci işlenen sayı. |
| **FS** | Giriş | 3-bit | Yapılacak işlemi seçer (Function Select). |
| **RESULT**| Çıkış | 4-bit | İşlem sonucu. |   
| **cout** | Çıkış | 1-bit | Elde (Carry out) çıkışı. |

## İşlem Tablosu 

*FS (Function Select) girişine göre yapılan işlemler:*

| FS (Binary) | FS (Decimal) | İşlem | Açıklama |
| :---: | :---: | :--- | :--- |
| 000 | 0 | **AND** | A ve B mantıksal VE işlemi (Örnek) |
| 001 | 1 | **OR** | A ve B mantıksal VEYA işlemi (Örnek) |
| 010 | 2 | **ADD** | A + B Toplama İşlemi (Örnek) |
| 011 | 3 | **SUB** | A - B Çıkarma İşlemi (Örnek) |
| ... | ... | ... | ... |
