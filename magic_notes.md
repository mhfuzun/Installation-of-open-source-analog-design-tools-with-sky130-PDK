## click:
sol tık: x0 y0 ile alt sol köşe taşınır, kare yeniden boyutlanmaz
sağ tık: karenin sağ üst köşesi hareket ettirilerek yeniden boyutlandırılır.

b: karenin boyutlarını ekrana yazar.
s: select (bir alan üzerinde iken), bir kaç defa batığında elektriksel tüm bağlantıları gösterir.
a: select all

## command:
grid 0.05um 0.05um      : grid ayarla
grid                    : grid kapat
snap user               : seçme karesi için min dimension ayarlar
drc style drc(full)     : drc'leri tamamen ekrana basar
drc why                 : drc hatasını gösterir
erease poly             : alan içindeki malzemeyi siler
select area             : kutu içindeki alanı seçer
copy                    : seçili alanı kopyalar
save inverter           : tasarımı kayıt eder.
extract all             : her şeyi extract eder

## extract alma:
ext2spice hierarchy on
ext2spice scale off
ext2spice cthresh infinite
ext2spice lvs
ext2spice

## Mosfet için:
### source-drain için:
m1
--------------
mcon (paint mcon = viali+m1)
--------------
locali (li)
--------------
ndiffcont (ndc)
--------------
ndif

### pwell için:
--------------
locali (li)
--------------
psubstratepcontact (psc)
--------------
psustratpdiffusion (psd)

### poly contact için:
poly extension'a ek yap (ek poly alan ekle)
locali ekle
poly contact (pc) ekle

locali (li)
--------------
poly contact (pc)
--------------
polysilicon (poly)

### mimcap:
m4
--------------
mimcapc
--------------
mimcap
--------------
m3

### port atama:
label A w (m1)
* w, e, n, s
* m1'da
port make 1
* 1, 2, 3, ..
