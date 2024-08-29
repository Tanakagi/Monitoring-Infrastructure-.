# Task 5: Monitoring infrastructure compliance.

### In this task, I activated AWS Config rules to ensure compliance with tagging and Amazon Elastic Block Store (Amazon EBS) volumes.

<b>• On the Services  menu, I selected Config, then Add rule..</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the AWS Managed Rules section in the search field, I configured the following:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the **Configure rule** page, I scrolled down to **Parameters**, and configure the following settings:</br>
<b>• This rule now looks for resources that do not have a **project** tag.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then added a rule that looks for EBS volumes that are not attached to EC2 instances and then clicked save.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I Waited until at least one of the rules has completed evaluation.</br>
<b>• I then selected each of the rules to view the results of the audits.</br>
<b>• Under Resources in scope I selected **Compliant** from the list. I reviewed and noticed that my resources were compliant.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>•  **required-tags:** A compliant EC2 instance (because the Web Server has a **project** tag) and many non-compliant resources that do not have a **project** tag.</br>
<b>• **ec2-volume-inuse-check:** One complaint volume (attached to an instance) and one non-compliant volume (not attached to an instance).</br>
<img src="" height="80%" width="80%" />
</br>
</br>

## End of project.

<b>This was the end of my project as I was able to successfully:</br>
<b>• Create a VPC and secure it using network ACLs and Security groups,</br>
<b>• Launch 2 EC2 instances in a private and public subnet that could communicate with each other,</br>
<b>• Successfully troubleshoot connectivity issues and connect to the internet via my public server.</br>

</br>
</br>
