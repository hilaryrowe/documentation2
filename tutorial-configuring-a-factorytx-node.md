# Tutorial: Configuring a FactoryTX Node

After you [deploy Factory TX](/tutorial-deploying-factorytx.md), you can set up a FactoryTX node from scratch, which involves the following procedures:

* Connecting to a data source and confirming the authentication credentials and how to request the data

* Creating a new data receiver in the FTX configuration file

* Running the new data receiver and looking at the output

* Creating a new transmit with an API key

## Connecting to a Data Source {#docs-internal-guid-e2b35c38-6c14-7e9c-89d9-e5d535287fba}

Before you can pull data from a data source, you need to look at the machine and gather some information, including which protocol is being used \(file-based, SQL, OPC UA, etc.\) and the machine/asset name.

Before you can configure FactoryTX, make sure to test each data source to which you want to connect. You may need to use different software applications for each source. The following is a list of free tools that you can use:

* For FTP, use FileZilla: [https://filezilla-project.org/](https://filezilla-project.org/)

* For OPC-UA, use UAExpert: [https://www.unified-automation.com/products/development-tools/uaexpert.html](https://www.unified-automation.com/products/development-tools/uaexpert.html)

* For SQL, use HeidiSQL: [https://www.heidisql.com/download.php](https://www.heidisql.com/download.php)

**What to Test?**

* IP address or hostname of the target data source

* Authentication information

* Location of the data in folder/table/tag path

* List of fields/tags/files that you want to retrieve

In each case, you should be able to access the data that you want to use FactoryTX to transmit to Sight Machine before configuring each data receiver. This will make the connection process as straightforward as possible.

## Creating a New Data Receiver in the FTX Configuration File

When you open the FactoryTX tool for the first time, the skeleton of the source code will be available. You will need to fill in the missing parameters for the new data receiver.

**To create a new data receiver in the FTX configuration file:**

1. In a Web browser, navigate to the IP address of the NUC device or Virtual Machine. This information is available in the Resin.io interface. You want to connect to port 8090. For example: [http://IP\_ADDRESS:8090](http://IP_ADDRESS:8090)

2. On the Configuration tab, view the current configuration.

3. For each data receiver in the data\_receiver section, you will need to add a new block of JSON with the appropriate parameters for your new data source.  
   For more details on parameters, see the Data Receiver section in [Configurations in FactoryTX](/configurations-in-factorytx.md).

## Running the New Data Receiver and Looking at the Output

After you have a data receiver connected, you need to test the connection and look at the output. To do this, click the **Play** button on the left side of the interface.

![](/images/Running New Data Recevier Play Button.png)

## Creating a New Transmit with an API Key

You must set up the transmit information for the particular customer to the data flows to Sight Machine properly. For more information, see the Data Transmit section in [Configurations in FactoryTX](/configurations-in-factorytx.md).

**To create a new transmit with an API key:**

1. In the Sight Machine platform, in the AI Data Pipeline, go to **Models** &gt; **Location**, and then under FactoryTX API Credentials, copy both of the following:

   * **FactoryTX Username**

   * **FactoryTX API Key**

2. In FTX, on the Configuration tab, in the Source Code window, open the data\_transmit section.  
   **HINT: **You can expand any condensed code section by clicking the arrow to the left of it.  
   **Condensed:                          
   **![](/images/UI Config Code Condensed w Lines.png)**  
   Expanded:                          
   **![](/images/UI Config Code Expanded w Lines.png)

3. Paste the FactoryTX Username into API\_key\_ID parameter, and the FactoryTX API Key into the API\_key parameter. The following is sample code that you can copy and paste:  
   `"data_transmit" = [`

   `{`

   `"API_key_ID": "factory_5a676700398221437bce4cc337@sightmachine_ftx.com",`

   `"max_request_records": "3000",`

   `"poll_interval": "30",`

   `"base_url": "https://demo.sightmachine.io",`

   `"timeout": "120",`

   `"max_request_size_bytes": "6000000",`

   `"API_key": "BwH6AxSKqibgUbSK26-oODVKHM09K0sQIZ5JPoe8YRQ",`

   `"transmit_name": "remotedatapost"`

   `}`

   `]`



