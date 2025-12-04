# AI Career Coach – AI-Powered Career Guidance & Interview Preparation Platform

An intelligent, end-to-end career coaching system built using Next.js, NeonDB, Prisma ORM, Tailwind, Shadcn UI, and Gemini API.  
The platform provides personalized job recommendations, resume enhancement, interview preparation, and real-time AI chat to guide users through their entire career journey.

##  Features

### 1. AI-Driven Career Coaching
- Personalized job paths tailored to user skills, experience, and market demand.  
- Real-time answers about careers, tech stacks, job roles, and interview strategies.

### 2. Smart Resume Builder
- AI-generated resumes optimized for ATS.  
- Auto-rewrite of bullet points, project descriptions, and achievements.

### 3. Interview Preparation
- AI-generated mock questions and expected answers.  
- Voice-based follow-up questions (optional extension).  
- Structured feedback on clarity, content quality, and confidence.

### 4. Cover Letter & Email Generation
- One-click AI-generated cover letters, follow-up emails, HR outreach messages.

### 5. Scalable Backend
- Built with NeonDB + Prisma for performance and cloud-native reliability.  
- Secure user management with session-based authentication.

### 6. Modern, Responsive UI
- Built using Tailwind + Shadcn UI for minimal, elegant design.  
- Smooth animations, responsive layouts, and multi-device support.

##  System Architecture

Next.js (Frontend + API Routes)  
Gemini API (AI processing)  
Prisma ORM  
NeonDB (PostgreSQL Cloud Database)

##  Tech Stack

Frontend: Next.js, Tailwind CSS, Shadcn UI  
Backend: Next.js API Routes, Gemini API  
Database: NeonDB, Prisma ORM  
Hosting: Vercel  
Tools: TypeScript, JWT (optional), Zod (optional)

##  Folder Structure

ai-career-coach/  
app/  
components/  
utils/  
prisma/  
schema.prisma

##  Setup Instructions

1. Clone the Repository

git clone https://github.com/username/ai-career-coach.git  
cd ai-career-coach

2. Install Dependencies  
npm install

3. Create .env File

DATABASE_URL="your-neon-db-url"  
NEXT_PUBLIC_GEMINI_API_KEY="your-api-key"

4. Push Prisma Schema  
npx prisma generate  
npx prisma db push

5. Start Development Server  
npm run dev

##  Core AI Workflows

Career Recommendation Engine  
Resume Enhancement  
Mock Interview Flow

##  Database Schema

model User {  
  id        String   @id @default(cuid())  
  name      String?  
  email     String   @unique  
  createdAt DateTime @default(now())  
  sessions  Session[]  
}

model Session {  
  id        String   @id @default(cuid())  
  userId    String  
  content   Json  
  createdAt DateTime @default(now())  
  user      User     @relation(fields: [userId], references: [id])  
}

##  Motivation

This project aims to solve the lack of personalized guidance, structured interview practice, ATS-friendly resume writing, and clarity in career planning.

##  Future Enhancements

- Voice-based interviews  
- Job scraping + skill-gap analysis  
- Personalized learning paths  
- User analytics dashboard


