# 🕸️ WebScraping Project Documentation

This project utilizes a Selenium-based crawler to extract job postings and store them in a MongoDB database.

---

## 0. Describe 2 WebScrappers:
**About 2 WebScrappers:** 
 1.WebScrapingNoFluff, fetch data and parse through HTML pages,
    fetch raw data -> parse to separated jobs -> add skill list into each job
 2.WebScrapingJustJoin, fetch data and parse through http response,
    fetch raw data and parse into jobs with skill list
 3.Job's structure  from 2 websites are same 
**About the job structure:** 
```json

{

"job_title": "string", // Job title extracted from the HTML page

"company_name": "string", // Name of the hiring company

"min_salary": 15000, // Minimum salary (e.g., in Zloty)

"max_salary": 20000, // Maximum salary (e.g., in Zloty)

"location": "string", // City name or "Remote"

"jump_url": "string", // URL to the job detail page

"processed_at": "timestamp", // Time of data extraction

"query_term": "string" // Search keyword (e.g., "business analyst")
  
"must_have_skills": "Array"  //must-have skill set

}
```

**Fetch and store path into:** 
 1.`S5520` -> `DB_final` -> `jobs_raw` and `jobs_processed`
 2.`S5520` -> `DB_final` -> `jobs_processed_jj`





## 1. Critical Operational Steps ⚠️

**When running the code, manual intervention is required for the following browser pop-ups:**

* **Privacy Popup:** You MUST either **Accept** or **Cancel** the privacy consent window.
* **Login Window:** You MUST **Cancel** the login prompt (typically by clicking anywhere outside the window or clicking the close button).

* **You need to restart the kernel to clear the environment variables, to test on remote db and local db**
---

## 2. MongoDB Configuration

The system supports both local and cloud-based database deployments.

* **Local Deployment:** You can run this on your local MongoDB instance.
* **Atlas Configuration:** This configuration is set to connect with remote MongoDB Atlas. 

---







