# Task 1: Installing the CloudWatch agent.

### In this task, I used Systems Manager to install the CloudWatch agent on an EC2 instance. I configure it to collect both application and system metrics.

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

<b>• In the Targets section, I selected Choose instances manually, and then under Instances, I selected the Web Server. This configuration installs the CloudWatch agent on the web server.</br>
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
<b>I stored the configuration file in the AWS Systems Manager Parameter Store, which the CloudWatch agent can then retrieve.</br>
</br>

<b>• I selected "Create parameter", This parameter will be referenced when starting the CloudWatch agent.</br>
<b>I then configured the following information:</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b> I added the following ([configurations code](https://github.com/Tanakagi/Monitoring-Infrastructure./blob/3346d8344b86179da500444d573350792f8f8980/Parameter%20Store%20configuration%20value%20code.py)) under "value",</br>
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
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then clicked the run command and searched for AmazonCloudWatch-ManageAgent</br>
and clicked the name itself (its link) to Browse through the content of each tab to see how a command document is defined.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I selected the Content tab and scrolled to the bottom to see the script that ran on the target instance.</br>
<b>• The script references the AWS Systems Manager Parameter Store because it retrieves the CloudWatch agent configuration that I defined earlier.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I then returned  to the Run a command tab that I was using earlier.
<b>• I  selected  AmazonCloudWatch-ManageAgent.</br>
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• In the Command parameters section, I configure the following information:
<b>• This configures the agent to use the configuration I previously stored in the Parameter Store.</br>
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
</br>
</br>

<b>• I Waited for the Overall status to change to Success.</br> 
<b>•The CloudWatch agent was running on the instance and was sending log and metric data to CloudWatch.</br>
<img src="" height="80%" width="80%" />
</br>
</br>
