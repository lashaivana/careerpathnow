# CareerPathNow - Team Project

## 📁 პროექტის სტრუქტურა

```
careerpathnow/
├── index.html
├── css/
│   └── main.css          ← (SCSS-დან კომპილირებული, commit არ ვაკეთებთ)
├── scss/
│   ├── main.scss          ← მთავარი ფაილი (import-ები)
│   ├── utils/
│   │   ├── _variables.scss   ← ფერები, font-ები, spacing
│   │   └── _mixins.scss      ← responsive & helpers
│   ├── base/
│   │   └── _reset.scss       ← CSS reset
│   ├── components/
│   │   └── _buttons.scss     ← shared buttons
│   └── sections/
│       ├── _navbar.scss      ← კაცი 1
│       ├── _hero.scss        ← კაცი 1
│       ├── _about.scss       ← კაცი 2
│       ├── _services.scss    ← კაცი 2
│       ├── _reviews-contact.scss  ← კაცი 3
│       └── _footer.scss      ← კაცი 3
└── README.md
```

---

## 👥 გუნდის დაყოფა

| კაცი | ფაილები | სექციები |
|------|---------|----------|
| **კაცი 1** | `_navbar.scss`, `_hero.scss` | Navbar + Hero |
| **კაცი 2** | `_about.scss`, `_services.scss` | About Us + Services + Stories |
| **კაცი 3** | `_reviews-contact.scss`, `_footer.scss` | Reviews + Contact + Footer |

---

## 🚀 SCSS კომპილაცია

```bash
# Node.js-ით (sass package)
npm install -g sass
sass --watch scss/main.scss:css/main.css

# ან dart sass-ით
sass scss/main.scss css/main.css
```

---

## 🌿 GitHub Workflow

### პირველ რიგში:
```bash
git clone https://github.com/yourteam/careerpathnow.git
cd careerpathnow
```

### ყოველი კაცი თავის branch-ზე მუშაობს:
```bash
# კაცი 1
git checkout -b feature/navbar-hero

# კაცი 2
git checkout -b feature/about-services

# კაცი 3
git checkout -b feature/reviews-footer
```

### Commit & Push:
```bash
git add .
git commit -m "feat: navbar responsive mobile menu added"
git push origin feature/navbar-hero
```

### Pull Request:
1. GitHub-ზე "New Pull Request" 
2. `feature/navbar-hero` → `main` branch-ში
3. გუნდელი review-ს გაუკეთებს
4. Merge!

---

## ⚠️ Merge Conflicts თავიდან აცილება

- ყოველი კაცი **მხოლოდ თავის** SCSS ფაილებს ეხება
- `_variables.scss` და `_mixins.scss` — **ყველა კითხულობს, არავინ ცვლის** შეთანხმების გარეშე
- `index.html` — ყოველი კაცი თავის section-ს ამატებს, pull before push!

---

## 🎨 Color Palette

| Variable | Value | გამოყენება |
|----------|-------|------------|
| `$color-dark` | `#1a2332` | main background |
| `$color-yellow` | `#e8c840` | accents, highlights |
| `$color-white` | `#ffffff` | text on dark bg |
| `$color-yellow-bg` | `#f0d060` | section backgrounds |

## 📱 Breakpoints

| Mixin | Breakpoint |
|-------|-----------|
| `@include mobile` | < 768px |
| `@include tablet` | 768px - 1023px |
| `@include desktop` | ≥ 1024px |
