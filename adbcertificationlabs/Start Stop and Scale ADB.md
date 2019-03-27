Start, Stop and Scale Autonomous Database
-----------------------------------------

This section outlines the management activities that you would typically perform
on Oracle Autonomous Database. Tasks such as starting and stopping the service
and scaling the service are covered.

### Objectives

-   Start and Stop the ADB service

-   Scale the ADB service

### Lab Steps

### Stopping ATP Service

-   Sign in to your ADB **Service Console** and browse to the **Autonomous
    Database Details** page of your service.

![](media/4dfa4ac3b240a57043d652c5a250c0f1.tiff)

-   Click **Stop** to stop the service.

![](media/fa0b093de39946cdd6d4f4863a2346d0.tiff)

-   Click **Stop** again when prompted for confirmation.

![](media/08e6bb49174fcd940336be0403cfaf19.tiff)

-   The ADB service will take a few seconds to stop. Notice the status of
    **STOPPING**.

![](media/709596e3bb6e9db49549968c4da73a0e.png)

-   When the service is stopped, the status will change to **STOPPED**.

![](media/2ce782e50a4d6b39b25d45ac1838927a.png)

### Starting ADB Service

-   From the **Details** page of your ADB service, click **Start** to start your
    service.

![](media/8d010d4443e21e520d3b3caef21dad12.tiff)

-   Click **Start** again when prompted for confirmation.

![](media/bb799fa52de90f3ec2a0252a1d5fe722.tiff)

-   The ADB service will take a few seconds to start. For example, if you
    provisioned ATP service, you would notice the status of **STARTING** as
    follows:

![](media/9e9691ad671854472cbeaa68b1cbd36c.png)

-   When the service is started, the status will change to **AVAILABLE**.

![](media/425707f4071e4cbea789e93f1a9b87b2.png)

### Scaling ADB Service

-   From the **Details** page of your ADB service, click **Scale Up/Down** to
    scale your service.

![](media/b992b1bfec363a922f8c43d85f7ea5c3.tiff)

-   In the **Scale Up/Down** pop up, modify the **CPU CORE COUNT** to **4** and
    click **Update**.

![](media/4e1479c39b6c4a30a7eca6b13083f72e.png)

-   The ADB service will take a few seconds to scale. Notice the status of
    **SCALING IN PROGRESS**.

-   Note that the ATP square remains green during the scaling process. No
    interruption to the service occurs during all scaling operations.

![](media/951a989e14332e7f1e992a0960d34bc8.png)

-   When the scaling task is complete, the status will change to **AVAILABLE**.

![](media/425707f4071e4cbea789e93f1a9b87b2.png)

-   Note the new **CPU Core Count** is reflected in the service details.

![](media/5026143908836ff57f94388d5d846cc1.tiff)
