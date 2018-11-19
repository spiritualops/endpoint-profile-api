# endpoint-profile-api

- Author: Brian Thompson
- Client: Lucas Chumley

## Description

"The "Endpoint Profile" page displays a list of all known desktop and laptop computers (aka 
"endpoints") on the network. This page provides the user "at-a-glance' feedback about: 
the hostname of each endpoint, the operating system installed on the endpoint, and if the 
endpoint is currently on the network. By clicking on any of the endpoints the page provides
 more detailed information about the selected endpoint including: FQDN, IP address, MAC address, 
 Operating System, Processor, and RAM. The user can search for endpoints matching any of these properties."
 
 ## Features
 
 1. List screen that displays the following:
    1. Hostname of each endpoint
    2. OS installed on each endpoint
    3. Network status of each endpoint
 2. Detail screen that display the following:
    1. FQDN
    2. IP address
    3. MAC address
    4. OS
    5. Processor
    6. RAM
 3. Search functionality that can match any of the properties from F1 and F2.
    1. `sessionStorage` will be leveraged in the browser
    2. MongoDB used to store larger amounts of data (when `sessionStorage` becomes ineffecient)
 4. Rest API
    1. "list" endpoint
        1. Contains data for all endpoints to be displayed
        2. F1.1 - F1.3 in JSON format
        3. Unique ID for each endpoint
    2. "detail" endpoint
        1. Contains detailed data for a single endpoint
        2. F2.1-F2.6 in JSON format
        3. Endpoint IDs will be leveraged to map the detail page URLs.
    3. Unexposed functionality
        1. A listener needs to be created to process new connections to a network 
 
 ## Technology Stack
 
 ### Node.js

The API will be written in Node with the Express framework.  Node provides very powerful OS operations 
out-of-the-box, and is tailored to the ACs for this particular API.
 
 ### Angular
 
 Angular's built in HTTP works well with Rest APIs.  Additionally, Angular Material will be used to align
 Google's "Material Design" best practices.
 
 ### MongoDB
 
 A NoSQL database will be created when `sessionStorage` begins to slow down the browser.
 
 