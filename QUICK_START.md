# 🚀 Quick Start Guide
## Get Your Warehouse System Running in 5 Minutes!

---

## Step 1: Deploy Online (Required for Multi-User)

### Fastest Method: Netlify (Drag & Drop)

1. **Go to**: [netlify.com](https://www.netlify.com)

2. **Sign Up**: Click "Sign up" (free forever)

3. **Deploy**:
   - Click "Add new site" → "Deploy manually"
   - Drag your entire project folder into the box
   - Wait 30 seconds

4. **Get URL**:
   - Netlify gives you: `random-name-12345.netlify.app`
   - This is your live website!

5. **Share**:
   - Copy the URL
   - Send to all warehouse users
   - Everyone can now access it!

**⏱️ Time: 3 minutes**

---

## Step 2: First Login

1. **Open the URL** in your browser

2. **Login as Admin**:
   ```
   Username: admin
   Password: admin123
   ```

3. **You're in!** You can see the admin dashboard

---

## Step 3: Upload Stock Data

1. **From Admin Dashboard**, switch to **Warehouse Manager view** OR logout and login as:
   ```
   Username: warehouse
   Password: warehouse123
   ```

2. **Click** "Stock Management" tab

3. **Upload your Parts.csv**:
   - Click the upload area
   - Select your CSV file
   - Wait for import (shows progress)

4. **Done!** Your stock is now in the system

---

## Step 4: Test the Workflow

### A. Submit a Request (as User)

1. **Logout** and login as:
   ```
   Username: user1
   Password: user123
   ```

2. **Search for an item**:
   - Type in the search box
   - Select an item

3. **Submit request**:
   - Enter quantity
   - Write reason
   - Click "Submit Request"

### B. Approve Request (as Manager)

1. **Logout** and login as:
   ```
   Username: warehouse
   Password: warehouse123
   ```

2. **See pending request**:
   - It appears in "Pending Requests" tab

3. **Approve it**:
   - Add comments (optional)
   - Click "Approve"

### C. View Report (as Technical Manager)

1. **Logout** and login as:
   ```
   Username: technical
   Password: technical123
   ```

2. **See the dashboard**:
   - View statistics
   - See charts
   - View detailed table
   - Export report

---

## Step 5: Add Your Team

### Method 1: Use Existing Accounts

Share these credentials with your team:

**For regular warehouse workers:**
```
Username: user1, user2
Password: user123
```

**For warehouse managers:**
```
Username: warehouse
Password: warehouse123
```

**For technical/reporting managers:**
```
Username: technical
Password: technical123
```

### Method 2: Add New Users

Currently, new users must be added to the database manually. Contact me to add more users with format:
```javascript
{
  username: "newuser",
  password: "newpassword",
  full_name: "New User Name",
  email: "user@email.com",
  role: "user",  // or warehouse_manager, technical_manager
  department: "Workshop"
}
```

---

## ✅ You're Done!

Your system is now:
- ✅ Live on the internet
- ✅ Accessible from any laptop
- ✅ Supporting multiple users
- ✅ Ready to use!

---

## 📱 Access from Any Device

**Desktop/Laptop:**
- Just open the URL in any browser

**Mobile Phone:**
- Open the URL in mobile browser
- Add to home screen for quick access
- Works perfectly on phones!

**Tablet:**
- Same as mobile
- Great for warehouse floor use

---

## 🔐 Security First!

### Change Passwords Immediately

**Important:** Change all default passwords before sharing with your team!

Contact me to update passwords in the database.

---

## 🆘 Troubleshooting

### "Can't find the URL"
- Check your Netlify dashboard
- Look for "Published at: [URL]"

### "Login not working"
- Check username and password spelling
- Make sure caps lock is off
- Try refresh the page

### "Stock items not showing"
- Make sure CSV was uploaded successfully
- Click refresh button
- Check CSV file format matches Parts.csv

### "Users can't access"
- Share the FULL URL including `https://`
- Example: `https://mywarehouse.netlify.app`
- NOT: `mywarehouse.netlify.app` (missing https://)

---

## 📞 Need Help?

See complete guides:
- **README.md** - Full documentation
- **DEPLOYMENT_GUIDE.md** - Detailed deployment options

---

## 🎯 Quick Reference

### URLs to Remember

**Your Website**: `https://[your-name].netlify.app`  
**Netlify Dashboard**: `https://app.netlify.com`

### Demo Accounts

| Role | Username | Password |
|------|----------|----------|
| Admin | admin | admin123 |
| Manager | warehouse | warehouse123 |
| Technical | technical | technical123 |
| User | user1 | user123 |

### Main Features

- 📤 Upload CSV stock data
- 🔍 Search items
- ✍️ Submit requests
- ✅ Approve/reject requests
- 📊 View analytics
- 📥 Export reports

---

## 🎉 Success!

**Your warehouse system is live and ready!**

Share the URL with your team and start managing your stock efficiently! 📦✨

---

**Total Setup Time: 5-10 minutes**  
**No technical knowledge required**  
**Works immediately after deployment**
