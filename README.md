App Dev Cloud with JBoss BRMS Install Demo 
==========================================
This demo is to install JBoss BRMS in the Cloud based on leveraging any Red Hat OpenShift container based platform, such as:

 - [Red Hat Container Platform (OCP)](https://github.com/redhatdemocentral/ocp-install-demo)
  
 - [Red Hat Container Development Kit (CDK)](https://github.com/redhatdemocentral/cdk-install-demo)

It delivers a fully functioning containerized JBoss BRMS installation.


Install JBoss BRMS on OpenShift
-------------------------------
1. First ensure you have an OpenShift container based installation, such as one of the followling installed first:

  - [OCP Install Demo](https://github.com/redhatdemocentral/ocp-install-demo)

  - [CDK Install Demo](https://github.com/redhatdemocentral/cdk-install-demo)

  - or your own OpenShift installation.

2. [Download and unzip this demo.](https://github.com/redhatdemocentral/rhcs-brms-install-demo/archive/master.zip)

3. Add products to installs directory.

4. Run 'init.sh' or 'init.bat' file. 'init.bat' must be run with Administrative privileges:
```
   $ ./init.sh 192.168.99.100  # example for OCP.

   $ ./init.sh 10.1.2.2        # example for CDK.
```

5. Login to JBoss BRMS to start developing rules projects (the address will be generated by the init script).

  - OCP example: [http://rhcs-brms-install-demo.192.168.99.100.xip.io/business-central](http://rhcs-brms-install-demo.10.1.2.2.xip.io/business-central) ( u:erics / p:jbossbrms1! )
  
  - CDK example: [http://rhcs-brms-install-demo.10.1.2.2.xip.io/business-central](http://rhcs-brms-install-demo.10.1.2.2.xip.io/business-central) ( u:erics / p:jbossbrms1! )


Notes
-----
This project can be installed on any OpenShift platform, such as the Red Hat Container Development Kit (CDK) or OpenShift Container Platform (OCP). Itis possible to install it on any available installation, just point this installer at your installation by passing an IP of your OpenShift installation:
```
  $ ./init.sh IP"
```

Should your local network DNS not handle the resolution of the above address, giving you page not found errors, you can apply the
following to your local hosts file:

```
$ sudo vi /etc/hosts

# add host for OCP demo resulution
192.168.99.100   rhcs-brms-install-demo.192.168.99.100.xip.io 

# add host for CDK demo resolution.
10.1.2.2   rhcs-brms-install-demo.10.1.2.2.xip.io 
```


Supporting Articles
-------------------
- [Real App Dev in the Cloud with JBoss BRMS Install Demo](http://www.schabell.org/2016/03/real-appdev-in-cloud-jboss-brms-install-demo.html)


Released versions
-----------------
See the tagged releases for the following versions of the product:

- v1.3 - JBoss BRMS 6.3.0 and JBoss EAP 6.4.7 running on any given OpenShift installation.

- v1.2 - JBoss BRMS 6.3.0 and JBoss EAP 6.4.7 running on Red Hat CDK.

- v1.1 - JBoss BRMS 6.2.0.GA-redhat-1-bz-1334704 and JBoss EAP 6.4.4 running on Red Hat CDK.

- v1.0 - JBoss BRMS 6.2.0-BZ-1299002, JBoss EAP 6.4.4 and running on Red Hat CDK using OpenShift Enterprise image. 

![OSE pod](https://github.com/redhatdemocentral/rhcs-brms-install-demo/blob/master/docs/demo-images/rhcs-brms-pod.png?raw=true)

![OSE build](https://github.com/redhatdemocentral/rhcs-brms-install-demo/blob/master/docs/demo-images/rhcs-brms-build.png?raw=true)

![JBoss BRMS](https://github.com/redhatdemocentral/rhcs-brms-install-demo/blob/master/docs/demo-images/jboss-brms.png?raw=true)
