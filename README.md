# 🚀 Mekanism ATS - Project Structure

📦 mekanism-ats
 ┣ 📂 public                   # 🖼️ Static assets (company logos, icons, mock PDFs)
 ┣ 📂 src
 │ ┣ 📂 app                    # 🛣️ Next.js App Router (Pages & API)
 │ │ ┣ 📂 (auth)               # 🔐 Route Group: Authentication
 │ │ │ ┗ 📂 login
 │ │ │   ┗ 📜 page.tsx         # Secure login screen
 │ │ ┣ 📂 (dashboards)         # 🛡️ Route Group: Protected Application
 │ │ │ ┣ 📂 admin              # 👑 Page 1: Governance & Security
 │ │ │ │ ┣ 📂 users
 │ │ │ │ │ ┗ 📜 page.tsx       # User Lifecycle Management
 │ │ │ │ ┗ 📂 audit-logs
 │ │ │ │   ┗ 📜 page.tsx       # System Activity & Security Heatmap
 │ │ │ ┣ 📂 hr                 # 📊 Pages 2, 3, 4: Command Center
 │ │ │ │ ┣ 📂 analytics
 │ │ │ │ │ ┗ 📜 page.tsx       # Hero Dashboard & Vendor Leaderboard
 │ │ │ │ ┣ 📂 jobs
 │ │ │ │ │ ┣ 📜 page.tsx       # Active Requisitions Table
 │ │ │ │ │ ┗ 📂 create
 │ │ │ │ │   ┗ 📜 page.tsx     # The Job Builder & Vendor Assignment
 │ │ │ │ ┗ 📂 pipeline
 │ │ │ │   ┗ 📜 page.tsx       # Master Kanban Pipeline
 │ │ │ ┣ 📂 manager            # 🎯 Page 5: Evaluation Terminal
 │ │ │ │ ┗ 📂 interviews
 │ │ │ │   ┗ 📜 page.tsx       # Scorecards & Vendor Rating
 │ │ │ ┗ 📂 vendor             # 🤝 Pages 6, 7: Sourcing Portal
 │ │ │   ┣ 📂 performance
 │ │ │   │ ┗ 📜 page.tsx       # Domain-Specific Analytics Dashboard
 │ │ │   ┗ 📂 board
 │ │ │     ┣ 📜 page.tsx       # Active Bounties (Job Cards)
 │ │ │     ┗ 📂 [jobId]
 │ │ │       ┗ 📜 page.tsx     # Job Details & Frictionless Submission Dropzone
 │ │ ┣ 📂 api                  # ⚙️ Backend Serverless Routes
 │ │ │ ┣ 📂 auth               # Session management
 │ │ │ ┣ 📂 candidates         # Resume parsing, deduplication, status updates
 │ │ │ ┣ 📂 jobs               # Requisition CRUD operations
 │ │ │ ┗ 📂 vendors            # Analytics and rating calculations
 │ │ ┣ 📜 layout.tsx           # Root application layout (Providers, Fonts)
 │ │ ┗ 📜 page.tsx             # Initial landing/redirect logic
 │ ┣ 📂 components             # 🧩 UI Architecture (Stitch/Relume Exports)
 │ │ ┣ 📂 features             # Complex, domain-specific modules
 │ │ │ ┣ 📂 kanban             # Kanban columns, draggable cards
 │ │ │ ┣ 📂 forms              # Job builder, candidate submission forms
 │ │ │ ┣ 📂 charts             # Funnel charts, skill radars, heatmaps
 │ │ │ ┗ 📂 modals             # Deep-dive slide-out drawers, scorecards
 │ │ ┣ 📂 layout               # Page structure elements
 │ │ │ ┣ 📜 Sidebar.tsx        # Dynamic navigation based on user role
 │ │ │ ┗ 📜 Header.tsx         # Top bar with global search & notifications
 │ │ ┗ 📂 ui                   # Atomic components (Buttons, Inputs, Badges, Tables)
 │ ┣ 📂 lib                    # 🛠️ Core Configurations & Utilities
 │ │ ┣ 📜 db.ts                # PostgreSQL/Supabase connection instance
 │ │ ┣ 📜 utils.ts             # Date formatting, class merging (Tailwind-merge)
 │ │ ┗ 📜 rbac.ts              # Role-Based Access Control logic helper
 │ ┣ 📂 types                  # 🏷️ TypeScript Definitions
 │ │ ┣ 📜 user.ts              # Interfaces for Admin, HR, Manager, Vendor
 │ │ ┣ 📜 candidate.ts         # Interfaces for Resumes, Status, Parsed Skills
 │ │ ┗ 📜 job.ts               # Interfaces for Requisitions
 │ ┗ 📂 services               # 🔌 Third-Party Integrations
 │   ┣ 📜 email.ts             # Resend/SendGrid workflow notifications
 │   ┗ 📜 ai-parser.ts         # Resume parsing & skill matching logic
 ┣ 📜 .env.local               # 🔑 Environment Variables (DB string, API keys)
 ┣ 📜 middleware.ts            # 🚦 Edge Middleware (Route protection & redirects)
 ┣ 📜 next.config.mjs          # ⚙️ Next.js build configuration
 ┣ 📜 tailwind.config.ts       # 🎨 Tailwind theme, colors, and plugins
 ┗ 📜 package.json             # 📦 Project dependencies
