# Task 1: Installing the CloudWatch agent.

### In this task, you use Systems Manager to install the CloudWatch agent on an EC2 instance. You configure it to collect both application and system metrics.

<b>• In the AWS Management Console, I selected Systems Manager.</br> 
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the left navigation pane, I clicked Run Command.</br>
<img src="" height="50%" width="50%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>


<b> I scrolled to the Command parameters section and filled in the following information:</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the Targets section, I selected Choose instances manually, and then under Instances, selected the check box next to Web Server. This configuration installs the CloudWatch agent on the web server.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then viewed the output from the job to confirm that it ran successfully.</br>
<b>•  I then viewed the output from the job to confirm that it ran successfully.</br>
<img src="" height="80%" width="80%" />
</br>
</br>
<b>• Under Targets and outputs, I selected the instance and then clicked View output. </br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then expanded Step 2 - Output instead. and selected this option because the instance I was using was created from a Linux AMI.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>
</br>

<b> I then configured the CloudWatch agent to collect the desired log information. The instance has a web server installed,</br>
so I configured the CloudWatch agent to collect the web server logs and general system metrics.
<b>I stored the configuration file in AWS Systems Manager Parameter Store, which the CloudWatch agent can then retrieve.</br>
</br>

<b>• I selected "Create parameter", This parameter will be referenced when starting the CloudWatch agent.</br>
<b>I then configured the following information:</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b> I added the configurations code under (LINK) "value",</br>
<b> I then examined the above configuration code. which defines the following items to be monitored:</br>
<b>• **Logs:** Two web server log files to be collected and sent to CloudWatch Logs</br>
<b>• **Metrics:** CPU, disk, and memory metrics to be sent to CloudWatch Metrics</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then used another Run Command to start the CloudWatch agent on the web server.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the following commands and clicked enter:</br>
<b>• Before running the commands, I  viewed the definition of the command.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the button next to AWS-ConfigureAWSPackage.</br>
<img src="" height="80%" width="80%" />
</br>
</br>
