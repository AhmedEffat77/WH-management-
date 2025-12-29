# 📁 File Navigation Guide

## Quick Reference - What Each File Does

---

## 🌐 HTML Pages (User Interface)

### `index.html` 
**Purpose:** Login page  
**Who uses:** Everyone  
**What it does:** Authenticates users and redirects to appropriate dashboard

### `user-dashboard.html`
**Purpose:** Regular user interface  
**Who uses:** Warehouse workers, requesters  
**What it does:**
- Search and select items
- Submit requests with quantity and notes
- View own request history
- Track request status (pending/approved/rejected)

### `warehouse-dashboard.html`
**Purpose:** Manager interface  
**Who uses:** Warehouse managers  
**What it does:**
- View pending requests needing approval
- Approve or reject requests with comments
- Upload stock data from CSV files
- Manage inventory
- View request history

### `technical-dashboard.html`
**Purpose:** Reports and analytics  
**Who uses:** Technical managers, supervisors  
**What it does:**
- View daily/weekly reports
- See requests by department
- Display charts (pie chart for status, bar chart for departments)
- Filter by date range
- Export reports to CSV

### `admin-dashboard.html`
**Purpose:** System overview  
**Who uses:** System administrators  
**What it does:**
- View all users
- See system statistics
- Monitor recent activity
- Quick access to other dashboards

---

## ⚙️ JavaScript Files (Functionality)

### `js/auth.js`
**Purpose:** Core utilities  
**Contains:**
- `authenticateUser()` - Login functionality
- `getCurrentUser()` - Get logged-in user
- `requireRole()` - Check user permissions
- `logout()` - Logout function
- `apiGet()`, `apiCreate()`, `apiUpdate()`, `apiPatch()`, `apiDelete()` - Database operations
- `formatDate()` - Date formatting
- `showNotification()` - Pop-up messages
- `exportToCSV()` - Export data
- `parseCSV()` - Read CSV files

**Used by:** All pages (included via `<script>` tag)

### `js/user-dashboard.js`
**Purpose:** User features  
**Contains:**
- Item search with autocomplete
- Request submission form handling
- Stock availability checking
- Request table display
- Real-time stats updates

**Used by:** `user-dashboard.html`

### `js/warehouse-dashboard.js`
**Purpose:** Manager features  
**Contains:**
- Pending requests display
- Approve/reject workflow
- CSV file upload and parsing
- Stock table display with search
- Request history filtering
- Export functionality

**Used by:** `warehouse-dashboard.html`

### `js/technical-dashboard.js`
**Purpose:** Reports and charts  
**Contains:**
- Dashboard statistics calculation
- Chart.js chart generation
- Date range filtering
- Request table by department
- CSV report export
- Analytics processing

**Used by:** `technical-dashboard.html`

---

## 📄 Documentation Files

### `README.md` ⭐ START HERE FIRST
**Purpose:** Complete system documentation  
**Contents:**
- System overview
- Features list
- Installation instructions
- User guide for each role
- Technical details
- FAQ

**Read this:** To understand the entire system

### `DEPLOYMENT_GUIDE.md` ⭐ DEPLOY HERE
**Purpose:** How to put it online  
**Contents:**
- 5 deployment methods explained
- Step-by-step instructions
- Free hosting options
- Paid hosting options
- Custom domain setup
- Troubleshooting

**Read this:** When ready to deploy for multiple users

### `QUICK_START.md` ⭐ FASTEST PATH
**Purpose:** Get started in 5 minutes  
**Contents:**
- Rapid deployment to Netlify
- Quick testing workflow
- Essential setup steps
- Immediate access guide

**Read this:** If you want to deploy ASAP

### `SYSTEM_COMPLETE.md` ⭐ PROJECT SUMMARY
**Purpose:** What's included  
**Contents:**
- Complete feature list
- What was delivered
- Testing results
- Next steps
- Success checklist

**Read this:** To see everything that was built

### `FILE_MAP.md` (This file)
**Purpose:** Navigate the project  
**Contents:**
- What each file does
- How files relate to each other
- Quick reference guide

**Read this:** To understand the project structure

---

## 🗂️ Complete File Structure

```
warehouse-system/
│
├── 📄 HTML Pages (Frontend UI)
│   ├── index.html                      # Login
│   ├── user-dashboard.html             # User interface
│   ├── warehouse-dashboard.html        # Manager interface
│   ├── technical-dashboard.html        # Reports & analytics
│   └── admin-dashboard.html            # Admin overview
│
├── 📁 js/ (JavaScript Functionality)
│   ├── auth.js                         # Core utilities & API
│   ├── user-dashboard.js               # User features
│   ├── warehouse-dashboard.js          # Manager features
│   └── technical-dashboard.js          # Technical features
│
└── 📚 Documentation
    ├── README.md                        # Complete guide
    ├── DEPLOYMENT_GUIDE.md              # How to deploy
    ├── QUICK_START.md                   # 5-minute setup
    ├── SYSTEM_COMPLETE.md               # Project summary
    └── FILE_MAP.md                      # This file
```

---

## 🔄 How Files Work Together

### User Flow Example:

```
1. User opens: index.html
   └─> Loads: js/auth.js
   └─> Authenticates user
   └─> Redirects to: user-dashboard.html

2. User Dashboard loads
   └─> Loads: js/auth.js (utilities)
   └─> Loads: js/user-dashboard.js (features)
   └─> Calls API: GET /tables/stock_items (load items)
   └─> Calls API: GET /tables/requests (load requests)
   └─> Displays interface

3. User submits request
   └─> js/user-dashboard.js processes form
   └─> js/auth.js makes: POST /tables/requests
   └─> Database stores request
   └─> User sees success message

4. Manager opens: warehouse-dashboard.html
   └─> Loads: js/auth.js + js/warehouse-dashboard.js
   └─> Calls API: GET /tables/requests (sees user's request)
   └─> Manager clicks "Approve"
   └─> js/warehouse-dashboard.js makes: PATCH /tables/requests
   └─> Database updates request status

5. Technical Manager opens: technical-dashboard.html
   └─> Loads: js/auth.js + js/technical-dashboard.js
   └─> Calls API: GET /tables/requests
   └─> Displays charts using Chart.js
   └─> Shows approved request in report
```

**All users see the same data because they share the same database!**

---

## 📖 Reading Order

### For First-Time Users:

1. **README.md** (10 min) - Understand what you have
2. **QUICK_START.md** (5 min) - Deploy it quickly  
3. **Test the system** (10 min) - Try all features
4. **DEPLOYMENT_GUIDE.md** (read as needed) - Deep dive into deployment

### For Deployment:

1. **QUICK_START.md** - Fastest method (Netlify)
2. **DEPLOYMENT_GUIDE.md** - All deployment options
3. **README.md** - User training materials

### For Development/Customization:

1. **FILE_MAP.md** (this file) - Understand structure
2. **js/auth.js** - See core functions
3. **Individual dashboard JS files** - See specific features

---

## 🎯 Where to Find Things

### "How do I deploy?"
→ **DEPLOYMENT_GUIDE.md** or **QUICK_START.md**

### "How does login work?"
→ **js/auth.js** (authenticateUser function)

### "How to add a new feature to user dashboard?"
→ **js/user-dashboard.js**

### "How do the charts work?"
→ **js/technical-dashboard.js** (Chart.js integration)

### "What are the demo accounts?"
→ **README.md** or **SYSTEM_COMPLETE.md**

### "How to troubleshoot?"
→ **DEPLOYMENT_GUIDE.md** (Troubleshooting section)

### "What database tables exist?"
→ **README.md** (Data Storage section)

### "How to export data?"
→ **js/auth.js** (exportToCSV function)

### "How to upload CSV?"
→ **js/warehouse-dashboard.js** (handleFileUpload function)

---

## 💾 Database Tables (Not Files, But Important)

### `users` table
- Stores user accounts
- 5 demo users included
- Fields: id, username, password, full_name, email, role, department, active

### `stock_items` table
- Stores inventory
- 20 sample items included
- Fields: reference, model, category, available_qty, etc.

### `requests` table
- Stores all requests
- Empty initially
- Fields: user_id, item_reference, quantity, status, etc.

---

## 🔗 Dependencies (External Libraries)

All loaded via CDN (no installation needed):

- **Tailwind CSS** - Styling
- **Font Awesome** - Icons
- **Chart.js** - Charts (technical dashboard only)

---

## 🎨 File Relationships Diagram

```
                    index.html (Login)
                         │
            ┌────────────┼────────────┐
            ↓            ↓            ↓
    user-dashboard  warehouse-    technical-
                    dashboard     dashboard
            │            │            │
            └────────────┼────────────┘
                         ↓
                    js/auth.js
                    (Shared by all)
                         │
                         ↓
                 RESTful Table API
                    (Database)
```

---

## 📝 Quick Tips

### Want to customize colors?
→ Edit inline Tailwind classes in HTML files

### Want to add a feature?
→ Edit the appropriate dashboard JS file

### Want to change how login works?
→ Edit `js/auth.js`

### Want to modify charts?
→ Edit `js/technical-dashboard.js`

### Want to add more demo users?
→ Add to users table via database

### Want to test locally?
→ Just open `index.html` in browser

---

## ✅ You're All Set!

You now understand:
- What each file does
- How files work together
- Where to find specific features
- How to navigate the project

**Ready to deploy? Go to QUICK_START.md!** 🚀

---

**Happy warehouse management! 📦✨**
