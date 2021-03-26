---
title: Caiasoft Offsite Request Addon
layout: default
nav_order: 1
---

# Caiasoft Offsite Request Addon

## Addon files: 

https://www.notion.so/atlassys/Caiasoft-Offsite-Request-Addon-5b357978ea2747759c00938afd1d7936#3e34b91da6e64e1e8fc1d226b94d067f

## Implementation steps:

* Submit ticket to [support@atlas-sys.com](mailto:support@atlas-sys.com) to install Aeon API (if hosted server)
* Discuss desired processing queues (use workflow example to guide discussion)
    * configure queues in Queues table of Customization Manager 
    * Note: an error queue is required
* Get API key and Caiasoft server URL from Caiasoft
* Provide Caiasoft with Aeon API key (found in WebPlatformConfig) and list of Queue IDs used for workflow (specifically steps where Caia will be updating Aeon)
* Install addon in Aeon Customization Manager and configure using Caiasoft URL, API key, and queues specified in workflow (need to configure queues for initial retrieval in addon)
* TEST!
    * Recommend scheduling test with Atlas & Caiasoft to ensure everything is working properly and to troubleshoot as needed before scheduling test with site staff
* When ready, switch Caia connection information (if using test credentials)
    * We recommend running one final test if connection information changes
* Go Live! 


## Caiasoft Offsite Request Workflow:

Note: all queue names are suggestions

* Patron submits request -> Awaiting Offsite Request Processing
* Staff review request to confirm all necessary details
* Print Callslip 
* Request status changes to Submitted Offsite Request
* Addon kicks off here, submits request details to Caiasoft
* On successful transmission, status changes to In Item Retrieval - Offsite
	* If the request fails, check Error Processing Offsite Request queue and see the request notes for details
* Offsite staff will pull requested materials and update Caiasoft
* Request status will change to In Transit from Offsite (OPTIONAL)
* When material arrives, places items on hold in Aeon
* To return material, route the request(s) to Awaiting Return to Offsite
* Offsite staff will pick up materials and transmit a file to Caiasoft
* Request status will change to Awaiting Item Reshelving - Offsite (OPTIONAL)
* When materials are put away in their permanent storage location, offsite staff will transmit one file file update
* Request status will change to Request Finished

! [flowchart showing workflow outlined above in visual chart](\assets\images\Aeon Caiasoft Default Workflow.png)


## Questions?

Caiasoft: Laura Beatham - [laura@caiasoft.com](mailto:laura@caiasoft.com), [https://www.caia-solutions.com/](https://www.caia-solutions.com)

Atlas Systems: Katie Gillespie - [kgillespie@atlas-sys.com](mailto:kgillespie@atlas-sys.com), [https://www.atlas-sys.com](https://www.atlas-sys.com)