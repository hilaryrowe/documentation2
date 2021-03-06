# Validating the Configuration

After you edit the FTX configuration file, the system validates it for you and will tell you if any information is missing. You can do the following:

* **Validate the schema: **The configuration file will not be loaded by the application if there are errors. If any field is wrong or if any required field is not set properly, an indicator appears both on the left side of the code line in question, and in the lower-right corner. In addition, the Submit button will be disabled until you resolve all the errors. You can click the lower error link to open the error console, which will list all errors currently in the code.  
  ![](/configurations-in-factorytx/Errors and Console w Lines.png)

* **Test the configuration: **Check the logs for data receiver services to make sure that the connection works.  
  ![](/images/UI Full Log Screen w Lines.png)



