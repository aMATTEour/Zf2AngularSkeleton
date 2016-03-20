Zendframework2 backend and AngularJS frontend basic skeleton
============================================================

Introduction
------------
This skeleton includes Zend2, AngularJS and Doctrine2.
Also included ZendDeveloperTools and Ocramius ocra-service-manager modules for profiling the application.

Installation
------------
### Step 1

Update composer in project folder:

    composer update

### Step 2

Update composer in project folder:

    composer update



Doctrine2 commands
------------
### Generate entity

Run following command in project folder:

    php ./vendor/doctrine/doctrine-module/bin/doctrine-module orm:convert-mapping --namespace="Application\Entity\\" --from-database annotation ./module/Application/src/


### Generate getter/setter in entity

Run following command in project folder:

    php ./vendor/doctrine/doctrine-module/bin/doctrine-module orm:generate-entities ./module/Application/src/ --generate-annotations=true


### Create database table from entity
PostgreSQL: the **GeneratedValue** must be **IDENTITY** such as **@ORM\GeneratedValue(strategy="IDENTITY")**
Run following command in project folder:

    php ./vendor/doctrine/doctrine-module/bin/doctrine-module orm:schema-tool:create



