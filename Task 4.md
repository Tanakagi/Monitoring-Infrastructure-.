# Task 4: Creating real-time notifications.

### In this task, I created a real-time notification that informed me when an instance is stopped or terminated.
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/20fc11aaf011a443fdd62e63c54204015574b0d5/Project%20Images/Image%2056.png" height="80%" width="80%" />
</br>
</br>

<b>• In the left navigation pane I expanded  "Events", then "Rules".
<b>• I selected "Create rule".</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/20fc11aaf011a443fdd62e63c54204015574b0d5/Project%20Images/Image%2057.png" height="80%" width="80%" />
</br>
</br>

<b>• In the Event Source section, I configure the following settings:</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/ae57f0186edf14b51d36ea74404722dad0b3e3d2/Project%20Images/Image%2058.png" height="80%" width="80%" />
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/ae57f0186edf14b51d36ea74404722dad0b3e3d2/Project%20Images/Image%2059.png" height="80%" width="80%" />
</br>
</br>

<b>• In the Targets section on the right, I configured the following settings, then Created the rule:</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2060.png" height="80%" width="80%" />
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2061.png" height="80%" width="80%" />
</br>
</br>

### Configuring real-time notification
<b> **I configured Amazon Simple Notification Service (Amazon SNS) to send real-time notifications to my email address.**</br>


<b>• On the Services  menu, I selected Simple Notification Service, then Topics.</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2062.png" height="80%" width="80%" />
</br>
</br>

<b>•. I clicked the link in the "Name" column.</br>
<b>• I  saw a single subscription associated with my email address. This is the Topic I configured in Task 2.</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2063.png" height="80%" width="80%" />
</br>
</br>

<b>• I went to EC2 Instance page and then Stopped the webserver instance.</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2064.png" height="80%" width="80%" />
</br>
</br>

<b>• I then received an email with details about the instance that was stopped.</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2065.png" height="80%" width="80%" />
</br>
</br>

<b>• In the Targets section on the right, I configured the following settings, then Created the rule:</br>
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/5c501dcc0cd355cc0b76869cf23700587030c069/Project%20Images/Image%2066.png" height="80%" width="80%" />
<img src="https://github.com/Tanakagi/Monitoring-Infrastructure./blob/6cde22bf1ad72845d1c90b5daf1fe8c5e4e05971/Project%20Images/Image%2067.png" height="80%" width="80%" />
</br>
</br>
