## ToDo

- Work on a document that reference all the datasets available on KJ13 with the different licence restrictions.
- Intake Observational catalogue
- Understand CMOR (CF Compliant standard)
- Create a list of available CMORISERs for dataset (check ESMValTool website, ILAMB-DATA scripts)
- Contact communities regarding potential Observation Dataset. Maybe create a survey.
- Add Observational datasets with a focus on Australia / Southern ocean

We have started a Data Development Project at NCI (kj13).
The project is used to process the datasets needed to run the evaluation recipes that are part of ILAMB, ESMValTool and COSIMA Cookbook.

You can browse the content of what we have collected so far in 

`/g/data/kj13/datasets/`

`auxiliary_data` contains some auxiliary files  needed for plotting of masking the data. They are mainly shapefiles for `cartopy`.

## ESMValTool

`esmvaltool` contains the datasets needed to run the ESMValTool recipes.
We are in the process of getting all the recipes working at NCI:
see here: https://github.com/ACCESS-NRI/ESMValTool-workflow

In that directory you have:

`esmvaltool_climate_data` which contains some model outputs that are automatically downloaded by the ESMValTool because it cannot find them at NCI. They are essentially model outputs from models participating to the CMIP (CMIP3, CMIP5, CMIP6 projects). OBS4MiP is an observation project to support CMIP.
Those datasets are downloaded automatically from the ESGF platform:
https://esgf.nci.org.au/projects/esgf-nci/

`obsdata-v2` contains observational datasets directly used by ESMValTool.
They are basically CMORised version of datasets in `raw-data`. 
The datasets are organised into Tiers. 
Tier1 comes with no licensing restrictions.
Tier2 comes with some restrictions but can be shared and redistributed.
Tier3 cannot be shared.
**would be good to clarify those definitions**

You can find a list of the datasets in the ESMValTool documentation:
https://docs.esmvaltool.org/en/latest/input.html

**would be great to have a table with a link to the original dataset, licensing information etc**

The source of the data can be found by browsing the ESMValTool code.
or by using esmvaltool directly.

`module use /g/data/xp65/public/modules`
`module load conda/access-med`

`esmvaltool data info CERES-EBAF` (example)

`raw-data` contains raw datasets (not CMORISED)
We only have Tier3 for now.

**would be good to see if some datasets are available in the NCI-Catalog or in the NCI-Thredd catalog**

https://geonetwork.nci.org.au/geonetwork/srv/eng/catalog.search#/home
https://dapds00.nci.org.au/thredds/catalog.html


## ILAMB

	The ILAMB-data collection has been replicated in project kj13 and can be found in

`/g/data/kj13/datasets/ilamb`

See the ILAMB-Data repository for context:
https://www.ilamb.org/
https://github.com/rubisco-sfa/ILAMB-Data

We have already worked on collecting the licences for those:
https://github.com/ACCESS-NRI/ILAMB-workflow/issues/11

The table above gives a good idea of what I would like to have across the data stored in kj13

https://docs.google.com/spreadsheets/d/1gaMN7naLY4-Hnom6oR6wlPL-nmjAxQ01A3OGvbKWmbI/edit#gid=0

That data collection is being replicated to the `ct11` project which is an NCI data collection

https://docs.google.com/document/d/1pjrNfRf-T0Uvu9cFXvp1nuBYYHMD5f_NbU4F6C0TuKo/edit


## IOMB

Very similar to ILAMB but for ocean

https://github.com/rubisco-sfa/IOMB-Data


## CMORISers 

Used to make the files CF-Compliant which is a requirement for the tools we are using.
There are a lot availbale in ESMValTool, ILAMB etc...
