Using Oracle Machine Learning
-----------------------------

Oracle Autonomous Database includes a built-in, browser-based SQL notebook tool
called **Oracle Machine Learning**. It provides an interactive data analysis
environment where teams can work together to build shared, sophisticated reports
and dashboards. It is perfect for data scientists, SQL report builders and SQL
developers and business analysts.

In this lab you will be using the **Oracle Machine Learning** notebook
application provided with autonomous database.

### Objectives

-   Create OML Users

-   Exploring OML Home Page

-   Run a SQL Statement

-   Sharing Notebooks

### Required Artifacts

-   Please ensure you have provisioned an Oracle **Autonomous Data Warehouse**
    or an **Autonomous Transaction Processing** database.

### Lab Steps

### Sign-In to Autonomous Database Service Console (either ADW or ATP)

-   Sign in to **Oracle Cloud Infrastructure Home Page** using the credentials
    provided and the instructions from an earlier lab.

-   Browse to your **Autonomous Data Warehouse Home** page.

![](media/bb55ec2ed68157baf541ca34d0f7556a.tiff)

-   From the **Autonomous Data Warehouse Home** page, click on the instance name
    to open the **Autonomous Data Warehouse Details** page.

![](media/396382f46478516c70d8983b54dcb2fb.tiff)

-   From the **Autonomous Data Warehouse Details** page, click on **Service
    Console** to sign in to the service console.

![](media/5c8fd28d857b174dce6221e6424cd796.tiff)

-   If prompted to **Sign In**, fill in the following **User** and **Password**
    and click **Sign In**:

    -   Username: **ADMIN**

    -   Password: **\<Password\>** specified during provisioning (e.g.
        Welcome_123\#)

![](media/be583405ef7f35967ea587b76e2b8a87.png)

-   You will be placed in the **Overview** page.

![](media/9eb48ed2bfdf0548c12694fe771d7ed8.png)

### Creating OML Users

-   From the **Autonomous Data Warehouse Service Console**, click on
    **Administration** link in the left menu.

    ![](media/b8c393865a9e11c172604d54e55629e4.tiff)

-   On the service **Administration** page, click **Manage Oracle ML Users**.

    ![](media/646671c78d18946a049c71a8383e26c9.tiff)

-   You will be presented the **Machine Learning User Administration** page.
    This page allows you to manage OML user accounts, i.e. the users that can
    login and use OML notebook application. Click the **Create** button to
    create a new OML user.

>   **Note:** Do not login as the **ADMIN** user for OML as Administrative users
>   cannot login to OML.

![](media/0a125f2e95ec8de4cf78e3a8f0653a6e.tiff)

-   On the **Create User** page, enter the following information and click
    **Create**:

    -   User Name : **omluser1**

    -   First Name : (Optional) \<First Name\>

    -   Last Name : (Optional) \<Last Name\>

    -   Email Address : **\<Your Email\>**

    -   Generate password and email details to the user : **Unchecked** (This
        will allow you to enter a password on this screen, otherwise you will
        get an email with a link to set your password)

    -   Password : **\<Password for OML User\>**

![](media/10211ff948c44dccc039c17cd6136ab8.tiff)

-   Observe the **User Created** message. You should see that user
    **omluser1** is listed in the **Users** section.

    ![](media/583a8baead6a4cfe6986550c33c37c79.tiff)

-   If you supplied a valid email address and **Checked** the **Generate
    password and email details to the user** option, a welcome email should
    arrive within a few minutes in your **Inbox**.

    -   Below is the email which each user receives welcoming them to the OML
        application. It includes a direct link to the OML application for that
        user which they can bookmark.

        ![](media/bd9628b8c59d396abbd95f21528bd612.tiff)

    -   When you click on the link **Access Oracle ML SQL notebook** above, you
        will be asked to set a password for the OML user.

-   Using the same steps, create another user named **omluser2**. 

![](media/bdcbf8ebaeaba9d21e32283957f78843.tiff)

-   You will use these two users later in this lab.

### Sign-In and Explore the OML Home Page

-   Sign-in to OML using the link from the welcome email, or by clicking
    the **Home** button

    ![](media/dcf9e2b3a3a211c611102ff50b00628e.tiff)

    on the top right of Oracle Machine Learning** User Administration**.

    ![](media/b1931f05788dc3c494efa915c31d32b7.tiff)

-   Sign-in using the **omluser1** user.

    ![](media/8f74ef34b444f735b8ab909e4c155e45.tiff)

-   Once you have successfully signed-in to OML the **Oracle Machine Learning**
    home page will be displayed.

    ![](media/166f4c1768f59a822b61e7582fd05ab0.tiff)

-   The grey menu bar at the top of the screen provides links to the main OML
    menus for the application (left corner) and the workspace/project and user
    maintenance on the right-hand side.

    ![](media/336e8e3370264c40b45ffd742f4b7d09.tiff)

-   On the home page the main focus is the **Quick Actions** panel. The icons in
    this panel provide shortcuts to the OML pages for running queries and
    managing your saved queries.

![](media/966792c9b4b5a0cff6a93bde264c8727.tiff)

>   **Key OML Concepts**

>   **What is a Workspace?** A workspace is an area where you can store your
>   projects. Each workspace can be shared with other users so they can
>   collaborate with you. For collaborating with other users, you can provide
>   different levels of permission such as Viewer, Developer and Manager – these
>   will be covered in more detail later in this workshop. You can create
>   multiple workspaces.

>   **What is a Project?** A project is a container for organizing your
>   notebooks. You can create multiple projects.

>   **What is a Notebook?** A notebook is a web-based interface for building
>   reports and dashboards using a series of pre-built data visualizations which
>   can then be shared with other OML users. Each notebook can contain one or
>   SQL queries and/or SQL scripts. Additional non-query information can be
>   displayed using special markdown tags (an example of these tags will be
>   shown later).

>   **Note:** All your work is automatically saved – i.e. there is no **Save**
>   button when you are writing scripts and/or queries.

### Running a SQL Statement

-   From the home page click on **Run SQL Statement** in the **Quick Actions**
    panel to open a new SQL query scratchpad.

    ![](media/bdc5f9f2487989ecf18460a383b24c00.tiff)

-   If this is your first time exploring this link, the notebook server will
    startup.

    ![](media/f2aa88778437f35b3b032fc12ba8e500.tiff)

-   You will be presented the **SQL Query Scratchpad**.

    ![](media/ee6ab8c93f0198a1b74bcb69caa98dee.tiff)

-   The white panel below the title **SQL Query Scratchpad** is an area known as
    **Paragraph**. Within a scratchpad you can have multiple paragraphs. Each
    paragraph can contain one SQL statement or a SQL script.

-   You need to enter the SQL in **SQL Paragraph**. SELECT

    p.prod_category_desc,

    t.calendar_year as year,

    t.calendar_month_desc as Month,

    TRUNC(SUM(amount_sold)) as revenue,

    TRUNC(AVG(SUM(amount_sold)) over (PARTITION BY t.calendar_year ORDER BY
    p.prod_category_desc, t.calendar_month_desc ROWS 2 PRECEDING)) as
    avg_3M_revenue,

    TRUNC(AVG(SUM(amount_sold)) over (ORDER BY p.prod_category_desc,
    t.calendar_month_desc ROWS 5 PRECEDING)) as avg_6M_revenue,

    TRUNC(AVG(SUM(amount_sold)) over (ORDER BY p.prod_category_desc,
    t.calendar_month_desc ROWS 11 PRECEDING)) as avg_12M_revenue

    FROM sh.sales s, sh.times t, sh.products p

    WHERE s.time_id = t.time_id

    AND s.prod_id = p.prod_id

    AND prod_category_desc = 'Electronics'

    GROUP BY p.prod_category_desc, t.calendar_year, calendar_month_desc

    ORDER BY p.prod_category_desc, t.calendar_year, calendar_month_desc;

-   Your screen should now look like this:

    ![](media/1c154bf267f71f837ba29df4950dcb83.tiff)

-   On the top-right, click

    ![](media/133c0cbebe11c55053ce103ada3af5af.tiff)

    (**Run this Paragraph)** to execute the SQL statement.

    ![](media/e4b5fc3dd9e69136be50d8a22408285f.tiff)

-   The results will be displayed in a tabular format as follows:

    ![](media/9071a216e7397c1edc6beec76b567382.tiff)

#### Changing the Report Type

-   Using the report menu, you can change the table to a graph and/or export the
    result set to a CSV or TSV file.

    ![](media/7bd4cf612e1da9c9e99ea068120c3dd8.tiff)

-   When you change the report type to one of the graphs, then a Settings link
    will appear to the right of the menu which allows you to control the layout
    of columns within the graph.

-   Click on the **Bar Chart** icon to change the output to a bar graph (see
    below)

    ![](media/49937653b2b3b7c820049fd4ac322cb3.tiff)

-   Click on

    ![](media/50db2b32340c1dbbea0e8a2754e84731.tiff)

    to unfold the settings panel for the graph.

    ![](media/c3445e54d40b4a6718fde8a3677be245.tiff)

-   To add a column to one of the **Keys**, **Groups** of **Values** panels just
    drag and drop the column name into the required panel.

-   To remove a column from the **Keys**, **Groups** of **Values** panel just
    click on the “x” next to the column name displayed in the relevant panel.

#### Changing the Graph Layout

-   With the graph settings panel visible:

    -   Remove all columns from the both the **Keys** and **Values** panels.

    -   Drag and drop **MONTH** into the **Keys** panel

    -   Drag and drop **REVENUE** into the **Values** panel

    -   Drag and drop **AVG_12M_REVENUE** into the **Values** panel

-   The report should now look like the one shown below.

    ![](media/1b12dba0751cf160ea4354cfe6975258.tiff)

#### Cleanup the Report

-   Click on the Settings link to hide the layout controls.

-   Click on **Hide editor** button which is to the right of the “Run this
    paragraph” button.

    ![](media/1548ebb63cece407811b371eff185cdd.tiff)

-   Now only the output is visible.

    ![](media/9c1564e97e1bfb894d71b7de35ca8a31.tiff)

### Saving the SQL as a New Notebook

-   The SQL Scratchpad in the previous section is simply a default type notebook
    with a system generated name. But we can change the name of the scratchpad
    we have just created SQL Query Scratchpad.

-   Click on the hamburger menu

    ![](media/78f30c8880ae494d3eacdf2ee55f643c.tiff)

    on top left and then click on **Menu** to return to the OML home page.

    ![](media/752d7e46c258b6e4891dc9c2933fcb38.tiff)

-   Notice that in the **Recent Activities** panel there is a potted history of
    what has happened to your SQL scratchpad Notebook.

    ![](media/28c642b4c068423015937657dc83266f.tiff)

-   Click on **Notebooks** in the **Quick Actions** panel.

    ![](media/f6e134bff34a70e10805485269969972.tiff)

-   The **Notebooks** page will be displayed:

    ![](media/ce0642ac2082aca4c70cd2992263988a.tiff)

-   Let’s rename our **SQL Query Scratchpad** notebook to something more
    informative.

-   Click on the row **Notebook** so it gets highlighted and the menu buttons
    above will activate.

    ![](media/c5dfcbae0a95ddaeb7a844775ef5da81.tiff)

-   Click on the **Edit** button to pop-up the settings dialog for this
    notebook.

    ![](media/d680e2d375c83fd0a98d347e398ab744.tiff)

-   Enter the information as shown in the image below (note that the connection
    information is read-only because this is managed by the autonomous
    database). Click **OK** to save your notebook.

    ![](media/0dcf2aa444aa7085f86927a4892d03a2.tiff)

-   You will see that your SQL Query Scratchpad notebook is now renamed to the
    new name you specified.

    ![](media/82e228d9e16c628940cb919b9f081455.tiff)

### Sharing Notebooks

-   By default, when you create a notebook it’s only visible to you. To make it
    available to other users you need to share the workspace containing the
    notebook. You can create new workspaces and projects to organize your
    notebooks for ease of use and to share with other users.

-   To demonstrate the sharing process let’s begin by logging in to OML as our
    second OML (**omluser2**) user and checking if any notebooks are available.

-   Click on your user name in the top right corner (**omluser1**) and select
    **Sign Out**.

    ![](media/61e1b16c60006cfcc1bfe5d48163321a.tiff)

-   Now sign-in as OML user **omluser2** using the password you entered at the
    beginning of this workshop:

    ![](media/5fe079f9cd56abccb38b618740049458.tiff)

-   Notice that you have no activity listed in the **Recent Activities** panel
    on your OML home page and you don’t have any notebooks.

    ![](media/c869a6a37965babf5bc225e233734c39.tiff)

-   **Hint**: Click on the Notebooks link in the Quick Actions panel:

    ![](media/813be625069bd2c6b4b00a39a85ad490.tiff)

-   Logout of OML and sign in back OML as **omluser1**.

| [./media/image46.tiff](./media/image46.tiff) |   | [./media/image47.tiff](./media/image47.tiff) |
|----------------------------------------------|---|----------------------------------------------|


#### Change Workspace Permissions

-   From the OML home page, click on **OML Project (OML Workspace)** link in the
    top right corner on the OML home page to display the workspace-project menu.
    Select **Workspace Permissions**.

    ![](media/0d4acfe03dee74b7c9d83c7c49744525.tiff)

-   The permissions dialog box will appear. In the dialog box next to **Add
    Permissions** text type **OMLUSER2** (use uppercase). Set the permission
    type to **Viewer** (this means read-only access to the workspace, project
    and notebook).

    ![](media/a5599a408d4a73f094e6c3350ffde14f.tiff)

-   Click the Add button to add the user omluser2 as a read-only viewer of the
    workspace.

-   Your form should look like this:

    ![](media/f841e11959269a697d4ef9f90e626dac.tiff)

-   Finally, click the **OK** button.

#### Accessing shared notebooks

-   Now repeat the process you followed at the start of this section and
    sign-out of OML and sign-in to OML again as user omluser2.

-   First thing to note is that the Recent Activities panel below the Quick
    Links panel now shows all the changes user omluser1 made within the
    workspace OML-Workspace.

    ![](media/54bb0c24c87aeba371459b546a3faceb.tiff)

-   As user omluser2 you can now run the Sales Analysis Over Time notebook by
    clicking on the blue-linked text in the Recent Activities panel (note that
    your recent activity will be logged under the banner labelled "Today").

    ![](media/8ebadafb054116eda43598a41fa81f27.tiff)

-   The notebook will now open:

    ![](media/bc4046d45d093678d45ca75bf052e109.tiff)

### Creating and Running SQL scripts

-   Log out from user OMLUSER2 and log in as OMLUSER1.

-   The **Run SQL Statement** link on the home page allows you to run a single
    query in a paragraph. To be able to run scripts you can use the **Create a
    SQL Script** link on the home page.

    ![](media/42492cefb06160f09e04418e6778badd.tiff)

-   A new SQL scratchpad will be created with the **%script** identifier already
    selected, this identifier allows you to run multiple SQL statements.

    ![](media/dd82fc1bf28f623a9480f7bea292bb02.tiff)

-   Next, we are going to use a script shows how to use the SQL pattern matching
    MATCH_RECOGNIZE feature for sessionization analysis based on JSON web log
    files.

-   [Download](https://www.dropbox.com/s/wjzixmv2xzihg1i/oml_sql2.sql?dl=0) the
    OML Script, open the script in your favorite editor and **Copy** the
    contents.

-   Paste the script to the **%script** paragraph:

    ![](media/d8b0dab62befbd63bb2dbfdfeee11dc9.tiff)

-   You can then run the script/paragraph and the output will appear below the
    code that makes up the script.

    ![](media/67d50218891fe3bd632b23404c07cd63.tiff)

-   The result should look something like this:

![](media/1fb84371ceb91de12b0a388ffa6246ca.tiff)
