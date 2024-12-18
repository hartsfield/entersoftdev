# Enterprise Web Applications: A Model For Production

How do enterprise software engineers continuously integrate and deploy (CICD) production web applications? Herein we describe a CICD workflow for enterprise development firms. Engineers should reference this model in understanding the multi-step process necessary for running and maintaining a scalable production-ready web application.

#### Intro: Development -> Staging -> Production

Enterprise web applications require a multi-system environment. Development machines are the computers used by engineers to code and test the pre-release application, and access and deploy the finalized version of it, where it's then sent to a staging server designed to mimic the production environem, tested, and finally deployed to production server cluster(s), where users can access it.

##### Cloud Servers

Firstly, create an account on Google Cloud Platform, and spin up a Linux virtual machine. Once its instantiated, copy the gcloud command used for accessing it remotely via ssh, and paste it into your terminal.

##### Domain and DNS

Now we may purchase our domain name, and configure its DNS records.

    Host        Type   Priority   Data
    @           A      --         33.33.3.33        
    *           A      --         33.33.3.33
    subdomain   CNAME  --         domain-name.com
    www         A      --         33.33.3.33

##### Development Environment


