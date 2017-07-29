# Ubuntu Server Setup (16.04 LTS)
Basic setup for java web server for Ubuntu 16.04 LTS

## Tomcat 8
1. Install Tomcat Server
>
> sudo apt-get install tomcat8
>
2. Install Tomcat Manager, Docs
>
> sudo apt-get install tomcat8-admin, tomcat8-docs
>
3. Setup admin user

    3.1 open tomcat user file
    > sudo vi /var/lib/tomcat8/conf/tomcat-users.xml

    3.2 add user and assign role
    > `<role rolename="manager-gui" />`
    >
    > `<role rolename="manager-script" />`
    >
    > `<role rolename="manager-jmx" />`
    >
    > `<role rolename="manager-status" />`
    >
    > `<role rolename="admin" />`
    >
    > `<user username="admin" password="password" roles="admin,manager-gui,manager-script"/>`
