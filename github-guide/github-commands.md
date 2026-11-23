# GitHub Guide — GitHub va Remote komandalar

**Muallif: Axmadov Ibratjon**

## Kirish
GitHub — Git repository’larini internetda saqlash, ulashish, ko‘rib chiqish va loyihalar ustida hamkorlik qilish platformasi. Git lokal kompyuterda versiyalarni boshqaradi, GitHub esa repository’ni onlayn saqlash va boshqalar bilan ulashishga yordam beradi.

## 1. GitHub nima?
GitHub — Git asosida ishlaydigan onlayn platforma. Unda loyihalarni repository ko‘rinishida saqlash, kodni ko‘rish va hamkorlik qilish mumkin.

**Vazifasi:** loyihani internetda saqlash va boshqalarga taqdim etish.  
 `https://github.com/` saytiga kirib hisob yaratish.

## 2. Git va GitHub farqi
- **Git** — versiya nazorati tizimi; kompyuterda lokal ishlashi mumkin.
- **GitHub** — Git repository’larini onlayn saqlash va boshqarish xizmati.

Git commitlarni yaratadi va tarixni boshqaradi. GitHub esa repository’ni internet orqali ko‘rish, ulashish va hamkorlikni tashkil etishga yordam beradi.

## 3. GitHub account nima?
GitHub account — foydalanuvchining GitHub’dagi shaxsiy hisobidir. Hisob orqali repository yaratish, loyihalarni saqlash va platforma imkoniyatlaridan foydalanish mumkin.

**Qachon kerak:** o‘z loyihangizni GitHub’ga joylash yoki boshqa loyihalarni kuzatish uchun.  
**Eslatma:** parolni hech kimga bermang va ikki bosqichli himoyadan foydalanish tavsiya etiladi.

## 4. Repository nima?
GitHub repository — loyiha fayllari, commitlar, branchlar va loyiha haqidagi ma’lumotlar saqlanadigan masofaviy ombor.

Repository ichida kod, README, hujjatlar va boshqa kerakli fayllar bo‘lishi mumkin.

## 5. Public va Private repository farqi
- **Public repository** internetdagi hammaga ko‘rinadi.
- **Private repository** faqat egasi va ruxsat berilgan foydalanuvchilarga ko‘rinadi.

Ochiq ko‘rsatish kerak bo‘lgan maktab loyihasi uchun o‘qituvchi talabiga qarab Public tanlanishi mumkin. Maxfiy ma’lumotlarni hech qachon repository’ga joylamang.

## 6. Remote nima?
Remote — lokal Git repository bilan bog‘langan masofaviy repository manzili. Ko‘pincha GitHub’dagi repository remote sifatida ulanadi. `origin` odatda asosiy remote uchun ishlatiladigan nom.

## 7. `git remote add`
Mavjud lokal repository’ga remote manzil qo‘shadi.

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```
`USERNAME` va `REPOSITORY` o‘rniga o‘z GitHub username’ingiz va repository nomingizni yozing. Bu buyruq odatda repository’ni birinchi marta GitHub bilan ulashda ishlatiladi.

## 8. `git remote -v`
Ulangan remote repository’larning fetch va push manzillarini ko‘rsatadi.

```bash
git remote -v
```
Agar `origin` ko‘rinsa, remote manzil ulangan. Fetch — ma’lumotni olib kelish, push — commitlarni yuborish uchun ishlatiladi.

## 9. `git push`
`git push` lokal commitlarni remote repository’ga yuboradi.

```bash
git push -u origin main
git push -u origin github-guide
```
`-u` upstream bog‘lanishni o‘rnatadi. Keyingi safar ayrim holatlarda oddiy `git push` yozish kifoya bo‘ladi.

## 10. `git pull`
`git pull` remote repository’dagi yangilanishlarni olib keladi va joriy branchga birlashtiradi.

```bash
git pull origin main
```
**Qachon ishlatiladi:** GitHub’dagi yangi o‘zgarishlarni lokal kompyuterga olish kerak bo‘lganda. Ishni boshlashdan oldin kerakli branchda ekaningizni tekshiring.

## 11. `git clone`
`git clone` masofaviy repository’ning nusxasini kompyuterga yuklab, lokal Git repository yaratadi.

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```
Bu buyruq mavjud loyihani kompyuterga olish uchun ishlatiladi. Klonlashdan keyin yaratilgan papkaga `cd` orqali kiring.

## 12. GitHub’da branch nima?
GitHub’dagi branch — repository ichidagi alohida ish yo‘nalishi. U `main` branchni darhol o‘zgartirmasdan vazifa bajarishga yordam beradi. Branchlar sahifasida mavjud yo‘nalishlarni ko‘rish mumkin.

## 13. GitHub’da commit nima?
Commit — repository tarixidagi saqlangan o‘zgarishlar to‘plami. GitHub’da commit xabari, muallifi va o‘zgarishlar tafsilotini ko‘rish mumkin.

Yaxshi commit xabari qisqa va mazmunli bo‘ladi, masalan: `Add terminal guide`.

## 14. GitHub’da faylni tahrirlash
Repository ichida kerakli faylni ochib, **Edit** tugmasi orqali matnni o‘zgartirish mumkin. So‘ng **Commit changes** orqali o‘zgarish saqlanadi.

**Tartib:**
1. GitHub’da repository’ni oching.
2. Tahrir qilinadigan faylni tanlang.
3. Edit belgisini bosing.
4. Matnni o‘zgartiring.
5. Commit xabarini yozib, o‘zgarishni saqlang.

O‘zgarish qaysi branchga kiritilayotganini tekshiring.

## 15. GitHub’da branchni o‘chirish
Repository’ning **Branches** sahifasida branchni o‘chirish mumkin. Terminaldan remote branchni o‘chirish komandasi:

```bash
git push origin --delete branch-name
```
Odatda ish merge qilingandan keyin branch o‘chiriladi. Ushbu topshiriqda branchlarni o‘chirmang.

## GitHub’da yangi repository yaratish — 5 bosqich
1. GitHub hisobingizga kiring.
2. Yuqoridagi **+** menyusidan **New repository** ni tanlang.
3. Repository nomini `git-github-master-guide` deb kiriting.
4. O‘qituvchi talabiga ko‘ra Public yoki Private tanlang.
5. **Create repository** tugmasini bosing.

Agar lokal papkada README va `.gitignore` allaqachon yaratilgan bo‘lsa, GitHub’da repository ochayotganda README, `.gitignore` yoki license faylini avtomatik yaratish kataklarini belgilamang.

## Lokal loyihani GitHub’ga ulash
```bash
git remote add origin https://github.com/USERNAME/git-github-master-guide.git
git remote -v
git branch -M main
git push -u origin main
```
Repository manzilini o‘zingiznikiga almashtiring.

## Savol-javoblar
**1. GitHub nima?**  
Git repository’larini internetda saqlash va ulashish platformasi.

**2. Git va GitHub bir xilmi?**  
Yo‘q. Git versiyalarni boshqaradi, GitHub esa repository’larni onlayn saqlash xizmatidir.

**3. Public repository kimlarga ko‘rinadi?**  
Internetdagi barcha foydalanuvchilarga.

**4. Private repository kimlarga ko‘rinadi?**  
Egasi va ruxsat berilgan foydalanuvchilarga.

**5. `git push` nima qiladi?**  
Lokal commitlarni remote repository’ga yuboradi.

**6. `git pull` nima qiladi?**  
Remote’dagi yangilanishlarni olib kelib, joriy branchga birlashtiradi.

**7. `git clone` nima uchun kerak?**  
Masofaviy repository nusxasini kompyuterga yuklab olish uchun.

## Xulosa
GitHub loyihalarni internetda saqlash va boshqalar bilan ulashish imkonini beradi. `remote`, `push`, `pull` va `clone` komandalarini bilish lokal Git bilan GitHub o‘rtasida ishlash uchun muhim.

## Foydali maslahatlar
GitHub loyihalarni internetda saqlash, boshqalar bilan ulashish va jamoaviy ishlash imkonini beradi.