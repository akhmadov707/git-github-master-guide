# Terminal Guide — Terminal komandalar

**Muallif: Axmadov Ibratjon**

## Kirish
Terminal — kompyuter bilan matnli buyruqlar orqali muloqot qilish imkonini beradigan dastur yoki interfeys. Terminal yordamida papka va fayllarni boshqarish, dasturlarni ishga tushirish hamda Git komandalarini bajarish mumkin.

## 1. Terminal nima?
Terminal foydalanuvchiga buyruqlar yozish orqali operatsion tizim bilan ishlash imkonini beradi. Windows’da Windows Terminal, PowerShell yoki Git Bash’dan foydalanish mumkin.

**Vazifasi:** grafik menyular o‘rniga buyruqlar orqali ish bajarish.

## 2. Terminal nima uchun kerak?
Terminal quyidagi vazifalar uchun ishlatiladi:
- fayl va papkalarni yaratish va ko‘rish;
- papkalar orasida yurish;
- dasturlarni ishga tushirish;
- Git buyruqlarini bajarish;
- tizim bilan tez ishlash.

## 3. `pwd` — joriy joylashuvni ko‘rish
`pwd` terminal ayni paytda qaysi papkada turganini to‘liq manzili bilan ko‘rsatadi.

```bash
pwd
```
**Qachon ishlatiladi:** buyruqlarni qaysi papkada bajarayotganingizni tekshirish uchun.

## 4. `ls` — fayllarni ko‘rish
`ls` joriy papkadagi fayl va papkalar ro‘yxatini ko‘rsatadi.

```bash
ls
ls -la
```
Birinchi buyruq oddiy ro‘yxatni, ikkinchisi yashirin fayllarni ham ko‘rsatishi mumkin. Windows PowerShell’da `ls` alias sifatida ishlaydi.

## 5. `cd` — papkaga kirish
`cd` ko‘rsatilgan papkaga o‘tadi.

```bash
cd documents
cd git-github-master-guide
```
**Qachon ishlatiladi:** kerakli loyiha papkasiga kirish uchun. Papka nomi to‘g‘ri yozilgan bo‘lishi kerak.

## 6. `cd ..` — yuqori papkaga chiqish
`cd ..` joriy papkaning bitta yuqori darajasiga qaytadi.

```bash
cd ..
```
**Qachon ishlatiladi:** ichki papkadan uning ota papkasiga qaytish kerak bo‘lganda.

## 7. `mkdir` — papka yaratish
`mkdir` yangi papka yaratadi.

```bash
mkdir my-folder
mkdir images resources
```
Ikkinchi buyruq ikkita papka yaratadi. Papka nomini keyinchalik `cd` bilan ochish mumkin.

## 8. `touch` — fayl yaratish
Git Bash, macOS va Linux’da `touch` yangi bo‘sh fayl yaratadi yoki mavjud faylning vaqt belgisini yangilaydi.

```bash
touch notes.txt
touch README.md
```
Windows PowerShell’da muqobil ko‘rinish:
```powershell
New-Item notes.txt -ItemType File
```

## 9. `cat` — fayl mazmunini ko‘rish
`cat` matnli fayl ichidagi yozuvlarni terminalda chiqaradi.

```bash
cat notes.txt
cat README.md
```
**Qachon ishlatiladi:** faylni matn muharririsiz tez ko‘rib chiqish uchun. Katta fayllarda natija uzun bo‘lishi mumkin.

## 10. `clear` — terminalni tozalash
`clear` terminal oynasidagi avvalgi matnlarni ekrandan tozalaydi. U fayllarni o‘chirmaydi.

```bash
clear
```
Windows PowerShell’da `cls` ham ishlatiladi.

## 11. `cp` — nusxa olish
`cp` fayl yoki papkadan nusxa yaratadi.

```bash
cp notes.txt notes-copy.txt
```
`notes.txt` faylining `notes-copy.txt` nomli nusxasi yaratiladi. Nusxa olishdan oldin manba fayl mavjudligini tekshiring.

## 12. `mv` — ko‘chirish yoki nomini o‘zgartirish
`mv` fayl yoki papkani boshqa joyga ko‘chiradi yoki nomini o‘zgartiradi.

```bash
mv old.txt new.txt
mv notes.txt documents/
```
Birinchi buyruq fayl nomini o‘zgartiradi, ikkinchisi faylni boshqa papkaga ko‘chiradi.

## 13. `rm` — fayl o‘chirish
`rm` ko‘rsatilgan faylni o‘chiradi.

```bash
rm notes-copy.txt
```
**Xavfsizlik:** faqat o‘zingiz yaratgan sinov fayllarini o‘chiring. O‘chirishdan oldin fayl nomini tekshiring. Ushbu topshiriqda `rm -rf` kabi qaytarish qiyin bo‘lgan buyruqlardan foydalanmang.

## 14. `git init` — repository yaratish
`git init` joriy papkada yangi Git repository boshlaydi.

```bash
mkdir my-project
cd my-project
git init
```
Shundan so‘ng Git ushbu papkadagi o‘zgarishlarni kuzatishga tayyor bo‘ladi.

## 15. `git status` — Git holatini tekshirish
`git status` Git repository’dagi yangi, o‘zgargan va staging area’ga qo‘shilgan fayllar holatini ko‘rsatadi.

```bash
git status
```
**Qachon ishlatiladi:** fayllarni tahrirlashdan keyin, add va commitdan oldin.

## Amaliy mashq: papka va fayllar bilan ishlash
Quyidagi buyruqlarni Git Bash’da ketma-ket bajarib ko‘ring:

```bash
mkdir terminal-practice
cd terminal-practice
pwd
touch first.txt
ls
cat first.txt
cp first.txt first-copy.txt
ls
mv first-copy.txt second.txt
ls
rm second.txt
ls
cd ..
```

Mashqdan maqsad — papka yaratish, unga kirish, fayl yaratish, ro‘yxatni ko‘rish, nusxa olish, nomini o‘zgartirish va sinov faylini o‘chirishni o‘rganish.

## Git Bash va PowerShell haqida
Git Bash Unix uslubidagi ko‘plab buyruqlarni taqdim etadi. PowerShell esa Windows’ning buyruq qobig‘i hisoblanadi. Ayrim buyruqlar o‘xshash bo‘lsa-da, ba’zi parametrlar farq qilishi mumkin. Masalan, PowerShell’da fayl yaratish uchun `New-Item` ishlatiladi.

## Savol-javoblar
**1. Terminal nima?**  
Kompyuterga matnli buyruqlar kiritish uchun dastur yoki interfeys.

**2. `pwd` nima qiladi?**  
Joriy papkaning manzilini ko‘rsatadi.

**3. `ls` nima uchun kerak?**  
Joriy papkadagi fayl va papkalarni ko‘rsatadi.

**4. `cd ..` nima qiladi?**  
Bitta yuqori papkaga qaytadi.

**5. `mkdir` nima qiladi?**  
Yangi papka yaratadi.

**6. `touch` qayerda ishlaydi?**  
Git Bash, macOS va Linux’da bo‘sh fayl yaratish uchun ishlatiladi.

**7. `rm` bilan ishlaganda nimaga e’tibor berish kerak?**  
Faqat kerakli sinov faylini tanlash va nomini tekshirish kerak.

## Xulosa
Terminal buyruqlari kompyuterda fayl va papkalarni tez boshqarishga yordam beradi. Buyruqni kiritishdan oldin joriy joylashuvni `pwd` bilan tekshirish va xavfli buyruqlarni tushunmasdan bajarmaslik kerak.

## Xulosa
Terminal kompyuter bilan buyruqlar orqali ishlash, fayl va papkalarni boshqarish hamda Git buyruqlarini bajarish imkonini beradi.

## Foydali maslahatlar
Terminal buyruqlarini yozishda har bir belgiga e'tibor berish kerak. Buyruqlarni bajarishdan oldin ularni tekshirish tavsiya etiladi.