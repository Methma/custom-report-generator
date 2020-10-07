# custom-report-generator

This is a custom implementation of the WSO2 APIM Analytics Monthly Usage Report.

This implementation creates a table with the following information.

* API Name
* API Version
* UserName
* Hit Count

# Build

1) Checkout wso2/analytics-apim v3.1.0 version [1] and build it using 'mvn clean install' command.
2) Run 'mvn clean install'.
3) Copy the bundle 'org.wso2.analytics.apim.custompdf-3.1.0-SNAPSHOT.jar' into {ANALYTICS_HOME}/lib
 directory
4) Set the report:implClass config in conf/dashboard/deployment.yaml to org.wso2.analytics.apim.custompdf.CustomPDFGenerator
5) Start the dashboard server, and try downloading the usage report via the admin dashboard. This should result in a PDF report with the above mentioned columns instead of the default ones. 

[1]. https://github.com/wso2/analytics-apim/tree/v3.1.0