# 📖 Story: Deploying Web Invites on Vercel

---

## 🏷️ Title
Fusing React, Tailwind, and Vite for a Live Wedding Invitation Deployment

---

## 📝 Background
We developed an interactive digital wedding invitation platform featuring responsive layouts, guest RSVP submission elements, and smooth animations.

---

## ❓ Problem
We needed to integrate a React and TypeScript frontend client with backend RSVP storage APIs and deploy the site securely without running expensive server infrastructure or managing container configurations for a highly seasonal landing page.

---

## ⚖️ Decision
We decided to decouple the frontend entirely, building the application client inside a **PNPM Workspace** utilizing React, Vite, and Tailwind CSS, and hosting the application on **Vercel** for serverless, global CDN distribution.

---

## 🛠️ Implementation
* Initialized a PNPM monorepo to isolate dependencies and share configurations.
* Configured Vite for fast local hot-reload and optimized production build output.
* Deployed the project repository to Vercel, mapping dynamic environment variables to secure target API endpoints.

---

## 📈 Result
* **Zero Infrastructure Overhead**: Secured stable site delivery during traffic peaks without provisioning servers.
* **Fast Load Times**: Globally distributed static assets using Vercel's CDN, ensuring immediate invite loads for mobile guests.

---

## 🎓 Lessons

### General Lesson
* Keep client assets static and serverless whenever possible to minimize maintenance and scaling costs.

### Technical Lesson
* PNPM workspaces simplify the management of shared TypeScript configurations across decoupled frontend components.

### Business Lesson
* Seasonal landing pages are best served via serverless static hosting models rather than continuous server infrastructure.

---

## 🎨 Social Media Distribution Playbook

### 🔗 Potential LinkedIn Angles
* Why serverless hosting is the most cost-efficient choice for temporary high-traffic landing pages.

### 🎥 Potential Video Angles
* Walking through the PNPM workspace configuration files.

### 📨 Potential Newsletter Angles
* Setting up automated deployment webhooks using GitHub Actions and Vercel.
