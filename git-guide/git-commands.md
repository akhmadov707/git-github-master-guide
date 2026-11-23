# Git Guide — Git asoslari va Git komandalar

**Muallif: Axmadov Ibratjon**

## Kirish
Git — fayllardagi o‘zgarishlarni kuzatish va loyiha versiyalarini boshqarish uchun ishlatiladigan taqsimlangan versiya nazorati tizimi. Git yordamida loyiha tarixini saqlash, oldingi holatlarni ko‘rish va alohida branchlarda ishlash mumkin.

## 1. Git nima?
Git — dasturiy loyihadagi fayllar o‘zgarishini qayd etib boradigan versiya nazorati tizimi. U kompyuterda lokal ishlaydi va internet bo‘lmasa ham commit yaratish mumkin.

**Vazifasi:** loyiha tarixini saqlash va o‘zgarishlarni boshqarish.  
**Qachon ishlatiladi:** yangi loyiha boshlaganda yoki mavjud loyihadagi ishlarni kuzatishda.  

```bash
git --version
```
Bu buyruq o‘rnatilgan Git versiyasini ko‘rsatadi.

## 2. Git nima uchun kerak?
Git loyiha fayllaridagi o‘zgarishlar tarixini saqlaydi. Xato yuz bersa, oldingi commitlarni ko‘rish mumkin. Branchlar orqali yangi funksiyalarni asosiy ishga ta’sir qilmasdan tayyorlash mumkin.

**Asosiy imkoniyatlari:**
- o‘zgarishlar tarixini saqlash;
- oldingi versiyalarni ko‘rish;
- xatolarni aniqlash;
- branchlarda mustaqil ishlash;
- jamoa bilan hamkorlik qilish.


```bash
git log --oneline
```
Buyruq commitlar tarixini qisqa ko‘rinishda chiqaradi.

## 3. Repository nima?
Repository — loyiha fayllari va Git tarixi saqlanadigan joy. Lokal repository kompyuterda, remote repository esa GitHub kabi serverda bo‘lishi mumkin.

**Vazifasi:** fayllar va ularning o‘zgarish tarixini bir joyda saqlash.  

```bash
mkdir mening-loyiham
cd mening-loyiham
git init
```
Natijada joriy papkada yangi lokal repository boshlanadi.

## 4. Global va Local konfiguratsiya farqi
Git konfiguratsiyasi commit muallifining ismi va emailini belgilaydi.

- **Global** sozlama odatda foydalanuvchining barcha repository’lariga tatbiq etiladi.
- **Local** sozlama faqat joriy repository uchun amal qiladi.
- Local qiymat mavjud bo‘lsa, shu repository’da global qiymatdan ustun turadi.

**Global sozlash:**
```bash
git config --global user.name "Ism Familiya"
git config --global user.email "email@example.com"
```
**Joriy repository uchun sozlash:**
```bash
git config user.name "Ism Familiya"
git config user.email "email@example.com"
```
**Tekshirish:**
```bash
git config --global user.name
git config --global user.email
git config --list
```
Haqiqiy email yoki o‘qituvchi tavsiya qilgan emaildan foydalaning.

## 5. `git init`
`git init` joriy papkada yangi Git repository yaratadi. Bu buyruq loyiha fayllarini Git yordamida kuzatishni boshlash uchun ishlatiladi.

```bash
mkdir yangi-loyiha
cd yangi-loyiha
git init
```
Natijada papkada Git boshqaruv ma’lumotlari yaratiladi. Buyruqni loyiha papkasida bir marta bajarish yetarli.

## 6. `git status`
`git status` repository holatini ko‘rsatadi. U yangi, o‘zgargan, staging area’ga qo‘shilgan va commit qilinmagan fayllarni aniqlashga yordam beradi.

```bash
git status
```
**Qachon ishlatiladi:** fayllarni tahrirlashdan keyin, `git add` dan oldin va commitdan oldin.

## 7. `git add`
`git add` tanlangan fayllardagi o‘zgarishlarni staging area’ga qo‘shadi. Staging area — keyingi commitga kiritiladigan o‘zgarishlar tayyorlanadigan bosqich.

```bash
git add README.md
git add .
```
Birinchi buyruq faqat `README.md` faylini, ikkinchisi joriy papkadagi kuzatiladigan o‘zgarishlarni qo‘shadi. Commit qilishdan oldin `git status` bilan tekshiring.

## 8. `git commit`
`git commit` staging area’dagi o‘zgarishlarni repository tarixida yangi commit sifatida saqlaydi. Commit xabari bajarilgan ishni qisqa va aniq ifodalashi kerak.

```bash
git add README.md
git commit -m "Add project description"
```
**Qachon ishlatiladi:** ma’lum bir ish qismi tugab, uni tarixda saqlashga tayyor bo‘lganda.

## 9. `git log`
`git log` repository’dagi commitlar tarixini ko‘rsatadi. Unda commit muallifi, sana va xabar ko‘rinadi.

```bash
git log
git log --oneline
```
Birinchi buyruq batafsil tarixni, ikkinchisi esa qisqa ro‘yxatni ko‘rsatadi. Bu buyruq qaysi ishlar saqlanganini tekshirishda foydali.

## 10. `git branch`
Branch — repository ichidagi alohida ish yo‘nalishi. `git branch` branchlarni ko‘rsatadi yoki yangi branch yaratadi.

```bash
git branch
git branch yangi-vazifa
```
Yulduzcha (`*`) hozir qaysi branchda turganingizni bildiradi. Ikkinchi buyruq yangi branch yaratadi, lekin unga o‘tmaydi.

## 11. `git switch`
`git switch` mavjud branchga o‘tadi. `-c` parametri yangi branch yaratib, unga bir vaqtda o‘tish imkonini beradi.

```bash
git switch main
git switch -c yangi-vazifa
```
**Qachon ishlatiladi:** boshqa vazifaga o‘tishda yoki yangi ish yo‘nalishini boshlashda.

## 12. `git merge`
`git merge` boshqa branchdagi o‘zgarishlarni joriy branchga birlashtiradi. Avval natija qaysi branchga qo‘shilishini tanlab, o‘sha branchga o‘tiladi.

```bash
git switch main
git merge yangi-vazifa
```
ushbu maktab topshirig‘ida o‘quvchi merge bajarmaydi. Bu jarayon keyingi darsda o‘qituvchi tomonidan ko‘rsatiladi.

## 13. `git branch -d`
`git branch -d` lokal branchni o‘chiradi. Odatda ishi tugagan va birlashtirilgan branchni tozalash uchun ishlatiladi.

```bash
git switch main
git branch -d yangi-vazifa
```
Git birlashtirilmagan ish bo‘lsa ogohlantirishi mumkin. Ushbu loyiha davomida branchlarni o‘chirmang.

## Git bilan ishlashning odatiy ketma-ketligi
```bash
git status
git add README.md
git status
git commit -m "Update README"
git log --oneline
```
Bu ketma-ketlik holatni tekshirish, faylni stagingga qo‘shish va commit yaratishni ko‘rsatadi.

## Savol-javoblar
**1. Git nima?**  
Git — fayllardagi o‘zgarishlarni kuzatadigan versiya nazorati tizimi.

**2. Repository nima?**  
Repository — loyiha fayllari va ularning Git tarixini saqlaydigan joy.

**3. `git add` nima qiladi?**  
O‘zgarishlarni keyingi commit uchun staging area’ga qo‘shadi.

**4. `git commit` nima qiladi?**  
Tayyorlangan o‘zgarishlarni repository tarixida saqlaydi.

**5. Branch nima uchun kerak?**  
Asosiy branchga darhol ta’sir qilmasdan alohida vazifada ishlash uchun.

**6. `git status` nimani ko‘rsatadi?**  
Repository’dagi fayllarning joriy holatini ko‘rsatadi.

**7. Global va local sozlamaning farqi nima?**  
Global barcha loyihalar uchun, local esa faqat joriy repository uchun amal qiladi.

## Xulosa
Git loyiha tarixini tartibli saqlashga yordam beradi. `init`, `status`, `add`, `commit`, `log`, `branch` va `switch` buyruqlari kundalik ishda ko‘p ishlatiladi. Har bir commitdan oldin o‘zgarishlarni tekshirish yaxshi odat hisoblanadi.