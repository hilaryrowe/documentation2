# Configuring a File-Based Plugin

The customer may have data from local machines. A file-based plugin could be a CSV file, log files, Excel file, etc.

## File-Based FTX Configuration File Sample

![](/configuring-a-data-receiver/Full FTX File Based Config File Code Sample w Lines.png)

## Calling pandas.read\_csv

The PARSE function allows for all of the functionality for Pandas. This is a powerful toolset that should handle many of the cases for differences in the CSV file format. For more information, refer tof you do not have remote\_delete\_files enabled, you need to keep all files in the completed folder so that FTX knows which ones have already been processed.

If you have remote\_delete\_files enabled, you can rotate files using a tool such as Logrotate:

[https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read\_csv.html](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html)

## Managing the Completed/Incoming Folder

Before pandas.read\_csv is called, the file is copied locally to a temporary file.

You can see which files have been completed in the completed folder. By default, this is located in: **/var/spool/sightmachine/factorytx/databuffer/completed**

If you do not have remote\_delete\_files enabled, you need to keep all files in the completed folder so that FTX knows which ones have already been processed.

If you have remote\_delete\_files enabled, you can rotate files using a tool such as Logrotate.

