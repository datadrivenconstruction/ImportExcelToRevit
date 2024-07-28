# DDC Import Excel to Revit
## Import parameter values from Excel

 Add-in allows to import parameter values from Excel database, created with [DataDrivenConstruction Excel Add-in](https://datadrivenconstruction.io/index.php/ddc-excel-plugin-for-working-with-revit-ifc-and-dwg/) or [DDC Revit converter](https://datadrivenconstruction.io/index.php/convertors/).

## Supported Revit versions

Revit 2020-2024

<img src="[https://your-image-url.type](https://datadrivenconstruction.io/wp-content/uploads/2024/07/project-data.gif)" width="900" >


## Installation

 To install for Revit 20XX run `\DdcImportExcel\DdcImportExcel.Installer\output\DdcImportExcel-<version>-Revit20XX.msi`. Then restart all Revit instances if some were running.

## Usage

1. Export you Revit model to xlsx file using [DataDrivenConstruction Excel Add-in](https://datadrivenconstruction.io/index.php/ddc-excel-plugin-for-working-with-revit-ifc-and-dwg/) or DataDrivenConstruction Revit convertor  [DDC Revit converter](https://datadrivenconstruction.io/index.php/convertors/)

2. Go to Add-Ins tab in Revit, select `Import DDC Excel` from `DdcImportExcel` panel.

- If xlsx file named the same, as you model file + `_rvt` postfix is found in `DDC` subfolder of your models folder, import will occur from it.

- If there is no such file, add-in ask you to locate it.

- Import from a file will be performed from a sheet that has the same name as the model, truncated to 25 characters.

- If no such sheet is found, the add-in will ask you to enter the name of the required sheet.

3. After importing, the log file saved in the Windows temporary folder will be prompted to be opened (for example, in Notepad).

  

## Features

- Change parameter values in Excel cells and import them back into the model.
- Create new parameters by creating new columns on the sheet and adding the "new_" prefix to the names of new parameters. *Important*: these parameters will be created as shared project parameters for instances of elements of the category for which the parameter value will be specified in the Excel table. You must specify the parameter data type after the name in the same way as exported parameters, after the colon (currently, only String type is supported). There must be a ` : ` (space-colon-space) separator after the parameter name.

 
## Support
If you encounter any issues or have questions, please file an issue on the GitHub repository or email us at info@datadrivenconstruction.io.
