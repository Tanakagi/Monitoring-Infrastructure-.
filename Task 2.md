# Task 2: Monitoring application logs using CloudWatch Logs

### In this task, I  generated log data on the Web Server and then monitored the logs using CloudWatch Logs.
<img src="" height="80%" width="80%" />
</br>
</br>

<b> I Opened a new web browser tab, and entered the WebServerIP address</br> 
<b>•This took me to the web server Test Page.</br>
<b>•You now generate log data by attempting to access a page that does not exist.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then generated log data by attempting to access a page that did not exist.</br>
<b>• I appended `/start` to the browser URL, and press Enter.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I receive an error message because the page is not found. This generated data in the access logs that are being sent to CloudWatch Logs.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I Kept the tab open in my web browser but returned to the browser tab showing the AWS Management Console.
<b>• From the Services  menu, I selected CloudWatch.</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• In the left navigation pane, I chose Log groups.</br>
<b>• I saw two logs listed: "HttpAccessLog" and "HttpErrorLog".</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected "HttpAccessLog".</br>
<b>• In the "Logs streams" section, I chose the "Log stream" in the table.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I saw a line with my `/start` request with a code of 404, which means that the page was not found.</br>
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

### Creating a metric filter in CloudWatch Logs
<b>I then configured a filter to identify 404 Errors in the log file. This error  normally indicates that the web server is generating invalid links that users are selecting.</br>

<b>• 1. In the left navigation pane, I clicked "Log groups"</br>
<b>• then clicked the check box next to "HttpAccessLog".</br>
<b>• From the **Actions** dropdown menu, I selected "Create metric filter".</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then typed in the  following line into the "Filter Pattern" box:</br> 
<b>This line tells CloudWatch Logs how to interpret the fields in the log data and defines a filter to find lines only with "status_code=404", which indicates that a page was not found.</br>
<b>• In the "Test pattern" dropdown menu section, I selected the EC2 instance id.</br>
<b>• then clicked "Test pattern"</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the Results section, I saw this status code which indicated that the requested page was not found.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the "Create filter name" section, in the "Filter name" box, enter "404Errors"</br>
<b>• In the "Metric details" section, I configured the following information:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then clicked "Create metric filter".</br>
<b>•This metric filter can now be used in an alarm.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

### Create an alarm using the filter

<b>•  In the "404Errors panel", I selected the check box in the top-right corner.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• And Configured the following settings:</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• 1. In the "Notification" section, I configured the following:
<b>•then clicked "Create topic"</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• For "Name and description", I filled in the following settings:</br>
<b>• then clicked "Create alarm"</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I went to the email I entered, looked for a confirmation message, Confirmed subscription.</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• Back in the console, In the left navigation pane, under "CloudWatch".</br>
<b>• I was able to access the webserver to generate log data.</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• I went back to the web page and added a page name after the IP address. I repeated this five times to generate log data.</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b>• I then went back to the AWS console page and waited 2 minutes for the alarm to trigger.</br>
<b>• The graph shown on the CloudWatch page  turned red to indicate that it was in the Alarm state.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then checked my email and received an email with the subject ALARM: "404 Errors".</br>
<img src="" height="80%" width="80%" />
</br>
</br>
