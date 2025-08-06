Filter Creation & Color Override Tool
Overview
This Dynamo script automates the creation and application of view filters in Revit. It reads a list of parameter values and their corresponding colors from a Microsoft Excel file, then generates and applies the necessary view filters to the active view based on user selections in a simple interface.

This tool is designed to standardize view graphics for electrical systems, save significant time, and ensure project-wide consistency.

Requirements
Before running this script, please ensure you have the following:

Software:

Revit 2023 or newer.

The Data-Shapes package for Dynamo must be installed.

Excel File:

An .xlsx file must be prepared with the exact column headers in the first row. The script will create one filter for each row of data.

Revit Project:

The active Revit project must contain elements with the parameter you wish to filter by (e.g., "Service Type").

How to Use (Step-by-Step via Dynamo Player)
This script is designed to be run from the Dynamo Player for the best user experience.

Step 1: Open Dynamo Player
In Revit, go to the Manage tab and click on Dynamo Player.

Step 2: Navigate to the Script
Click the "Browse to folder" icon and navigate to the folder where you have saved this Dynamo script (.dyn file). Your script should appear in the list.

Step 3: Open the User Interface
Click the "Edit Inputs" icon next to the script name. This will launch the custom user interface.

Step 4: Configure the Options in the UI
The main window will appear. Fill out the options as needed:

Select Excel File: Click this button and navigate to your prepared .xlsx file that contains the filter data.

Select Categories to FIlter: Check the boxes for all element categories you want the filters to apply to (e.g., Conduits, Cable Trays, Lighting Fixtures). ✅

Select Parameter: Choose the parameter the filters will be based on from the dropdown list (e.g., Service Type).

Select Rule Type: Choose the logical rule for the filters (e.g., Equals, Does not equal).

Add 'DV-' prefix...: Check this box if you want all created filter names to start with "DV-".

Step 5: Run the Script
Once all options are configured, click the "Run" button at the bottom of the window.

Step 6: Check the Results
A summary pop-up will appear telling you how many filters were created and applied. The filters will now be active and visible in your current Revit view.

Troubleshooting
The UI window doesn't appear?

Ensure the Data-Shapes package is correctly installed in Dynamo.

The summary says "0 filters created"?

This usually means the filters with those exact names already exist in the project. The script will not create duplicates.

Ensure you have selected at least one category in the UI.

The script returns an error?

Double-check that your Excel file has the correct column headers: ServiceType, Red, Green, Blue.

Make sure the parameter you selected in the UI exists on the categories you selected.

Version: 2.0

Author: Marcelo Alves
