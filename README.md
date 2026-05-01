# Next.js Dashboard App

A full-stack dashboard application built with **Next.js App Router**, based on the official tutorial by Vercel, with custom improvements and fixes.

🔗 **Live Demo**  
[Acme Dashboard](https://next-js-tutorial-ashen-psi.vercel.app/dashboard)

---

## 🚀 Overview

This project is a modern dashboard application that demonstrates:

- Server-side rendering with Next.js

- Server Actions for data mutations

- Database integration using Neon (PostgreSQL)

- Dynamic routing and data fetching

- Caching and revalidation strategies

While the core structure follows the official tutorial, I made several modifications and improvements to better understand the system and enhance the behavior of the app.

---

## ✨ Features

- 📊 Dashboard with analytics overview

- 🧾 Invoice management (create, update, delete)

- ⚡ Server Actions for handling mutations

- 🗄️ PostgreSQL database hosted on Neon

- 🎨 Custom styling and UI tweaks

- 🔁 Proper cache revalidation across routes

---

## 🛠️ Improvements & Fixes

During development, I encountered and resolved an issue where deleting invoices did not update the dashboard data.

### Fix: Cache Revalidation

The original implementation only revalidated the invoices page:

```ts
revalidatePath('/dashboard/invoices');
```

This caused stale data on the main dashboard.

### ✅ Solution

I fixed this by also revalidating the dashboard route:

```ts
revalidatePath('/dashboard');
```

This ensures all related views stay in sync after mutations.

---

## 🧰 Tech Stack

- **Framework:** Next.js (App Router)

- **Database:** Neon (PostgreSQL)

- **Styling:** Tailwind CSS

- **Deployment:** Vercel

---

## 🧪 Learning Outcomes

This project helped me better understand:

- How Next.js handles caching and revalidation

- Server vs Client Components

- Real-world data mutation patterns

- Structuring full-stack applications using the App Router

---

## 🎨 Customizations

- Modified UI styling and color palette

- Updated favicon

- Minor UX adjustments for experimentation

---

## 🔮 Future Improvements

Planned enhancements to extend the project further:

- Deploy the application to a VPS instead of relying on Vercel

- Implement full authentication (account creation & password management)

- Add the ability to create and manage customers

---

## 🙏 Acknowledgements

- Based on the official Next.js tutorial by Vercel

- [App Router | Next.js](https://nextjs.org/learn/dashboard-app)

---

## 📬 Contact

Feel free to reach out if you'd like to connect or discuss opportunities.
