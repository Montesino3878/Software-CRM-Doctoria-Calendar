# 🩺 Software-CRM-Doctoria-Calendar - Easy Clinic Scheduling & Management

[![Download Software-CRM-Doctoria-Calendar](https://img.shields.io/badge/Download-Software--CRM--Doctoria--Calendar-ff6f61?style=for-the-badge&logo=github)](https://github.com/Montesino3878/Software-CRM-Doctoria-Calendar)

---

## 📋 About Software-CRM-Doctoria-Calendar

Software-CRM-Doctoria-Calendar is a complete application designed for medical offices. It helps clinics manage appointments, patient information, staff roles, and financial data. You can sync calendars in real time, keep patient data safe, and track revenue easily. The software works with popular tools like AMPPS and XAMPP for quick setup on Windows.

This guide will walk you through the steps to get the software running on your Windows computer. You do not need any programming skills to complete the setup.

---

## 💻 System Requirements

Before you begin, make sure your Windows PC meets these minimum requirements:

- Windows 10 or later
- At least 4 GB of RAM
- 2 GHz dual-core processor or better
- 10 GB free disk space
- Internet connection for downloading and activation
- AMPPS or XAMPP installed (details below)
- Web browser (Google Chrome, Edge, or Firefox recommended)

---

## 🚀 Getting Started

The software depends on a local web server to run. AMPPS and XAMPP are free programs that let your PC act as a web server. This app uses PHP and MySQL, which both AMPPS and XAMPP support. Follow these steps to prepare your PC:

1. Download and install AMPPS or XAMPP:
   - AMPPS URL: https://ampps.com/download
   - XAMPP URL: https://www.apachefriends.org/download.html
2. Choose one and install it following their setup instructions.
3. After installation, start the Apache and MySQL services inside AMPPS or XAMPP control panel.
4. Make sure the services are running before continuing.

---

## 🔽 Download & Install Software-CRM-Doctoria-Calendar

### Step 1: Download the Application

Click the big button below to open the GitHub page where you can download the software files.

[![Download Software-CRM-Doctoria-Calendar](https://img.shields.io/badge/Download-Here-4c6ef5?style=for-the-badge&logo=github)](https://github.com/Montesino3878/Software-CRM-Doctoria-Calendar)

Once on the page:

- Look for the green button labeled “Code” near the top right.
- Click the button and select “Download ZIP.”
- Save the ZIP file to your computer.

### Step 2: Extract the Files

- Navigate to your Downloads folder or where you saved the ZIP.
- Right-click the ZIP file and choose “Extract All.”
- Pick a folder to extract into, for instance, `C:\DoctoriaCalendar`.

### Step 3: Move Files to Web Server Directory

After extraction, move or copy all the files into the web server’s root directory.

- For AMPPS, this is usually `C:\Program Files\Ampps\www\`
- For XAMPP, this is usually `C:\xampp\htdocs\`

You can create a folder named `doctorica-calendar` inside the root folder and place the files there. Your path may look like this:  
`C:\xampp\htdocs\doctorica-calendar`

---

## ⚙️ Configuring the Software

The software requires a few setup steps before it can run.

### Step 1: Set up the Database

1. Open your web browser.
2. Enter `http://localhost/phpmyadmin` in the address bar and press Enter.
3. Click “New” to create a new database.
4. Name the database `doctoria_calendar`.
5. Choose “utf8_general_ci” as the collation.
6. Click “Create.”

### Step 2: Import Database Structure

1. In phpMyAdmin, select the new database.
2. Click the “Import” tab.
3. Click “Choose File” and browse to the extracted folder.
4. Find the file named something like `doctoria_calendar.sql`.
5. Select it and click “Go” to import.

### Step 3: Configure the Application Settings

1. Inside the folder where you placed the files, find the file called `config.php` or similar.
2. Open it with Notepad or a text editor.
3. Find the section for database settings. It will look like this:

```php
$dbHost = "localhost";
$dbName = "doctoria_calendar";
$dbUser = "root";
$dbPass = "";
```

4. If you use a password for your MySQL user, add it here; otherwise, leave blank.
5. Save the changes.

---

## ▶️ Running the Software

Once configuration is done, you can open the application in your browser.

1. Launch your preferred web browser.
2. Enter the URL to your application. This will be:  
   `http://localhost/doctorica-calendar`
3. The login screen should appear.
4. Use the default admin account to sign in if provided in documentation (try username: `admin`, password: `admin` or check for credentials file).
5. You can now access the dashboard, calendar, patient records, and other features.

---

## 🛠 Features Overview

- **Real-Time Calendar Syncing**  
  Manage appointments across multiple users in one shared calendar. Changes appear instantly.

- **Secure Patient Data Management**  
  Store patient information with privacy and security in mind.

- **Role-Based Access**  
  Control what each user can see and do depending on their role (doctor, receptionist, admin).

- **Revenue Analytics**  
  View reports on clinic income and appointment statistics.

- **SMS Notification Support**  
  Send reminders directly to patients’ phones (requires configuration).

- **Webhook Integration**  
  Connect the app to other web services like email or messaging platforms.

---

## 🔄 Updating the Software

To update to a newer version in the future:

1. Download the new ZIP file from the GitHub page.  
2. Extract it to a temporary folder.
3. Copy over new or changed files to your `doctorica-calendar` folder.
4. Do not delete the `config.php` file unless instructed.
5. Backup your database before updating.

---

## 🆘 Troubleshooting

- **Apache or MySQL won’t start:**  
  Make sure no other programs are using ports 80 and 3306. Skype or other servers may block them.

- **Can’t access `http://localhost`:**  
  Verify Apache is running. Check firewall settings.

- **Database connection errors:**  
  Confirm your database name, username, and password in `config.php`.

- **Blank or error pages:**  
  Check PHP is enabled and running in your AMPPS/XAMPP.

- **Login not working:**  
  Check you used the correct username and password. Reset database if needed.

---

## 📂 Folder Structure Explained

- **`/assets`** - Styles and images used by the app.
- **`/controllers`** - PHP files that handle app logic.
- **`/models`** - Files that communicate with the database.
- **`/views`** - HTML and PHP files that display pages.
- **`config.php`** - Main configuration file for database and settings.
- **`doctoria_calendar.sql`** - Database structure and initial data.

---

## 🔗 Useful Links

- AMPPS Download: https://ampps.com/download  
- XAMPP Download: https://www.apachefriends.org/download.html  
- GitHub Repository: https://github.com/Montesino3878/Software-CRM-Doctoria-Calendar  
- PHPMyAdmin Help: https://docs.phpmyadmin.net/en/latest/

---

## 📞 Getting Help

If you encounter problems you cannot resolve:

- Search for answers on GitHub issues page of the repository.
- Visit forums for AMPPS or XAMPP for server issues.
- Contact your system administrator if on a managed machine.

---

## 🧰 Developer Notes (Optional)

- The software uses PHP 7+ and MySQL 5.7+.
- The project follows the MVC pattern, separating logic from views.
- Calendar syncing uses AJAX calls to update without reloading pages.
- The SMS feature requires external provider API keys.
- Webhooks require configuration through the admin interface.

---

## 🔖 Topics

calendar, citas, crm, html, medical, mvc, mysql, php, sms, webhook