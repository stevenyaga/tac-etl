===========================
Basic Troubleshooting Guide
===========================

This guide summarizes various issues that may arise during the day to day running of the ETL batch jobs. For each issue, there is a list of possible remedy or cause:


.. note::
   
   **What are the services that depend on service account. Note that this account is yet to be provided**

      * Oracle Linked Server to the EDW that has been created under ETL SQL Server database to retrieve data from EDW
      * The credential and proxy linked to the service account which has been created under ETL SQL Server instance inorder to run the SSIS packages      

Common issues
------------- 

#. **When service account user password expires and is reset, what are the services and accounts that need remapping**

    * Oracle Linked Server to the EDW that has been created under ETL SQL Server database to retrieve data from EDW

      .. image:: _static/images/sql_developer_login.png
         :alt: SQL Developer login
 
    * Update the credential and proxy linked to the service account which has been created under ETL SQL Server instance 

      * SQL server credential

         .. image:: _static/images/sql_server_credential.png
            :alt: SQL Server credential

      * SSIS package execution proxy

         .. image:: _static/images/sql_server_proxy.png
            :alt: SQL Server proxy
 
  
#. **ETL process cannot load data from EDW**

   * Check that the password for the service account has not expired

      * Try login into Oracle EDW database

         .. image:: _static/images/ssis_execution_log.png
            :alt: All SSIS executions

   * Confirm from EDW that there is valid data
   * Check the SSIS Execution logs. See :ref:`Execute Package <execute-package>`
      
      * Load SSIS All Executions Report
    
         .. image:: _static/images/ssis_execution_log.png
            :alt: All SSIS executions


      * SSIS executions summary
           
         .. image:: _static/images/ssis_execution_log_all.png
            :alt: All SSIS summary
