# Remediations Sections.

I will publish one series of remeditions product of one "Ethical Hacking Report", i see interting this theme, this very useful for remeditions of the vulnerabilities, this is process is usual in enterprice, when the client been make "Penetration Testing" over to app and vendor should by compromise to resolve this issues with patch, new politics, update, etc.

# Remediation 01

## Description. ###

During analysis was possible determine the software version of the server web use that host website, this through of the HTTP Header Request to the server.

## Information ###
    
[CWE:497 Exposure of Sensitive System Information to an Unauthorized Control Sphere](https://cwe.mitre.org/data/definitions/497.ht)
 
## Requirement ###

| Software or library |
| ------------- |
| Internet Information Services (IIS) |
| ASP.Net .Net Framework, lower that 4.8 | 

## Exploitation of the Requirement ###

No exist requirement of the exploitation

## Impact ##
 The expose of the software version is considered the bad practice the security, as can facilitate the search the vulnerability and settings that may affect the software used

## Mitigation ## 

Change settings of the web server for not divulge that information of the used version.
In the case 

## Steps ## 

In case of the tecnologic as "Microsoft" that use IIS and ASP.Net use one file  named "web.config", located usually in the root folder thi App,  this is file stay in format "xml", so inside you see one series of the "nodes" , we moust find the following nodes:

1. "system.webServer"
2. "httpProtocol"
3. "customHeaders"

And inside node add following line:

"<remove name="X-Powered-By"/>" 




[Reference](https://www.ibm.com/support/pages/disabling-iis-web-banner-andother-iis-headers)