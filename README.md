# 🎓 TalentPath - Comprehensive Learning & Career Platform

<div align="center">

![TalentPath Banner](https://img.shields.io/badge/TalentPath-Your_Career_Journey-orange?style=for-the-badge)

**Master Coding. Land Your Dream Job.**

[![Next.js](https://img.shields.io/badge/Next.js-15.5.5-black?style=flat&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=flat&logo=typescript)](https://www.typescriptlang.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791?style=flat&logo=postgresql)](https://www.postgresql.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat&logo=tailwind-css)](https://tailwindcss.com/)

[Features](#-features) • [Tech Stack](#-tech-stack) • [Getting Started](#-getting-started) • [Project Structure](#-project-structure) • [Contributing](#-contributing)

</div>

---

## 📖 Overview

**TalentPath** is a full-stack learning platform designed to help students and developers master Data Structures & Algorithms, prepare for technical interviews, compete in coding contests, and discover career opportunities — all in one unified platform.

### 🎯 Key Highlights

- 📚 **6,300+ DSA Problems** from LeetCode, GeeksForGeeks, HackerRank, and Codeforces
- 🏆 **Real-time Coding Contests** with automated evaluation
- 💻 **Multi-language Online Compiler** (Python, JavaScript, C++, Java, C)
- 🧠 **Aptitude Test Module** for quantitative and logical reasoning
- 💼 **Job Portal** with company-wise problem filtering
- 🗺️ **Career Roadmaps** for personalized learning paths
- 🤖 **AI-Powered Chatbot** for coding assistance (Gemini API)
- 👨‍💼 **Admin Dashboard** with role-based access control

---

## ✨ Features

### 🔐 Authentication & Authorization
- **NextAuth** integration with Google OAuth
- Multi-role access control (Admin, Student)
- Secure session management with JWT
- Protected routes and API endpoints

### 💡 DSA Practice Sheet
- **6,300+ curated problems** across multiple platforms
- Filter by difficulty (Easy, Medium, Hard)
- Platform-specific sheets (LeetCode, GeeksForGeeks)
- **Company-wise problem filtering** (Google, Amazon, Microsoft, etc.)
- Progress tracking with visual indicators
- Bookmark favorite problems
- Real-time statistics with pre-calculated topic stats

### 🏆 Coding Contests
- Create and manage contests with admin panel
- **Monaco Editor** integration for code editing
- Support for 5+ programming languages
- Automated test case evaluation
- Real-time leaderboards and rankings
- Submission history with detailed results
- Contest timer and automatic submission cutoff

### 💻 Online Compiler
- **Monaco Editor** with syntax highlighting
- Execute code in multiple languages:
  - Python, JavaScript, TypeScript
  - Java, C, C++
- Real-time compilation and execution
- Custom input support
- Error handling and output display

### 🧠 Aptitude Tests
- Quantitative reasoning questions
- Logical reasoning problems
- Verbal ability assessments
- **IndiaBIX platform integration**
- Automated scoring system
- Performance tracking and analytics

### 💼 Job Portal
- Browse internship and job opportunities
- Company-wise problem recommendations
- Application tracking
- Job details with requirements

### 🗺️ Career Roadmaps
- Structured learning paths
- Frontend, Backend, Full-Stack roadmaps
- AI/ML and Data Science tracks
- Step-by-step guidance with resources

### 🤖 AI Chatbot Assistant
- **Gemini API** powered intelligent assistant
- Context-aware coding help
- DSA concept explanations
- Debugging assistance
- Conversation history persistence
- Multi-conversation management

### 📊 Personal Dashboard
- Comprehensive progress tracking
- DSA problem statistics
- Contest performance metrics
- Aptitude test results
- Recent activity feed
- Quick action shortcuts

### 👨‍💼 Admin Panel
- **DSA Questions Management**: Add, edit, visibility control
- **Contest Management**: Create contests, add problems, manage test cases
- **Job Posting**: Add internships and job opportunities
- **Roadmap Creation**: Design learning paths
- **Aptitude Questions**: Create and manage test questions
- **User Management**: View user statistics and activity
- **Analytics Dashboard**: Platform-wide statistics

---

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 15.5.5 (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4, ShadCN UI
- **Animations**: Framer Motion
- **Code Editor**: Monaco Editor
- **UI Components**: Radix UI primitives
- **Form Handling**: React Hook Form + Zod validation
- **Markdown**: React Markdown with syntax highlighting

### Backend
- **Runtime**: Node.js
- **Framework**: Next.js API Routes
- **Authentication**: NextAuth 5 (Google OAuth)
- **Database**: PostgreSQL (Supabase)
- **ORM**: Drizzle ORM + Prisma
- **AI Integration**: Anthropic Claude API, Google Gemini API
- **File Storage**: Cloudinary (for future features)

### DevOps & Tools
- **Version Control**: Git, GitHub
- **Deployment**: Vercel (recommended)
- **Database Hosting**: Supabase
- **Package Manager**: npm
- **Linting**: ESLint 9 with TypeScript
- **Code Formatting**: Prettier (implied)

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** 20.x or higher
- **PostgreSQL** database (Supabase recommended)
- **Google OAuth** credentials
- **Gemini API** key (for AI chatbot)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/swamyrayudu/TalentPath.git
   cd TalentPath
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```



3. **Set up the database**

   Run the database migrations:
   ```bash
   # Using Drizzle
   npm run db:push
   
   # Or run SQL migrations manually in Supabase
   # Execute files in /migrations/ folder in order
   ```

4. **Initialize the visible problems system**

   In Supabase SQL Editor, run:
   ```sql
   -- Execute setup-visible-problems-system.sql
   -- This creates tables, functions, and triggers
   ```

5. **Seed initial data (optional)**
   ```bash
   # Run any seed scripts if available
   npm run seed
   ```

6. **Start the development server**
   ```bash
   npm run dev
   ```

7. **Open your browser**
   
   Navigate to `http://localhost:3000`

---

## 📁 Project Structure

```
TalentPath/
├── src/
│   ├── app/                      # Next.js App Router pages
│   │   ├── api/                  # API routes
│   │   │   ├── admin/            # Admin APIs
│   │   │   ├── ai-chat/          # AI chatbot API
│   │   │   ├── aptitude/         # Aptitude test APIs
│   │   │   ├── auth/             # Authentication
│   │   │   ├── compile/          # Code compilation
│   │   │   ├── contest-stats/    # Contest statistics
│   │   │   ├── dsa-stats/        # DSA statistics
│   │   │   ├── jobs/             # Job portal APIs
│   │   │   ├── problems/         # Problem management
│   │   │   └── visible-problems/ # Problem visibility
│   │   ├── admin/                # Admin dashboard pages
│   │   ├── aptitude/             # Aptitude test interface
│   │   ├── companies/            # Company-wise problems
│   │   ├── compiler/             # Online compiler
│   │   ├── contest/              # Contest pages
│   │   ├── dashboard/            # User dashboard
│   │   ├── dsasheet/             # DSA practice sheet
│   │   ├── jobs/                 # Job portal
│   │   └── roadmap/              # Career roadmaps
│   ├── components/               # React components
│   │   ├── admin/                # Admin components
│   │   ├── auth/                 # Authentication UI
│   │   ├── compiler/             # Compiler components
│   │   ├── contest/              # Contest components
│   │   ├── dashboard/            # Dashboard widgets
│   │   ├── dsa/                  # DSA sheet components
│   │   ├── layouts/              # Layout components
│   │   ├── providers/            # Context providers
│   │   └── ui/                   # ShadCN UI components
│   ├── lib/                      # Utility libraries
│   │   ├── db/                   # Database schema & config
│   │   ├── auth.ts               # Auth configuration
│   │   └── utils.ts              # Helper functions
│   ├── hooks/                    # Custom React hooks
│   ├── actions/                  # Server actions
│   └── middleware.ts             # Next.js middleware
├── migrations/                   # Database migrations
├── scripts/                      # SQL scripts & utilities
├── public/                       # Static assets
│   └── company-logos/            # Company logo images
├── components.json               # ShadCN config
├── next.config.ts                # Next.js configuration
├── tailwind.config.js            # Tailwind CSS config
├── tsconfig.json                 # TypeScript config
└── package.json                  # Dependencies
```

---

## 🗄️ Database Schema

### Core Tables

- **`users`** - User accounts and profiles
- **`problems`** - DSA problems (6,300+ entries)
- **`visible_problems`** - Filtered problems for users (auto-synced)
- **`dsa_topic_stats`** - Pre-calculated statistics
- **`user_progress`** - Problem completion tracking
- **`contests`** - Contest information
- **`questions`** - Contest problems
- **`test_cases`** - Problem test cases
- **`submissions`** - User code submissions
- **`aptitude_results`** - Aptitude test scores
- **`jobs`** - Job postings
- **`roadmaps`** - Learning path data
- **`chat_history`** - AI chatbot conversations
- **`notifications`** - User notifications

### Database Triggers

- **Auto-sync triggers** on `problems` table
- **Statistics refresh** on problem visibility changes
- Ensures data consistency across tables

---

## 🔑 Key Features Implementation

### 1. Visible Problems System

Uses a **two-table architecture** for performance:
- `problems` - Full dataset (admin only)
- `visible_problems` - Filtered subset (public)
- PostgreSQL triggers auto-sync changes
- Pre-calculated stats for instant queries

**Query Performance**: <200ms average response time

### 2. Contest System

- Real-time problem solving with Monaco Editor
- Automated test case evaluation
- Background code execution
- Submission tracking and leaderboards
- Contest timer with automatic cutoff

### 3. AI Chatbot

- Gemini API integration
- Conversation context preservation
- Multi-conversation management
- Markdown rendering with code highlighting
- Extended thinking/reasoning display

### 4. Admin Dashboard

Role-based access control with features:
- Bulk problem import (CSV)
- Visibility management
- Contest creation and management
- User analytics and statistics

---

## 🎨 UI/UX Features

- **Responsive Design**: Mobile-first approach
- **Dark Mode**: System-aware theme switching
- **Smooth Animations**: Framer Motion transitions
- **Accessible**: ARIA labels and keyboard navigation
- **Performance**: Optimized with Next.js 15 features
- **SEO-friendly**: Meta tags and Open Graph support

---

## 📊 Performance Optimizations

- **Database Indexing**: Optimized queries with strategic indexes
- **Caching**: Client-side caching for frequently accessed data
- **Code Splitting**: Automatic with Next.js
- **Image Optimization**: Next.js Image component
- **Lazy Loading**: React Suspense for heavy components
- **API Rate Limiting**: Protected endpoints

---

## 🔒 Security Features

- **NextAuth** for secure authentication
- **SQL Injection Protection**: Parameterized queries with Drizzle
- **XSS Protection**: Input sanitization
- **CSRF Tokens**: Built-in Next.js protection
- **Role-based Access Control**: Admin-only routes
- **Secure Headers**: Next.js security headers
- **Environment Variables**: Sensitive data protection

---

## 🧪 Testing

```bash
# Run linting
npm run lint

# Fix linting issues
npm run lint:fix

# Build for production (checks for errors)
npm run build
```

---

## 🚀 Deployment

### Vercel (Recommended)

1. Push code to GitHub
2. Import project in Vercel
3. Configure environment variables
4. Deploy automatically

### Manual Deployment

```bash
# Build the project
npm run build

# Start production server
npm start
```

---

## 📝 Environment Variables Reference

| Variable | Description | Required |
|----------|-------------|----------|
| `DATABASE_URL` | PostgreSQL connection string | ✅ |
| `NEXTAUTH_URL` | Application URL | ✅ |
| `NEXTAUTH_SECRET` | NextAuth secret key | ✅ |
| `GOOGLE_CLIENT_ID` | Google OAuth client ID | ✅ |
| `GOOGLE_CLIENT_SECRET` | Google OAuth secret | ✅ |
| `ANTHROPIC_API_KEY` | Claude API key | ❌ |
| `GEMINI_API_KEY` | Gemini API key | ✅ |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name | ❌ |
| `CLOUDINARY_API_KEY` | Cloudinary API key | ❌ |
| `CLOUDINARY_API_SECRET` | Cloudinary secret | ❌ |

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Commit changes**: `git commit -m 'Add amazing feature'`
4. **Push to branch**: `git push origin feature/amazing-feature`
5. **Open a Pull Request**

### Development Guidelines

- Follow TypeScript best practices
- Use ESLint configuration
- Write meaningful commit messages
- Test thoroughly before submitting PR
- Update documentation if needed

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 👥 Team

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/swamyrayudu">
        <img src="https://github.com/swamyrayudu.png" width="100px;" alt="Swamy"/>
        <br />
        <sub><b>R.V.V. Swamy</b></sub>
      </a>
      <br />
      <a href="https://www.linkedin.com/in/rayudu-veera-venkata-swamy/">LinkedIn</a>
    </td>
    <td align="center">
      <a href="https://github.com/Durga62823">
        <img src="https://github.com/Durga62823.png" width="100px;" alt="Durga Prasad"/>
        <br />
        <sub><b>Durga Prasad</b></sub>
      </a>
      <br />
      <a href="https://www.linkedin.com/in/peddapalli-satya-venkata-siva-durga-prasad-9b9602295/">LinkedIn</a>
    </td>
  </tr>
</table>

---

## 📞 Support

For support, email [psivadurgaprasad88@gmail.com](mailto:psivadurgaprasad88@gmail.com) or open an issue in the repository.

---

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) - React framework
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS
- [ShadCN UI](https://ui.shadcn.com/) - Component library
- [Supabase](https://supabase.com/) - Database hosting
- [Vercel](https://vercel.com/) - Deployment platform
- [Google Gemini](https://ai.google.dev/) - AI API
- [Monaco Editor](https://microsoft.github.io/monaco-editor/) - Code editor

---

<div align="center">

**Built with ❤️ by the TalentPath Team**

⭐ Star this repository if you find it helpful!

[Report Bug](https://github.com/swamyrayudu/TalentPath/issues) • [Request Feature](https://github.com/swamyrayudu/TalentPath/issues)

</div>
