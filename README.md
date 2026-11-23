# Git & GitHub Master Guide

Bu loyiha Git, GitHub va Terminal komandalarini o‘rganish, ularni amalda bajarish va natijalarni hujjatlashtirish uchun yaratildi.

## Muallif
Axmadov Ibratjon

## Loyiha maqsadi
Git orqali loyiha tarixini boshqarish, GitHub’da repository saqlash va Terminal yordamida fayl hamda papkalar bilan ishlash ko‘nikmalarini mustahkamlash.

## Loyiha logotiplari

![Git logotipi](images/git.png)

![GitHub logotipi](images/github.png)

## Loyiha bo‘limlari
- **Git Guide** — Git asoslari va asosiy komandalar.
- **GitHub Guide** — GitHub, remote repository va onlayn hamkorlik.
- **Terminal Guide** — terminal buyruqlari va fayl tizimi bilan ishlash.

## Papkalar tuzilishi
```text
git-github-master-guide/
├── README.md
├── .gitignore
├── git-guide/
│   └── git-commands.md
├── github-guide/
│   └── github-commands.md
├── terminal-guide/
│   └── terminal-commands.md
├── images/
│   ├── github.png
│   └── git.png
└── resources/
    └── useful-links.md
```

## Ishlash tartibi
1. `main` branchda asosiy fayllar yaratiladi.
2. `git-guide`, `github-guide` va `terminal-guide` branchlari `main` dan alohida yaratiladi.
3. Har bir branchda faqat o‘z mavzusiga tegishli Markdown qo‘llanma yoziladi.
4. Har bir branchda kamida ikkita mazmunli commit yaratiladi.
5. Uchala branch GitHub’ga alohida push qilinadi.


## Muallif ma’lumoti
Muallif: **Axmadov Ibratjon**. GitHub username va repository manzilini o‘zingiznikiga almashtiring. Parol yoki tokenni README yoki boshqa fayllarga yozmang.
## `.gitignore` ni tekshirish

`private-notes.txt` fayli loyiha ichida faqat `.gitignore` ishlashini tekshirish uchun turadi. Undagi login va parollar to‘liq soxta. Bu fayl GitHub’ga yuborilmaydi. `git status --ignored` buyrug‘i bilan `private-notes.txt` ignored holatida ekanini tekshiring.

## GitHub’ga topshirish bo‘yicha aniq tartib

Quyidagi buyruqlarda `USERNAME` o‘rniga GitHub username’ingizni yozing. GitHub’da avval `git-github-master-guide` nomli bo‘sh repository yarating. Agar lokalda README mavjud bo‘lsa, GitHub’da README yaratish katagini belgilamang.

### 1. Main branchni tayyorlash
Avval uchta qo‘llanma papkasini vaqtincha loyiha papkasidan tashqariga olib chiqing. Git Bash’da loyiha papkasi ichida quyidagilarni bajaring:
```bash
mkdir ../guides-temp
mv git-guide github-guide terminal-guide ../guides-temp/
git init
git branch -M main
git add README.md .gitignore images resources
git commit -m "Create main project structure"
git remote add origin https://github.com/USERNAME/git-github-master-guide.git
git push -u origin main
git status --ignored
```
`private-notes.txt` `.gitignore` sababli GitHub’ga yuborilmaydi. Uni `git add` bilan majburan qo‘shmang.

### 2. Git Guide branch
```bash
git switch main
git switch -c git-guide
mv ../guides-temp/git-guide .
git add git-guide/git-commands.md
git commit -m "Add Git guide first draft"
```
Endi `git-guide/git-commands.md` fayliga kichik qo‘shimcha yoki tahrir kiriting, so‘ng ikkinchi commit yarating:
```bash
git add git-guide/git-commands.md
git commit -m "Complete Git guide explanations"
git push -u origin git-guide
```

### 3. GitHub Guide branch
```bash
git switch main
git switch -c github-guide
mv ../guides-temp/github-guide .
git add github-guide/github-commands.md
git commit -m "Add GitHub guide first draft"
```
Faylga qo‘shimcha yoki tahrir kiriting, so‘ng:
```bash
git add github-guide/github-commands.md
git commit -m "Complete GitHub guide explanations"
git push -u origin github-guide
```

### 4. Terminal Guide branch
```bash
git switch main
git switch -c terminal-guide
mv ../guides-temp/terminal-guide .
git add terminal-guide/terminal-commands.md
git commit -m "Add Terminal guide first draft"
```
Faylga qo‘shimcha yoki tahrir kiriting, so‘ng:
```bash
git add terminal-guide/terminal-commands.md
git commit -m "Complete Terminal guide explanations"
git push -u origin terminal-guide
```

### 5. Yakuniy tekshiruv
```bash
git branch -a
git log --oneline --all
git status
```
GitHub repository sahifasida `main`, `git-guide`, `github-guide` va `terminal-guide` branchlari borligini tekshiring.

bu topshiriqda branchlarni merge qilmang va o‘chirmang. Har bir mavzuli branchni `main` dan yarating. Har bir branchda kamida ikkita mazmunli commit bo‘lishi kerak.
