# M14 Assignment: Visualizations of the Warehouse 

## Description

For this assignment, you will create a dashboard using the data warehouse
database for the IRS 990 data. Tableau is a Data Visualization platform commonly
used across companies and universities. It is especially geared toward Facts
(Measures) and Dimensions. We will connect to your MySQL RDS instance in the AWS
cloud from Tableau on your laptop using Tableaus Connection features. Then,
using that connection we will recreate the dashboard below.

[](https://www.youtube.com/watch?v=N00g9Q9stBo)The following are optional
readings:

-   [A Brief History of Data
    Visualization](https://www.youtube.com/watch?v=N00g9Q9stBo)

-   [Tableau Data
    Visualization](https://d.docs.live.net/1d1d8bead84ce354/Documents/INFORMATION_ARCHITECTURE_YU/INFORMATION_ARCHITECTURE_YU/02%20Assignments/Assignment_4/Tableau%20Data%20Visualization)

-   [What happens when Data Scientists and Designers Work
    Together](https://hbr.org/2018/03/what-happens-when-data-scientists-and-designers-work-together)

### What you will need?

To complete this assignment, you will need the following:

-   A Tableau Desktop installation

-   MySQL Workbench

-   A publicly accessible MySQL instance in the AWS Cloud

-   The following files downloaded:

    -   ./resources/Money_Finance.png

    -   ./resources/Procurement.png

    -   ./resources/Reporting_dashboard.png

    -   ./resources/Review_Approve.png

    -   ./scripts/contracts_report_no_EIN.sql

## Create Connection and Visualization

Use the database file to create a schema in your own AWS RDS MySQL instance and
connect to your Tableau Desktop instance. We will connect to the reporting
database that we just created, **contracts_report_no_EIN.sql. NOTE: **For
convenience, I have created the contracts_report DDL file with all the data to
load.

The DDL can be found titled **‘contracts_rept_no_EIN..sql”. **Run the script to
recreate the environment and be sure to load the appropriate database. Test that
the database accurately loaded by running a simple select statement.

### Connect Tableau Desktop to AWS RDS

To create a connection to your AWS RDS MySQL instance, you will follow a very
similar process to connecting the MySQL Workbench. Please follow these steps:

-   **Step 1.** Navigate to creating a new connection

-   **Step 2.** Select ‘To a Server’

-   **Step 3.** Search for MySQL

-   **Step 4.** When you click MySQL, you will be prompted for the connection
    properties

-   **Step 5.** Use the connection string information for the instance you have
    created and enter the appropriate information:

    -   Enter the MySQL RDS endpoint as your Server Host

    -   Use the appropriate port for your RDS instance (e.g., ‘3389’)

    -   Enter the database to connect to. We connect to ‘**contracts_repts’ **

    -   Enter your username and password

-   **Step 6.** Once connected you should see the tables appear:

    -   Dim_contracts

    -   Dim_date

    -   Dim_supplier

    -   Fact_contracts

-   **Step 7.** Using these tables, create the appropriate join on the fact
    table using the date, contracts, and supplier primary keys.

-   **Step 8.** Click ‘Update Now’ and you should see your data appear

You can view the
[video](https://github.com/yeshivadataanalytics/M14_Assignment/blob/master/resources/Tableau_Connection.mp4)
in the GitHub to review how to connect to Tableau. Remember you will need to
make sure your IP address is added to the security group to access the MySQL RDS
instance.

## Creating visualizations

For this part of the Assignment, recreate the following graphic and apply filter
on the Year from 1995 to 2019. Your submission should be a Tableau Workbook and
Screenshot. You can find the images uploaded to Canvas to support recreating the
icons and the banner.

![](media/8c8489f0a2675e98feba06612722a770.png)

## Submitting the Assignment

Once you have completed this portion of the Assignment save a screenshot of your
dashboard and your workboard in a zipped packaged and send them to
<brandon.chiazza@yu.edu>. Your file name should look like:
\<\<Group_Name\>\>_M14_Submission
