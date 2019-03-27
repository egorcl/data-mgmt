### Provisioning an Autonomous Database

**Objectives**

-   Learn how to login to the Oracle Cloud Console

-   Learn how to provision a new Autonomous Database

In this section you will be provisioning an ATP database using the cloud
console.

Go to [cloud.oracle.com](https://cloud.oracle.com), click Sign In to sign in
with your Oracle Cloud account.

![](media/53fae2ba1f4d4189a1f915df893f66a6.png)

Enter your Cloud Account Name and click **Next**.

![](media/b2a796ea56d0002761a6ba5b54b37721.png)

Enter your Cloud username and password, and click Sign In. In this example, the
Cloud username is *adw_admin*.

![](media/10c1a3ec2422b16889c3828a0d4438f4.png)

This will bring you to the main cloud page which may differ depending on whether
this cloud account has been used before and the main portal customized. Below
you will see the main screen for a new account, that shows available Guided
Journey’s. From here you can launch different Oracle cloud services. From the
top left select the drop down menu highlighted in red:

![](media/476fa622f064d5dbc257cfc83fa1f01d.png)

Select **Autonomous Transaction Processing** from the drop down menu

![](media/f1d1160d5dc6d38cec36f36fdf2a3eff.png)

This will put you in the main Autonomous Database Service Console (see below).
Any ADB Databases created will be listed here. You can also create and access
databases from this page.

It is possible to use different compartments to separate databases into
different associated groups, we will use the default compartment, so no change
just fyi:

![](media/729b50d8dd835b5a5867a39f7acbe418.png)

Click on the “**Create Autonomous Transaction Processing Database**” button, as
shown below:

![](media/12f390af471dd844bf65511d24a9f413.png)

The following information must be filled in this page:

**Workload Type-** Autonomous Data Warehouse or Autonomous Transaction
Processing

**Compartment** – This can be changed, to organize and isolate databases

**Display Name –** The name of the service displayed

**Database Name –** The name of the actual database

**CPU Core Count –** Number of CPU’s allocated to the database (min 1)

**Storage –** Storage allocated to database in Terabytes (min 1)

**Password –** Database “Admin” user password

**License Type –** Select whether customer is using existing on-premises
database licenses (BYOL) or requires new licences. Customer charge will be based
on selected option

**TAGS –** a metadata system that allows you to organize and track resources
within your tenancy. Tags are composed of keys and values that can be attached
to resources.

After filling fields, click **Create Autonomous Database** which will open up
the screen to complete you database information:

![](media/da8ab67c30a3494ccae9dfea0941ae89.png)

![](media/b07897d4b90d5fa5a49e682d2e896adf.png)

You will be placed on the Database Details page and your database will be in
“**Provisioning**” status. The Database Details page displays more information
about your instance, notice the various menu buttons that help you manage your
new instance.

![](media/9b986ed83288de5714cec3819a1b0aa3.png)

The status will automatically change to “**Available**” when the database is
ready in a few minutes…Your Autonomous database is up and running! Take notice
of the green color of the ATP logo indicating the service is available and
commands to start, stop, terminate, and scale the service.

![](media/644ac70d0a6e719210e8c5d9cb46d570.png)

Now connect to your database, click the Service Console button:

![](media/644ac70d0a6e719210e8c5d9cb46d570.png)

You will be placed in the Service Console page, you will notice there is no
activity displayed because this is a new instance. Select the **Administration**
option from the left:

![](media/767e4fd143629fb88d4ad252287de2f9.png)

On the administration page there are six options:

**Download Client Credentials (Wallet) –** this contains the credentials files
used for connectivity to the instance from client applications, tools

**Set Administrator Password –** used to change the “Admin” account password

**Download Oracle Instant Client –** points to different clients that can be
used to connect to the database (like sql\*plus)

**Set Resource Management Rules –** ATP has pre-created user resource groups,
those can be managed here

**Manage Oracle ML Users –** Notebook development environment that can be used
with ATP

**Send Feedback to Oracle –** email feedback on ATP

![](media/28f102c530dcd46cbcd3716cda916a97.png)
