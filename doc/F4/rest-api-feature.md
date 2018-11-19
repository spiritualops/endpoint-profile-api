# F4: Rest API

## Overview

- **s12**: "list" endpoint
    - Contains data for all endpoints to be displayed
    - F1.1 - F1.3 in JSON format
    - Unique ID for each endpoint
- **s13**: "detail" endpoint
    - Contains detailed data for a single endpoint
    - F2.1-F2.6 in JSON format
    - Endpoint IDs will be leveraged to map the detail page URLs.
- **s14**: Unexposed functionality
    - A listener needs to be created to process new connections to a network 