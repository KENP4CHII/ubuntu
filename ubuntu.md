```
asfşkajsfklşajsfasfşasf
```


## TEMEL LİNUX KOMUTLARI ÇALIŞMA SORULARI


# Dosya ve Dizin İşlemleri: 
   
##	Bir dizin oluşturun ve içine birkaç dosya ekleyin. Ardından bu dosyaları listeleyin ve silin. 

```bash
mkdir ornek_dizin
cd ornek_dizin
touch dosya1.txt dosya2.txt dosya3.txt
ls
rm dosya1.txt dosya2.txt dosya3.txt
```

## Dosya izinlerini (chmod) değiştirerek bir dosyayı okunabilir, yazılabilir ve çalıştırılabilir hale getirin. 

```bash
chmod +rwx dosya_adı
```

## Belirli bir dizindeki dosya ve alt dizinlerin sayısını ve boyutunu hesaplayın. 


## cp, mv ve rm komutlarını kullanarak bir dosyayı kopyalayın, taşıyın ve silin. 

```bash
cp kaynak_dosya hedef_dosya
cp dosya.txt dosya_kopya.txt
mv kaynak_dosya hedef_dizin
mv dosya_kopya.txt yeni_dizin/
rm dosya
rm dosya_kopya.txt
```

## touch komutuyla yeni bir dosya oluşturun ve bu dosyanın içeriğini echo kullanarak düzenleyin.

```bash
“touch yeni_dosya.txt
echo "Bu dosyanın içeriğidir." > yeni_dosya.txt
cat yeni_dosya.txt	
```

# Arama ve Filtreleme: 


##	grep komutunu kullanarak bir metin dosyasında belirli bir kelimeyi arayın.

``` bash
grep "aramak_istediğiniz_kelime" dosya.txt
```
##	find komutunu kullanarak belirli bir dizin altında bir dosya arayın. 

```bash
find /path/to/dizin -type f -name "aranan_dosya.txt"
```

## grep ve sed komutlarını kullanarak bir metin dosyasındaki belirli bir deseni değiştirin. 

```bash
sed 's/eski_desen/yeni_desen/g' metin_dosyasi.txt > gecici_dosya.txt && mv gecici_dosya.txt metin_dosyasi.txt
```

## grep ve wc komutlarını kullanarak belirli bir metin dosyasındaki satır sayısını bulun. 

```bash
grep -c '' metin_dosyasi.txt
wc -l metin_dosyasi.txt
```	

## Bir dizindeki dosyaları isim veya uzantılarına göre filtreleyin ve listesini alın.

```bash
ls /path/to/dizin/belirli_bir_isim*
ls /path/to/dizin/*.txt
```

# Sistem Bilgileri ve Yönetimi: 

## Sistemdeki disk alanının ne kadarının kullanıldığını kontrol edin. 

```bash
df -h
```

## top veya htop komutunu kullanarak sistemde çalışan işlemleri ve kaynak kullanımını izleyin.


##	ps komutunu kullanarak belirli bir kullanıcıya ait işlemleri listeleyin. 

```bash
ps -u kullanici_adi
ps -ef | grep kullanici_adi
```

## df ve du komutlarını kullanarak disk bölümlerini ve dosya/dizin boyutlarını görüntüleyin. 

## uname komutunu kullanarak sisteminizin hangi çekirdek sürümünü kullandığınızı belirleyin.


# Ağ İşlemleri:


 ## ping komutunu kullanarak bir web sitesine erişilebilirliği kontrol edin. 


## ifconfig veya ip addr komutlarını kullanarak ağ arabirimlerini ve IP adreslerini görüntüleyin.


## netstat veya ss komutlarını kullanarak sistemde açık olan bağlantıları ve portları listeleyin. 

## nslookup veya dig komutlarını kullanarak bir alan adının IP adresini çözün. 

## curl veya wget komutlarını kullanarak belirli bir URL'den bir dosya indirin.


# Kullanıcı ve İzin Yönetimi: 


##	Bir kullanıcı oluşturun ve bu kullanıcıya ait temel bilgileri ve izinleri görüntüleyin. 

```bash
sudo adduser yeni_kullanici_adı
 id yeni_kullanici_adı
```

##	Bir kullanıcının parolasını (passwd) değiştirin. 

```bash
sudo passwd parola
```

## sudo komutunu kullanarak bir kullanıcıya yönetici (root) yetkileri verin. 

```bash
sudo adduser kullanici_adi sudo
sudo -l -U kullanici_adi
```

## chmod ve chown komutlarını kullanarak bir dosyanın izinlerini ve sahibini değiştirin. 

```bash
chmod 755 dosya.txt

sudo chown yeni_kullanici:dosya_grubu dosya.txt
```

##	/etc/sudoers dosyasını düzenleyerek belirli bir kullanıcının sudo yetkilerini özelleştirin.
```bash
sudo visudo

# Özelleştirilmiş sudo yetkileri
kullanici_adı   ALL=(ALL:ALL) /bin/ls
```
