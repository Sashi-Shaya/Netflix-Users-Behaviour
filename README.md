# Netflix User Engagement & Revenue Insights Dashboard

## 📌 Overview
This Power BI dashboard provides deep insights into **Netflix user engagement, subscription trends, and revenue optimization opportunities**. Leveraging **AI-driven insights**, the dashboard enables data-driven strategies to **enhance customer satisfaction, boost engagement, and maximize revenue**.

## 🔍 Problem Statement
Netflix faces challenges in **user engagement, churn reduction, and revenue optimization**. By understanding subscription trends and user behaviors, this dashboard helps identify:
- Hidden revenue opportunities
- Engagement optimization strategies
- Churn reduction methods through AI-driven insights

## 📊 Steps Followed
### **Data Processing & Cleaning**
1️⃣ **Loaded** dataset (CSV) into Power BI Desktop.
2️⃣ Opened **Power Query Editor** → Enabled "Column Distribution", "Column Quality", and "Column Profile" to assess data health.
3️⃣ Changed **column profiling settings** to analyze the entire dataset (not just 1,000 rows).
4️⃣ Verified **no missing values or errors** across columns.

### **Dashboard Design & Visualization**
5️⃣ Selected **canvas background** under "Format Page" settings.
6️⃣ Added **Five Key Card Visuals**:
   - Total Subscribers
   - Total Revenue Generated
   - Active Users
   - Inactive Users
   - Revenue Per User
7️⃣ Created **Four Bar Charts** to visualize active vs. inactive users.
8️⃣ Calculated **Active User Rate** metric.
9️⃣ Designed a **title box** for better dashboard readability.

### **Measure Creation (DAX Calculations)**
🔹 **Total Subscribers:**
```DAX
Total Subscriber = DISTINCTCOUNT('Netflix Userbase'[User ID])
```
🔹 **Revenue Generated:**
```DAX
Generated Revenue = CALCULATE(SUM('Netflix Userbase'[Monthly Revenue]), 'Netflix Userbase'[Active / Inactive] = "Active")
```
🔹 **Active Users:**
```DAX
Active Users = CALCULATE(COUNTROWS('Netflix Userbase'), 'Netflix Userbase'[Active / Inactive] = "Active")
```
🔹 **Inactive Users:**
```DAX
Inactive Users = CALCULATE(COUNTROWS('Netflix Userbase'), 'Netflix Userbase'[Active / Inactive] = "Inactive")
```
🔹 **Revenue Per User:**
```DAX
Average Revenue = [Generated Revenue] / [Active Users]
```

---

## 📈 Key Business Insights & AI-Driven Recommendations

### **1️⃣ Revenue Leakage from Inactive Users**
🔸 **74.43% of subscribers (1,822 users) are inactive** but have paid for the service before.
🔸 If reactivated, **revenue per user could double or triple without acquiring new users**.
✅ **Recommendation:** Implement an **AI-powered re-engagement system** with personalized content recommendations.

### **2️⃣ Subscription Tier Optimization**
🔹 **67.46% of users** are on Standard & Premium plans, while **33.1% remain on Basic**.
🔹 Small pricing gap between **Standard & Premium leads to fewer upgrades**.
✅ **Recommendation:** Offer **Premium trial periods** for Standard users and **AI-driven value comparisons** at renewal.

### **3️⃣ Mid-Year Engagement Drop**
📉 Engagement peaks in **July-September** but **drops sharply toward year-end**.
🔍 **Seasonal Viewing Insight:** Summer breaks drive high engagement, while holidays distract users.
✅ **Recommendation:** Introduce **"End of Year Retention Bundles"** to sustain engagement post-summer.

### **4️⃣ Age-Based User Behavior**
👤 **40-50 age groups** engage the most, while **50-55 engage the least**.
🔍 **Barriers for Baby Boomers:**
   - Complex UI navigation
   - Lack of personalized content
   - Digital literacy challenges
✅ **Recommendation:**
   - Develop a **"Senior-Friendly Mode"** with simplified UI.
   - Introduce **Guided Streaming Onboarding** for 50+ users.
   - Launch **family plans** to encourage younger members to assist older viewers.

### **5️⃣ Gender-Based Subscription Strategy**
👨 **502 males** vs. 👩 **355 females** – a **male-heavy user base**.
🔍 Women show **higher engagement per subscriber**, indicating potential for targeted retention efforts.
✅ **Strategic Moves:**
   - Develop **female-focused content promotions** (e.g., dramas, reality shows).
   - Offer **"Family & Shared Plans"** to attract more female users.

---

## 🚀 Impact & Business Value
🔹 **Improved user engagement & reduced churn** through AI-driven recommendations.
🔹 **Optimized pricing & subscription strategies** for revenue maximization.
🔹 **Targeted marketing & retention initiatives** based on gender, age, and engagement behavior.
🔹 **Informed decision-making** with data-driven insights on user activity and revenue trends.

📌 *This dashboard empowers Netflix to make smarter, AI-powered decisions that drive growth, customer retention, and revenue expansion.* 🚀

