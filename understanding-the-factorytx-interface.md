# Understanding the FactoryTX Interface {#docs-internal-guid-92afc525-66cc-fd30-3c17-d9363746a63c}

The FactoryTX interface provides a way to view, edit, and save changes to the three sections of the configuration file source code:

* Data Receiver

* Transforms

* Data Transmit

For more details about those three elements, see [Configurations in FactoryTX](/configurations-in-factorytx.md).

## Editing the Configuration

The Configuration section of FactoryTX allows you to view the FTX configuration file, as well as access other features.

![](/images/UI Full Configuration Screen w Lines.png)

On the Configuration screen, you can also do the following:

* Stop and start services as necessary.  
  ![](/images/UI Config Started w Lines.png)  
  ![](/images/UI Config Stopped w Lines.png)

* Check the status of CPU, memory, or disk usage.  
  ![](/images/UI Config Usage w Lines.png)

* Fold and unfold the code viewing window.  
  ![](/images/UI Config Fold w Lines.png)  
  ![](/images/UI Config Unfold w Lines.png)

* Launch a search. You can run wildcard and regex searches.  
  ![](/images/UI Config Search w Lines.png)

* Use the navigation links to jump to the data\_receiver, data\_transmit, or transforms section of the code.  
  ![](/images/UI Config Jump To w Lines.png)

* If you have any errors, indicators will appear on the screen.  
  ![](/images/UI Config Errors w Lines.png)  
  Click the error message link to open the error console, which lists all errors currently in the code.  
  
  **NOTE: **You cannot Submit code changes until you clear all errors. The console will provide the details you need to resolve them.  
  ![](/images/UI Config Error Console w Lines.png)

* Click **Submit** to submit configuration changes.  
  **NOTE: **The Submit button will remain disabled as long as no changes have been made to the configuration, or if it contains any errors.  
  ![](/images/UI Config Submit w Lines.png)

## Viewing Logs {#docs-internal-guid-92afc525-66df-d9a2-14de-6f2e54f61d02}

On the Log screen, you can view a list of the FTX logs as they are being created.

![](/images/UI Full Log Screen w Lines.png)

