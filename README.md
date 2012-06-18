# OGM Kitchensink 

## What is it?

ogm-kitchensink is a [OGM](http://www.hibernate.org/subprojects/ogm.html) demo app for [AS 7](http://www.jboss.org/jbossas) based on
[kitchensink](https://github.com/jbossas/quickstart/tree/master/kitchensink)

# Prerequisites

* JDK 6
* [Maven 3](http://maven.apache.org/)
* [Git](http://git-scm.com/)


## How to use it:

* Build:

         $ mvn clean package

* Deploy:

         $ mvn cargo:run

* Running tests (uses Arquillian managed container):

         $ mvn test

## How to deploy on OpenShift Express

* Sign up for OpenShift account at - [https://openshift.redhat.com]([https://openshift.redhat.com])
* Install OpenShift Express command line tools

        $ gem install rhc

* Create OpenShift domain and app

        $ rhc-create-domain -n <domain>
        $ rhc-create-app -a <app> -t jbossas-7.0 --nogit

* Add the git repo created by rhc-create-app as remote

        $ git remote add openshift <repo-url>

* Push to Openshift

        $ git push -f openshift master

* Demo site - http://\<app\>-\<domain\>.rhcloud.com

# Links

* [Hibernate OGM](http://www.hibernate.org/subprojects/ogm.html)
* [AS 7 Command Line Interface](https://community.jboss.org/wiki/CommandLineInterface)
* [Openshift documentation](https://www.redhat.com/openshift/documents)

