---
layout: default
title: On Prem Setup SQL Server 2016
---
<div class="alert alert-success" role="alert"> This page describes the 
<strong>
{{ site.onp_text }}
</strong>
solution.
</div> 

## On Prem: Setup SQL Server 2016 
--------------------------

<div class="row">
    <div class="col-md-6">
        <div class="toc">
            <li><a href="#prepare-your-sql-server-2016-installation">Prepare your SQL Server 2016 Installation</a></li>
            <li><a href="#set-up-logins-in-sql-server">Set up logins in SQL Server</a></li>
            <li><a href="#ready-to-run-code">Ready to Run Code</a></li>
        </div>
    </div>
    <div class="col-md-6">
        The instructions on this page will help you to add this solution to your on premises SQL Server 2016.  
        <p>
        If you instead would like to try this solution out on a virtual machine, visit the <a href="http://aka.ms/loanchargeoffsql">Cortana Intelligence Gallery</a> and use the Deploy button.  All the configuration described below will be done for you, as well as the initial deployment of the solution. </p>
    </div>
</div>

## Prepare your SQL Server 2016 Installation
-------------------------------------------

The rest of this page assumes you are configuring your on premises SQL Server 2016 for this solution.

If you need a trial version of SQL Server 2016, see [What's New in SQL Server 2016](https://msdn.microsoft.com/en-us/library/bb500435.aspx) for download or VM options. 

For more information about SQL server 2016 and R service, please visit: <a href="https://msdn.microsoft.com/en-us/library/mt604847.aspx">https://msdn.microsoft.com/en-us/library/mt604847.asp</a>

Complete the steps in the Set up SQL Server R Services (In-Database) Instructions. The set up instructions file can found at  <a href="https://msdn.microsoft.com/en-us/library/mt696069.aspx" target="_blank"> https://msdn.microsoft.com/en-us/library/mt696069.aspx</a>

### Set up logins in SQL Server
If you are administering your own server and want to add a user to run the code of this solution, use the steps below.

1. Complete SQL Server 2016 R Services instruction in https://msdn.microsoft.com/en-us/library/mt696069.aspx
2. Check out code from Github - https://github.com/Microsoft/r-server-loan-chargeoff 
3. Create a user login - refer to createuser.sql from code in github
4. Login as created user and create a database
5. Run power shell script named Loan_ChargeOff.ps1 from SQLR folder from github

### Ready to Run Code 
---------------------

You are now ready to run the code for this solution.  

* Typically a data scientist will create and test a predictive model from their favorite R IDE, at which point the models will be stored in SQL Server and then scored in production using Transact-SQL (T-SQL) stored procedures. 
You can follow along with this by following the <a href="Typical.html">Typical Workflow.</a>.

* If you’re just interested in the outcomes of this process, we have created a fully automated solution that loads the data in the database, trains and scores the models and provides recommendations by executing a PowerShell script. This is the fastest way to deploy to your on-prem server. See <a href="Powershell_Instructions.html">PowerShell Instructions</a> for this deployment.
	