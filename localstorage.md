# Local Storage

Persistent local storage is one of the areas where native client applications have held an advantage over web applications. 
    
    - For native applications, the operating system typically provides an abstraction layer for storing and retrieving application-specific data like preferences or runtime state 

    - These values may be stored in the registry, INI files, XML files, or some other place according to platform convention 

    - If your native client application needs local storage beyond key/value pairs, you can embed your own database, invent your own file format, or any number of other solutions.

### Cookies
    - invented early in the web's history
    - they can be used for persistent local local storage of small amounts of data
    - downsides:
        - included with every HTTP request
            - slows down web application by needlessly trasmitting the same data over and over
            - sends data unencrypt over the internet
                - unless your entire web app is served over ssl
        - limited to about 4 KB of data
            - enough to slow your application but not enough to be useful 

    - desired aspects of using local storage:
        - a lot of storage space
        - on the client
        - persists beyond a page refresh
        - isn't transmitted to the server

   **Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways**


**[🠴 RETURN](README.md)**