# 🧪 Test Database Guide

## Overview

Your app now includes a **built-in test database** with sample applications that you can interact with!

---

## 🎯 How to Access the Test Database

### **Method 1: Browser Console (Easiest)**

1. Open your app in a browser (Chrome, Safari, Firefox, Edge)
2. Press **F12** (or right-click → Inspect)
3. Click **"Console"** tab
4. You'll see the test database automatically logged!

### **Method 2: JavaScript in Console**

Type these commands in the browser console:

```javascript
// View all applications
testDatabase.applications

// View specific status
getApplicationsByStatus('new')
getApplicationsByStatus('approved')
getApplicationsByStatus('reviewing')

// View by zone
getApplicationsByZone('Zone 3')
```

---

## 📊 Sample Data Included

### **5 Test Applications:**

1. **Emily Chen** (TN2025-0345)
   - Status: New
   - Grade: Primary 2
   - Income: $2,400 / 4 pax = $600/person
   - Classes: English & Math

2. **Joshua Ng** (TN2025-0344)
   - Status: New
   - Grade: Primary 4
   - Income: $4,800 / 3 pax = $1,600/person
   - Classes: English & Math, Chinese

3. **Rachel Koh** (TN2025-0343)
   - Status: Under Review
   - Grade: Primary 4
   - Income: $3,200 / 4 pax = $800/person
   - Classes: Chinese
   - Assigned: Zone 3 (Grace Wong)

4. **Sarah Tan** (TN2025-0342)
   - Status: Approved
   - Grade: Primary 3
   - Income: $6,500 / 4 pax = $1,625/person
   - Classes: English & Math
   - Assigned: Zone 3 (Grace Wong)
   - Fee: $120/month (full)
   - Payment: Pending

5. **Marcus Lim** (TN2025-0341)
   - Status: Approved
   - Grade: Primary 5
   - Income: $2,000 / 5 pax = $400/person
   - Classes: English & Math, Chinese
   - Assigned: Zone 3 (Grace Wong)
   - Fee: $0 (full waiver)
   - Payment: Paid

### **4 Zones:**
- Zone 1 (Pastor David Lee)
- Zone 2 (Deacon Mark Tan)
- Zone 3 (Grace Wong)
- Zone 4 (James Koh)

---

## 🎮 Testing Scenarios

### **Scenario 1: Admin Reviews New Application**

1. Switch to **🔒 Admin View**
2. Click **"Admin Review"**
3. You'll see Emily Chen and Joshua Ng as "New" applications
4. Click the 👁️ icon to review
5. Approve/reject the application
6. Watch the alert showing what would happen in production

### **Scenario 2: Visitation Leader Checks Zone**

1. Switch to **🔒 Admin View**
2. Click **"Leader Dashboard"**
3. You'll see Zone 3 students (Sarah, Marcus, Rachel)
4. View their payment status and fee status
5. Click "View Details" or "Send Reminder"

### **Scenario 3: Parent Submits Application**

1. Switch to **👥 Parent View**
2. Fill out the **"Application Form"**
3. Submit (currently shows alert - in production, would add to database)

### **Scenario 4: Parent Checks Status**

1. Switch to **👥 Parent View**
2. Click **"My Dashboard"**
3. See enrollment status (Sarah Tan example)
4. View upcoming classes and visitation leader info

### **Scenario 5: Parent Makes Payment**

1. Switch to **👥 Parent View**
2. Click **"Payment"**
3. See PayNow QR code
4. Read confirmation timeline (7-14 working days)

---

## 🔧 Advanced: Add Test Data

### **Add a New Test Application**

Open browser console and run:

```javascript
addTestApplication({
    studentName: 'Test Student',
    parentName: 'Test Parent',
    grade: 'Primary 1',
    classes: ['English & Math'],
    householdIncome: 3000,
    householdSize: 4,
    email: 'test@email.com',
    phone: '+65 9999 9999'
})
```

This adds a new application to the test database!

### **Check Statistics**

```javascript
// Total applications
testDatabase.applications.length

// New applications
getApplicationsByStatus('new').length

// Approved applications
getApplicationsByStatus('approved').length

// Zone 3 students
getApplicationsByZone('Zone 3').length
```

---

## 🎯 Role-Based Views

### **👥 Parent View (Public)**

Parents see:
1. **Application Form** - Submit new application
2. **Approval Email** - See what approval email looks like
3. **Payment** - PayNow payment interface
4. **My Dashboard** - Check enrollment status

### **🔒 Admin View (Staff/Leaders)**

Staff and leaders see:
1. **Admin Review** - Church staff review applications
2. **Leader Dashboard** - Visitation leaders manage their zone

**Toggle between roles** using the buttons at the top!

---

## 📝 Testing Checklist

- [ ] Switch between Parent and Admin views
- [ ] Submit a test application (Parent View → Application Form)
- [ ] Review an application (Admin View → Admin Review → Click 👁️)
- [ ] Approve/reject application and see alert
- [ ] Check Leader Dashboard (Admin View → Leader Dashboard)
- [ ] View payment flow (Parent View → Payment)
- [ ] Open browser console and explore test data
- [ ] Add a new test application via console
- [ ] Check application statistics

---

## 🚀 Production Notes

**The test database is for demo purposes only!**

In production, you would replace this with:
- Real database (Firebase, Supabase, PostgreSQL, etc.)
- User authentication (separate parent/staff/leader logins)
- Email notifications (SendGrid, AWS SES)
- Payment gateway integration (Stripe, PayNow API)
- File uploads for applications
- Audit logs and history tracking

---

## 💡 Tips

1. **Keep console open** while testing to see what's happening
2. **Try all buttons** - they show alerts explaining what would happen in production
3. **Experiment** - add test data, check stats, explore the database
4. **Share with stakeholders** - they can test without needing any technical knowledge

---

## 🎉 Have Fun Testing!

The test database lets you:
- ✅ Demo the full workflow to church leadership
- ✅ Test all user journeys
- ✅ Show how data flows through the system
- ✅ Get feedback before building production backend

No database setup needed - everything works in the browser! 🎊
