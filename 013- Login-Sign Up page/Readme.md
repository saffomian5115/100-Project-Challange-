# Student Portal (HTML/CSS)

🔗 **Live Link:** https://sarfraz-013-login-register.netlify.app/

---

## About

Ye Student Portal ka frontend hai, jo plain **HTML aur CSS** mein banaya gaya hai (koi framework ya React nahi). Isme teen pages hain:

- `login.html` — Login page
- `signup.html` — Sign Up page
- `dashboard.html` — Dashboard page (navbar ke sath)

Sab pages ek hi `style.css` file share karte hain.

---

## 🔐 Login Page UI

Login page ek **dark, glassy (frosted-glass) card** design follow karta hai jo background image ke upar center mein display hota hai.

**Components:**
- **Background:** Full-screen dark background image (`imgs/background.jpg`), jo blurred glass card ke peeche dikhta hai.
- **Navbar (top):** Sticky navbar jisme logo/title ("🌱 Sarfraz Pro-Dev") left side pe aur navigation links (Dashboard, Login, Sign Up) right side pe hain. Active link ke neeche underline animation hai.
- **Login Card:**
  - Center mein ek rounded card (`border-radius: 12px`), semi-transparent dark background (`rgba(17,24,39,0.5)`) aur `backdrop-blur` effect ke sath.
  - Card ka border halka grey hai, aur halki white glow shadow hai.
  - Heading: **"Login"** — bold, top par.
- **Input Fields (Email & Password):**
  - Floating label style — jaise hi user type kare ya field focus ho, label upar shift ho jata hai (smooth animation ke sath).
  - Har field ke right side pe ek matching icon hota hai (Email → envelope icon, Password → lock icon).
  - Fields ke neeche sirf ek bottom border hota hai (underline style), poora box nahi.
- **Extra Row:** "Remember Me" checkbox left side pe, aur "Forget Password" link right side pe (blue, underlined).
- **Login Button:** Full-width, solid blue button (`btn-primary`), hover par halka lighter blue ho jata hai.
- **Footer Text:** "Don't have Account? **Sign up**" — Sign up link blue aur underlined hai, jo `signup.html` ki taraf le jata hai.

**Color Theme:** Dark background + light gray text (`#f3f4f6`) + blue accents (`#1d4ed8` buttons, `#60a5fa` links) — overall ek modern, minimal, glassmorphism look.

---

## Files

```
.
├── login.html
├── signup.html
├── dashboard.html
├── style.css
└── imgs/
    └── background.jpg   (apni background image yahan rakhein)
```

## How to Run

Bas `login.html` (ya koi bhi HTML file) ko browser mein direct open kar dein — koi build step ya server zaroori nahi.