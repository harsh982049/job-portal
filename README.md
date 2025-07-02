# Job Portal – Full-Stack Recruitment Platform

A modern, full-stack recruitment platform where **recruiters can post jobs** and **candidates can apply**. The platform integrates **Clerk for authentication** and **Supabase for database and storage**, and features a clean UI built with **React, TailwindCSS, and ShadCN UI**.

---

## 🚀 Features

* 🔐 **Clerk Authentication** (Sign up, Sign in, Role-based access)
* 🏢 **Company Management** (Add new companies with logo upload)
* 📄 **Job Posting** (Recruiters can create job listings with Markdown support)
* 🔍 **Job Browsing** (Candidates can view and filter open jobs)
* 📁 **Supabase Storage** (Upload and serve company logos)
* 🎨 **Modern UI** using TailwindCSS + ShadCN
* ⚙️ **Form Validation** via React Hook Form + Zod

---

## 📦 Tech Stack

| Layer          | Tech Used                      |
| -------------- | ------------------------------ |
| Frontend       | React, TailwindCSS, ShadCN UI  |
| Auth           | Clerk                          |
| Backend (BaaS) | Supabase (Database + Storage)  |
| Forms & UX     | React Hook Form, Zod, MDEditor |
| Routing        | React Router DOM               |
| State/Fetch    | Custom Hooks, React useEffect  |

---

## 🛠️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/job-portal.git
cd job-portal
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Setup Clerk Authentication

* Go to [Clerk.dev](https://clerk.dev/) and create a new project.
* Get your **Clerk Publishable Key** and **Clerk Secret Key**.
* Enable sign in/sign up options for recruiters and candidates.

In your `.env` file:

```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
```

### 4. Setup Supabase

* Go to [Supabase.io](https://supabase.io/) and create a new project.
* Navigate to the SQL Editor and create tables:

#### Table: `companies`

* `id`: integer, primary key
* `name`: text
* `logo_url`: text

#### Table: `jobs`

* `id`: integer, primary key
* `title`: text
* `description`: text
* `location`: text
* `company_id`: integer (foreign key)
* `requirements`: text
* `recruiter_id`: text
* `isOpen`: boolean

#### Storage:

* Go to **Storage** tab
* Create a **public bucket** named: `company-logo`

In your `.env` file:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 5. Run the App

```bash
npm run dev
```

Visit the app at: `http://localhost:5173`

---

## 🔧 Future Improvements

* ✅ Candidate job application feature
* 🔍 Job search and filters by location/company
* 📅 Resume upload & preview
* 📊 Admin dashboard for analytics
* ✅ Automated test coverage
* 🌐 Deploy on Vercel or Netlify
