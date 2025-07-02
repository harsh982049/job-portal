# Job Portal – Full-Stack Recruitment Platform

A modern, full-stack recruitment platform where **recruiters can post jobs** and **candidates can apply**. The platform integrates **Clerk for authentication** and **Supabase for database and storage**, and features a clean UI built with **React, TailwindCSS, and ShadCN UI**.

---

## 🚀 Features

- 🔐 **Clerk Authentication** (Sign up, Sign in, Role-based access)
- 🏢 **Company Management** (Add new companies with logo upload)
- 📄 **Job Posting** (Recruiters can create job listings with Markdown support)
- 🔍 **Job Browsing** (Candidates can view and filter open jobs)
- 📁 **Supabase Storage** (Upload and serve company logos)
- 🎨 **Modern UI** using TailwindCSS + ShadCN
- ⚙️ **Form Validation** via React Hook Form + Zod

---

## 📦 Tech Stack

| Layer          | Tech Used                         |
|----------------|----------------------------------|
| Frontend       | React, TailwindCSS, ShadCN UI     |
| Auth           | Clerk                             |
| Backend (BaaS) | Supabase (Database + Storage)     |
| Forms & UX     | React Hook Form, Zod, MDEditor    |
| Routing        | React Router DOM                  |
| State/Fetch    | Custom Hooks, React useEffect     |

---

## 🛠️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/job-portal.git
cd job-portal

2. Install dependencies

npm install

3. Setup Clerk

    Go to Clerk.dev and create a project.

    Copy your CLERK_PUBLISHABLE_KEY and CLERK_SECRET_KEY.

    Enable Sign in / Sign up for both users and recruiters.

    In your .env file, add:

VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key

4. Setup Supabase

    Go to Supabase and create a new project.

    Create a companies table with fields:

        id: integer, PK

        name: text

        logo_url: text

    Create a jobs table with fields:

        id, title, description, location, company_id, requirements, recruiter_id, isOpen

    Create a company-logo Storage Bucket (public)

    In your .env file, add:

VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_anon_key

    ⚠️ Make sure bucket is public and project storage rules allow upload.

5. Run the app

npm run dev

    App runs locally at http://localhost:5173

🔧 Future Improvements

    ✅ Apply to job functionality for candidates

    🔍 Add search and filtering for jobs by location/company

    📁 Resume upload and preview

    📊 Admin dashboard for managing jobs & analytics

    🧪 Add unit & integration tests

    🌐 Deployment (e.g., Vercel or Netlify)