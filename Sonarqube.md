
SQ server consist 3 parts:

1)rules
2)web
3)db
port : 9000
User System :

user system sonsist sourcecode and sq scanner installed in it.

Workflow :

when u run the sq on source code then sq scanner will fetch the rules form the sq server and apply on the code.

scanner will the generate the report and store it into  sq DB,

web will display the output  



           WEB  ------- > DB
   
web developed in html - java - css -s

db H2 default - mssql - oracle -ps

addons Elasticsearch  


Sonarqube can not run on root user coz of addons Elasticsearch  function.

normal user we hv to create to run sonarqube


sonarqube scanner: it is utility which sacn the code and generate report

source code for build the anylysis


Quality profile vs Quality gates:

Every project has a quality profile set for each supported language. The profile defines which rules will be applied during analysis. 
After analysis, the quality gate takes the resulting metrics and compares them to its defined thresholds to determine if the code meets 
the requirements for release or merge.

Scanner types:

cmd
maven
gradle
jenkins
az devops
