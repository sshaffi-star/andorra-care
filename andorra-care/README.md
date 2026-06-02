# AndorraCare Web Apps

Healthcare web portal — Patient App & Staff Operations Dashboard.

## Apps
| App | File | Description |
|-----|------|-------------|
| Patient Portal | `andorra-patient-app.html` | Patient-facing health app |
| Staff Dashboard | `andorra-staff-dashboard.html` | Clinical operations dashboard |

---

## 🚀 How to Deploy (GitHub Pages)

### Step 1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) → **New repository**
2. Name it: `andorra-care` (or any name you like)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 2 — Upload the files

Drag and drop these files into the repository via the GitHub web interface:

```
index.html
andorra-patient-app.html
andorra-staff-dashboard.html
.github/
  workflows/
    deploy.yml
```

Or use Git in your terminal:
```bash
git clone https://github.com/YOUR_USERNAME/andorra-care.git
cd andorra-care
# copy all files here
git add .
git commit -m "Initial deployment"
git push origin main
```

### Step 3 — Enable GitHub Pages

1. In your repository → **Settings** → **Pages**
2. Under **Source**, select: **GitHub Actions**
3. The workflow will trigger automatically on every push to `main`

### Step 4 — Access your apps

After ~1 minute your apps will be live at:
```
https://YOUR_USERNAME.github.io/andorra-care/
```

---

## 🗄️ Neon Database (Future Integration)

The current apps are **static HTML** (no backend required). When you're ready to connect a live database:

1. Sign up at [neon.tech](https://neon.tech)
2. Create a new project: **AndorraCare**
3. Copy your connection string:
   ```
   postgresql://user:password@ep-xxx.neon.tech/andorracare?sslmode=require
   ```
4. Use it in a backend API (Node.js/Express or Next.js) to serve dynamic data
5. Update the HTML files to fetch from your API endpoint

**Recommended Neon tables (based on PRD):**
- `patients` — patient profiles
- `appointments` — scheduling
- `medications` — prescriptions & tracking
- `staff` — clinical staff accounts
- `audit_logs` — ASPC compliance logs

---

## 📁 Project Structure

```
andorra-care/
├── index.html                   # Portal landing page
├── andorra-patient-app.html     # Patient mobile app
├── andorra-staff-dashboard.html # Staff operations dashboard
├── .github/
│   └── workflows/
│       └── deploy.yml           # Auto-deploy to GitHub Pages
└── README.md
```
