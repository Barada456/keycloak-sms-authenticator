# keycloak-sms-authenticator

To install the SMS Authenticator one has to:
  use command : mvn clean install  , 
  then 2 jar files will be created under target folder ,
  copy both jar files and move it to keycloak installation folder > standalalone > deployments > paste both jars > it will show as deployed .

Configure your REALM to use the SMS Authentication. First create a new REALM (or select a previously created REALM).

Under Authentication > Flows:

    Copy 'Browse' flow to 'openstandia browser' flow
    Click on 'Actions > Add execution on the 'Openstandia Browser Forms' line and add the 'Twilio SMS Authentication'
    Set 'Twilio SMS Authentication' to 'REQUIRED'
    To configure the SMS Authernticator, click on Actions Config and fill in the attributes.

Under Authentication > Bindings:

    Select 'Browser with SMS' as the 'Browser Flow' for the REALM.

Users > view all users > select the user > attributes > add 2 attributes having "countryCode" and "phoneNumber" (note : both are case sensitive )
