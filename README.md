# Introduction
Cloudbees repo

# Sign-up for Workshop Environment

To make it easier for you to work on the labs, you are provided with pre-provisioned Azure environment. You will receive sign-up link for the lab environment from your instructor.

* Register for the lab environment by providing your information and clicking on **Submit** button.
![alt text](Images/registration.png)

* On the next page, click the **Launch Lab** button.
![alt text](Images/Launch-lab.jpg)

* Wait for the lab environment to be provisioned. Sometimes this can take upto **10 minutes**. Once environment provisioning is complete, you will receive details in email as well as in the browser.
![alt text](Images/environment.jpg)

 > Note: Lab environment is enabled only for specific duration or workshop end time - whichever is earlier. At the end of the allowed time, environment will be self-destructed.
 
 
* Login in azure portal,Launch cloud shell.
![alt text](Images/Launch_cloudshell.jpg)

* In cloud shell click on **advanced settings**
![alt text](Images/advanced_settings.jpg)

* Choose existing RG, create new storage account and file, click on **create storage**
![alt text](Images/storage_account.jpg)

* Now you can see storage is successfully created.
![alt text](Images/storage_created.jpg)

* Run following command Connect to AKS Cluster via CloudShell or AZ CLI.
    ```
    az aks get-credentials --resource-group myAKSCluster --name myAKSCluster
     ```
![alt text](Images/get-credential.jpg)

* Run following command Verify deployments by ensure cjoc-0 pod is running. If status is creating etc, you should wait for about 2 minutes for completion
     ```
    kubectl get pods
     ```
![alt text](Images/get-pods.jpg)

* Run following command to find admin password of jenkins instance.
     ```
    kubectl exec cjoc-0 -- cat /var/jenkins_home/secrets/initialAdminPassword
     ```
![alt text](Images/jenkins-password.jpg)

* Run following command to find DNS name of CJOC, from this command you will get jenkins URL.
     ```
     kubectl get ingress
    ```
![alt text](Images/jenkin-URL.jpg)

* Now access the Jenkins URL in browser.
![alt text](Images/jenkins-url.jpg)

* Enter the Password of jenkins.
![alt text](Images/jenkins-pass.jpg)

* Click on **Request on trial license**.
![alt text](Images/trial-license.jpg)

* Now fill the details for signup-trial and click on **submit**.
![alt text](Images/signup-trial.jpg)

* Select the **Installed suggested plugins**.
![alt text](Images/customize-settings.jpg)

* It will started the all services of cloudbees.
![alt text](Images/started-page.jpg)

* Now you will instance configuration,click on **save&finish**
![alt text](Images/instance-configuration.jpg)

* Ready the operation center, Click on **start using operation center**.
![alt text](Images/ops.jpg)

* It will redirect the jenkins page and create new jenkins-master.
![alt text](Images/jenkins-master.jpg)

* Create new master and click on **go**.
![alt text](Images/new-master.jpg).

* Go with default configuration and click on **save**.
![alt text](Images/jenkins-configuration.jpg)

* Now you can see the jenkins master is created successfully.
![alt text](Images/master-successfully.jpg)

* Now jenkins-master is listed on jenkins dashboard.
![alt text](Images/jen-master.jpg)


