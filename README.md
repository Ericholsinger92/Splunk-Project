# Splunk-Project

Activity File: Part 1 - Master of the SOC

Each group is playing the role of an SOC analyst at a small company called Virtual Space Industries (VSI), which designs virtual reality programs for businesses.


VSI has heard rumors that a competitor, JobeCorp, may be launching cyberattacks to disrupt VSI's business.


As SOC analysts, you are tasked with using Splunk to monitor against potential attacks on your systems and applications.


Your Networking team has provided you with past logs to help you develop baselines and create reports, alerts, and dashboards.


**You've been provided the following logs:**
- Windows Server Logs - This server contains intellectual property of VSI's next-generation virtual reality programs.
- Apache Server Logs - This server is used for VSI's main public-facing website vsi-company.com.


**Windows Server Logs Instructions and Deliverables**

Load the logs into your Splunk environment.

Analyze the logs and the available fields.


Design the following deliverables to protect VSI from potential attacks by JobeCorp.


**Reports: Design the following reports to assist VSI with quickly identifying specific information.**


**A report with a table of signatures and associated SignatureID.**


This will allow VSI to easily view reports that show the ID number with a specific signature of the Windows activity.

 [![sig-and-sig-id.png](https://i.postimg.cc/kGr05nFn/sig-and-sig-id.png)](https://postimg.cc/dkBHHcxX)



**A report that provides the count and percent of the severity.**


This will allow VSI to quickly know the severity levels of the Windows logs being viewed.

[![severity-report-b4.png](https://i.postimg.cc/g0jFSt2P/severity-report-b4.png)](https://postimg.cc/DS9MmgGC)


**A report that provides a comparison between the success and failure of Windows activities.**

This will show VSI if there is a suspicious level of failed activities on their server.

[![success-failure-report-b4.png](https://i.postimg.cc/7LRvp15J/success-failure-report-b4.png)](https://postimg.cc/Y4QyFWft)




**Alerts: Design the following alerts to notify VSI of suspicious activity:**


Determine a baseline and threshold for hourly level of failed Windows activity.

- Create an alert to trigger when the threshold has been reached.
- The alert should trigger an email to SOC@VSI-company.com.

[![Failed-activity-alert-b4.png](https://i.postimg.cc/wB0ZDXXb/Failed-activity-alert-b4.png)](https://postimg.cc/wtRwpsbh)



**Determine a baseline and threshold for hourly count of the signature: an account was successfully logged on.**
- Create an alert to trigger when the threshold has been reached.
- The alert should trigger an email to SOC@VSI-company.com.

[![account-logged-on-alert.png](https://i.postimg.cc/wvbKYX3s/account-logged-on-alert.png)](https://postimg.cc/wyJ4hsX6)



**Determine a baseline and threshold for hourly count of the signature: a user account was deleted.**
- Design the alert based on the corresponding SignatureID, as the signature name sometimes changes when the Windows system updates.
- Create an alert to trigger when the threshold has been reached.
- The alert should trigger an email to SOC@VSI-company.com.

[![account-deleted-alert.png](https://i.postimg.cc/tTg0cSRj/account-deleted-alert.png)](https://postimg.cc/sBb0QJZ6)




**Visualizations and Dashboards: Design the following visualizations and add them to a dashboard called Windows Server Monitoring:**



- A line chart that displays the different signature field values over time.
- A line chart that displays the different user field values over time.
- A bar, column, or pie chart that illustrates the count of different signatures.
- A bar, column, or pie chart that illustrates the count of different users.
- A statistical chart that illustrates the count of different users.
- One single value visualization of your choice: radial gauge, marker gauge, etc.

[![windows-dash-b4-1.png](https://i.postimg.cc/rm4H3B67/windows-dash-b4-1.png)](https://postimg.cc/DJ25bYwc)
[![windows-dash-b4-2.png](https://i.postimg.cc/bvWM6z5Q/windows-dash-b4-2.png)](https://postimg.cc/Mc0dH8qT)
[![windows-dash-b4-3.png](https://i.postimg.cc/6pHFvVLb/windows-dash-b4-3.png)](https://postimg.cc/PCw6Gw71)





**Apache Web Server Instructions and Deliverables**

Load the logs into your Splunk environment.

Analyze the logs and the available fields.

Design the following deliverables to protect VSI from potential attacks by JobeCorp:


**Reports: Design the following reports to assist VSI with quickly identifying specific information:**


**A report that shows a table of the different HTTP methods (GET, POST, HEAD, etc).
**

This will provide insight into the type of HTTP activity being requested against their web server.

[![HTTP-method-b4.png](https://i.postimg.cc/MZMZKHx8/HTTP-method-b4.png)](https://postimg.cc/7b4rKxfB)



**A report that shows the top 10 domains that referred to VSI's website.
**

This will assist VSI with identifying suspicious referrers.

[![top-10-domains-report-b4.png](https://i.postimg.cc/XqwTGTQ9/top-10-domains-report-b4.png)](https://postimg.cc/dZVWgSM0)




**A report that shows the count of the HTTP response codes.**

This will provide insight into any suspicious levels of HTTP responses.

[![http-response-report-b4.png](https://i.postimg.cc/QNTsZzk8/http-response-report-b4.png)](https://postimg.cc/PNT0m2R9)






**Alerts: Design the following alerts:**



**Determine a baseline and threshold for hourly activity from a country other than the United States.**

- Create an alert to trigger when the threshold has been reached.
- The alert should trigger an email to SOC@VSI-company.com.

[![activity-outside-us-alert.png](https://i.postimg.cc/FzfMrYJC/activity-outside-us-alert.png)](https://postimg.cc/kRm1wXsW)




**Determine an appropriate baseline and threshold for hourly count of the HTTP POST method.**

- Create an alert to trigger when the threshold has been reached.
- The alert should trigger an email to SOC@VSI-company.com.

[![HTTP-post-alert.png](https://i.postimg.cc/RZR4bn1w/HTTP-post-alert.png)](https://postimg.cc/gxnCxjT0)




**Visualizations and Dashboards: Design the following visualizations and add them to a dashboard called Apache WebServer Monitoring.**

- A line chart that displays the different HTTP methods field over time.
- A geographical map showing the location based on the clientip field.
- A bar, column, or pie chart that displays the number of different URIs.
- A bar, column, or pie chart that displays the counts of the top 10 countries.
- A statistical chart that illustrates the count of different user agents.
- One single value visualization of your choice: radial gauge, marker gauge, etc.


[![apache-dashboard-b4-1.png](https://i.postimg.cc/130L3hfS/apache-dashboard-b4-1.png)](https://postimg.cc/LJXyxWtQ)
[![apache-dashboard-b4-2.png](https://i.postimg.cc/63PPmB1r/apache-dashboard-b4-2.png)](https://postimg.cc/DJq5W3h0)
[![apache-dashboard-b4-3.png](https://i.postimg.cc/yNV2JQZZ/apache-dashboard-b4-3.png)](https://postimg.cc/DSMxHc5v)






**Report Analysis for Severity**

- Access the Reports tab and select Yours to view the reports created from Part 1.
- Select the report you created to analyze the different severities.
- Select Edit > Open in Search.
- Take note of the percentages of different severities.
- Change the source from windows_server_logs.csv to "source="windows_server_attack_logs.csv
- Select Save.



**Review the updated results and answer the following question:**

**Did you detect any suspicious changes in severity?**

Before the attack

[![severity-report-b4.png](https://i.postimg.cc/g0jFSt2P/severity-report-b4.png)](https://postimg.cc/DS9MmgGC)

After the attack

[![severity-report-after.png](https://i.postimg.cc/c4GWxcXQ/severity-report-after.png)](https://postimg.cc/3W1V92MR)


Before attack information was 93. High was 6.9
After attack information was 79. High was 20. 



**Report Analysis for Failed Activities**

- Access the Reports tab and select Yours to view the reports created from Part 1.
- Select the report you created to analyze the different activities.
- Select Edit > Open in Search.
- Take note of the failed activities percentage.
- Change the source from windows_server_logs.csv to "source="windows_server_attack_logs.csv.
- Select Save.



**Review the updated results and answer the following question:**


**Did you detect any suspicious changes in failed activities?**
	

Before the attack

[![success-failure-report-b4.png](https://i.postimg.cc/7LRvp15J/success-failure-report-b4.png)](https://postimg.cc/Y4QyFWft)


After the attack

[![success-failure-report-after.png](https://i.postimg.cc/qRCf0tKb/success-failure-report-after.png)](https://postimg.cc/tZyvN42W)


Before the attack failed was 142 events. Success was 4622. 
After the attack failed was 93 events. Success was 5856.




**Now you will review the alerts you created in Part 1 and analyze the results.**



**Alert Analysis for Failed Windows Activity**
- Access the Alerts tab and select Yours to view the alerts created in Part 1.
- Select the alert for suspicious volume of failed activities.
- Select Open in Search.
- Change the source from windows_server_logs.csv to "source="windows_server_attack_logs.csv.


**Review the updated results and answer the following questions:**

[![Failed-activity-alert.png](https://i.postimg.cc/K8FmN5TZ/Failed-activity-alert.png)](https://postimg.cc/HVZGWX3K)

**Did you detect a suspicious volume of failed activity?**
- Yes


**If so, what was the count of events in the hour(s) it occurred?**
- 35 events


**When did it occur?**
- 8am March 25, 2020


**Would your alert be triggered for this activity?**
- Yes


**After reviewing, would you change your threshold from what you you previously selected?**
- No



**Alert Analysis for Successful Logons**

- Access the Alerts tab and select Yours to view the alerts created in Part 1.
- Select the alert of suspicious volume of successful logons.
- Select Open in Search.
- Change the source from windows_server_logs.csv to "source="windows_server_attack_logs.csv.



**Review the updated results, and answer the following questions:**

[![logged-on-alert-succcess.png](https://i.postimg.cc/KjBy7Kvk/logged-on-alert-succcess.png)](https://postimg.cc/H8YKdkMd)


**Did you detect a suspicious volume of successful logons?**
- Yes


**If so, what was the count of events in the hour(s) it occurred?**
- 196

**Who is the primary user logging in?**
- User J


**When did it occur?**
- 11am March 25, 2020


**Would your alert be triggered for this activity?**
- Yes

**After reviewing, would you change your threshold from what you you previously selected?**
- No



**Alert Analysis for Deleted Accounts**
- Access the Alerts tab and select Yours to view the alerts created in Part 1.
- Select the alert of suspicious volume of deleted accounts.
- Select Open in Search.
- Change the source from windows_server_logs.csv to "source="windows_server_attack_logs.csv.


**Review the updated results and answer the following question:**

[![deleted-account-alert-success.png](https://i.postimg.cc/8crY8xqq/deleted-account-alert-success.png)](https://postimg.cc/H8dzXvW2)


**Did you detect a suspicious volume of deleted accounts?**
- Yes, around 5am. Our alert would have caught it. 





**Now you will set up a dashboard and analyze the results.**

**Dashboard Setup**
- Access the Windows Webserver Monitoring dashboard.
- Access each panel you created and complete the following:
- Change the source from: windows_server_logs.csv to source="windows_server_attack_logs.csv.
- Save the dashboard.
- Edit the time on the dashboard to be All Time.


**Dashboard Analysis for Time Chart of Signatures**


**Analyze your new dashboard results and answer the following questions:**

[![windows-dash-after-1.png](https://i.postimg.cc/hGf6bJ2D/windows-dash-after-1.png)](https://postimg.cc/mcWmTrxJ)
[![windows-dash-after-2.png](https://i.postimg.cc/Vks3vZMb/windows-dash-after-2.png)](https://postimg.cc/RN8PbRgM)
[![windows-dash-after-3.png](https://i.postimg.cc/vHtJQw1s/windows-dash-after-3.png)](https://postimg.cc/Vd5GRTBG)



**Does anything stand out as suspicious?**
- The “an attempt was made to reset an account’s password” and “an account was locked out: signature exploded in activity. 


**What signatures stand out?**
- “An attempt was made to reset an account’s password” stood out, as well as “An account was locked out”


**What time did it begin/stop for each signature?**
- “Locked out”: 12am-3am on March 25, 2020
- “Reset password”: 10am-12pm


**What is the peak count of the different signatures?**
- “Reset password”: 1258
- “Locked out”: 896


**Dashboard Analysis for Users**

Analyze your new dashboard results and answer the following questions:


**Does anything stand out as suspicious?**
- Yes, User A and User K has explosions of activity. 


**Which users stand out?**
- User A and User K


**What time did it begin and stop for each user?**
- User A: 12am-3am
- User K: 8am-10am


**What is the peak count of the different users?**
- User A: 984
- User K: 1256



**Dashboard Analysis for Signatures with Bar, Graph, and Pie Charts**

Analyze your new dashboard results and answer the following questions:


**Does anything stand out as suspicious?**
- Yes


**Do the results match your findings in your time chart for signatures?**
- They correspond with the amounts for “Account locked out” and “Attempt to reset password.” 



**Dashboard Analysis for Users with Bar, Graph, and Pie Charts**


Analyze your new dashboard results, and answer the following questions:


**Does anything stand out as suspicious?**
- Yes


**Do the results match your findings in your time chart for users?**
- Yes it matches that there was a lot of activity for Users A and K



**Dashboard Analysis for Users with Statistical Charts**


Analyze your new dashboard results, and answer the following question:


**What are the advantages and disadvantages of using this report, compared to the other user panels you created?**
- You can easily filter from highest to lowest as well as alphabetically. Also you get exact numbers much easier that the more graphical charts. 




**Apache Web Server Logs**


Load the logs in your Splunk environment.
Now you will review the reports you created in Part 1 and analyze the results.


**Report Analysis for Methods**

- Access the Reports tab and select Yours to view the reports created from Part 1.
- Select the report that analyzes the different HTTP methods.
- Select Edit > Open in Search.
- Take note of the percent/count of the various methods.
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt.
- Select Save.


**Review the updated results and answer the following questions:**

[![HTTP-method-after.png](https://i.postimg.cc/pyb6Pqvy/HTTP-method-after.png)](https://postimg.cc/Pvy44bPk)


**Did you detect any suspicious changes in HTTP methods? If so which one?**
- Yes, a big increase in POST


**What is that method used for?**
- It is used to send data to a server




**Report Analysis for Referrer Domains**

- Access the Reports tab and select Yours to view the reports created from Part 1.
- Select the report that analyzes the different referrer domains.
- Select Edit > Open in Search.
- Take note of the different referrer domains.
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt.
- Select Save.


**Review the updated results, and answer the following question:**

[![referer-domains-after.png](https://i.postimg.cc/9FPhrqns/referer-domains-after.png)](https://postimg.cc/XpvhPX3g)


**Did you detect any suspicious changes in referrer domains?**
- Yes before the top 10 domains covered all 10,000 logs. Now it only covers about 4,500 events therefore there are a lot more referrer domains coming in. 




**Report Analysis for HTTP Response Codes**

- Access the Reports tab and select Yours to view the reports created from Part 1.
- Select the report that analyzes the different HTTP response codes.
- Select Edit > Open in Search.
- Take a note of the different HTTP response codes.
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt.
- Select Save.


**Review the updated results and answer the following question:**

[![http-response-after.png](https://i.postimg.cc/G2BR27Wj/http-response-after.png)](https://postimg.cc/k6dzYcXV)



**Did you detect any suspicious changes in HTTP response codes?**
- Yes, 404 error code went from 2.1% to 15%. 




**Now you will review the alerts you created in Part 1 and analyze the results.**


**Alert Analysis for International Activity**

- Access the Alerts tab and select Yours to view the alerts created in Part 1.
- Select the alert of suspicious volume of international activity.
- Select Open in Search.
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt.



**Review the updated results and answer the following questions:**

[![activity-outside-us-after.png](https://i.postimg.cc/ry36hNvB/activity-outside-us-after.png)](https://postimg.cc/rz1Ysxyj)



**Did you detect a suspicious volume of international activity?**
- Yes


**If so, what was the count of the hour it occurred in?**
- 935 events at 10pm March 25, 2020. 


**Would your alert be triggered for this activity?**
- Yes


**After reviewing, would you change the threshold you previously selected?**
- No




**Alert Analysis for HTTP POST Activity**

- Access the Alerts tab and select Yours to view the alerts created in Part 1.
- Select the alert of suspicious volume of HTTP POST activity.
- Select Open in Search.
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt.



**Review the updated results, and answer the following questions:**

[![http-post-after.png](https://i.postimg.cc/3rs8yhJ0/http-post-after.png)](https://postimg.cc/w3k8PSN9)



**Did you detect any suspicious volume of HTTP POST activity?**
- Yes


**If so, what was the count of the hour it occurred in?**
- 1296 events


**When did it occur?**
- 8pm March 25, 2020


**After reviewing, would you change the threshold that you previously selected?**
- No, our alert would have caught it. 





**Now you will set up a dashboard and analyze the results.**


**Dashboard Setup**

- Access the dashboard for Apache Webserver Monitoring.
- Access each panel and complete the following:
- Change the source from: source=apache_logs.txt to source="apache_attack_logs.txt
- Edit the time on the whole dashboard to be All Time.



**Dashboard Analysis for Time Chart of HTTP Methods**


**Analyze your new dashboard results and answer the following questions:**

[![apache-dashboard-after-1.png](https://i.postimg.cc/mDkqjPVZ/apache-dashboard-after-1.png)](https://postimg.cc/PpG2rrB0)
[![apache-dashboard-after-2.png](https://i.postimg.cc/9QH62FX1/apache-dashboard-after-2.png)](https://postimg.cc/LnvCBS1Z)
[![apache-dashboard-after-3.png](https://i.postimg.cc/BQKrR13X/apache-dashboard-after-3.png)](https://postimg.cc/SJm1MRJh)



**Does anything stand out as suspicious?**
- Yes, GET and POST seem to spike. 


**Which method seems to be used in the attack?**
- POST


**At what times did the attack start and stop?**
- 7-9pm on March 25, 2020


**What is the peak count of the top method during the attack?**
- 1296 of POST




**Dashboard Analysis for Cluster Map**


Analyze your new cluster map results and answer the following questions:


**Does anything stand out as suspicious?**
- Yes, a lot of traffic from Ukraine. 


**Which new city, country on the map has a high volume of activity?**
- Kiev, Ukraine. 


**What is the count of that city?**
- 439




**Dashboard Analysis for URI Data**


Analyze your dashboard panel of the URI data and answer the following questions:


**Does anything stand out as suspicious?**
- Yes, the account_logon URI saw a lot of activity. 


**What URI is hit the most?**
- Account_logon


**Based on the URI being accessed, what could the attacker potentially be doing?**
- Trying to log on to accounts, potentially a brute force attack. 

