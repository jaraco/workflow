# Describers: CKAN/Metadata

## What do Describers do?
Describers creates a descriptive record in the DataRefuge CKAN repository for each bag. Then they links the record to the bag, and make the record public

## Getting set up as a Describer
- Skills recommended for this role: in general, Describers need to have a good handle on metadata practices 
- Apply to become a Describer 
    - By asking your DataRescue guide or by filling out [this form](https://docs.google.com/a/temple.edu/forms/d/e/1FAIpQLSfh9YIFnDrc-Cuc0hTd-U37J3D8xw8K7VXmzWkPs6Y5Q0wfVg/viewform)
    - Note that an email address is required to apply.
    - Note also that you should be willing to have your real name be associated with the datasets, to follow archival best practices (see [guidelines on archival best practices for Data Refuge](http://www.ppehlab.org/blogposts/2017/2/1/data-refuge-rests-on-a-clear-chain-of-custody) for more information).
- The organizers of the event (in-person or remote) will send you an invite to the [Archivers app](http://www.archivers.space/), which helps us coordinate all the data archiving work we do.
	- Click the invite link, and choose a user name and a password.    
- Make sure you have an account on the DataRefuge slack (or other slack team recommended by your event organizers) This is where people share expertise and answer each other's questions.
	- Ask your event organizer to send you an invite 
- The organizers will also create an account for you in the CKAN instance at https://www.datarefuge.org/ 
  - Test that you can log in successfully
- Get set up with Python and the Python script to make a bag at the command line https://github.com/LibraryOfCongress/bagit-python
- If you need any assistance:
  - Talk to your DataRescue Guide if you are at an in-person event
  - Or post questions on Slack in the #Describers channel (or other channel recommended by your event organizers).     
      
## Claiming a bag
**Note: these features have not yet been implemented in the Archivers app. It should be there shortly.**
  - You will work on datasets that were bagged by Baggers. 
  - Go to the [Archivers app](http://www.archivers.space/), click `URLS` and then `DESCRIBE`: all the URLs listed are ready to be added to the CKAN instance
    - Available URLs are the ones that have not been checked out by someone else, that is, that do not have someone's name in the User column.
- Select an available URL and click its UUID to get to the detailed view, then click `Check out this URL`. It is now ready for you to work on, and no one else can do anything to it while you have it checked out. 

## Note: URL vs UUID
The `URL` is the link to examine and harvest, and the `UUID` is a canonical ID we use to connect the url with the data in question. The UUID will have been generated earlier earlier in the process. UUID stands for Universal Unique Identifier. 

## QA step 
- In the Archivers app click on the `Bag URL` in the Bag section.   
- The file should start downloading
- When it is downloaded, unzip it 
- Spot check some of the files (make sure they open and look normal, i.e., not garbled)

## Create new record in CKAN
- Go to [CKAN](https://www.datarefuge.org/) and click Organizations in the top menu
- Choose the organization (i.e., federal agency) that your dataset belongs to, for instance: `NOAA`, and click it.
- Click "Add Dataset"
- Start entering metadata in the new record, following the metadata template below.  
  - Title: title of dataset, e.g., "Form EIA-411 Data"
  - Description: Usually copied and pasted description found on webpage
  - Tags: basic descriptive keywords, e.g., "electric reliability", "electricity", "power systems"
  - License:  choose value in dropdown
  - Organization: choose value in dropdown, e.g., "United States Department of Energy"
  - Visibility: select "Public"
  - Source: URL where site is live, also in JSON, e.g., "http://www.eia.gov/electricity/data/eia411/"
- To decide what value to enter in each field:
    - Open JSON file that is in the bag you have downloaded; it contains some of the metadata you need
    - Go to the original location of the item on the federal agency website (found in the Json file), to find more more facts about the item such as description, title of the dataset, etc. 
    	- Alternatively, you can also open the html file that should be included in the bag and is a copy of that original main page. 
    
## Linking the CKAN record to the bag:
  - Click "Next: Add Data" at the bottom of the CKAN form
  - Enter the following information:
    - Link: Bag URL, e.g., "https://drp-upload-bagger.s3.amazonaws.com/remote/77DD634E-EBCE-412E-88B5-A02B0EF12AF6_2.zip"
    - Name: filename, e.g., "77DD634E-EBCE-412E-88B5-A02B0EF12AF6_2.zip"
    - Format: select "Zip"
  - Click "Finish"
  - Test that the link you just created work by clicking it, and verifying that the file begins to download. 
    - Note that you don't need to finish downloading it again.

## Finishing up
**Note: these features have not yet been implemented in the Archivers app. It should be there shortly.**
- In the Archivers app, add URL to the CKAN record in cell "CKAN record URL"
   - The syntax will be "https://www.datarefuge.org//dataset/[datasetNameGeneratedByCkan]"
- Check the Describe checkbox (on the right-hand side) to mark that step as completed. 
- Click `Save`.
- Click `Check in URL`, to release it and allow someone else to work on the next step. 

  
