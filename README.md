[![CircleCI](https://circleci.com/gh/snowdrop/rest-http-example/tree/master.svg?style=shield)](https://circleci.com/gh/snowdrop/rest-http-example/tree/master)

https://appdev.openshift.io/docs/spring-boot-runtime.html#mission-http-api-spring-boot

Based on 
(1). https://www.baeldung.com/spring-boot-keycloak
(2). https://www.yawintutor.com/there-was-an-unexpected-error-type-forbidden-status-403-access-denied/

![Screen 01](./images/screen1.png)

![Screen 02](./images/screen2.png)

![Screen 03](./images/screen3.png)

![Screen 04](./images/screen4.png)

![Screen 05](./images/screen5.png)

![Screen 06](./images/screen6.png)

![Screen 07](./images/screen7.png)

curl --location --request POST 'https://keycloak-sso.apps.cluster-pgwmr.pgwmr.sandbox320.opentlc.com/auth/realms/demo/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'client_id=client-token' \
--data-urlencode 'client_secret=caafe25a-491f-4021-b0b7-315b45e5c435' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'scope=openid' \
--data-urlencode 'username=user1' \
--data-urlencode 'password=password'

curl --location --request POST 'https://keycloak-sso.apps.cluster-pgwmr.pgwmr.sandbox320.opentlc.com/auth/realms/demo/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'client_id=client-token-2' \
--data-urlencode 'client_secret=8b7b069e-ecc2-4f92-8c7e-1c44acf73d33' \
--data-urlencode 'grant_type=client_credentials'

curl --location --request POST 'https://keycloak-sso.apps.cluster-pgwmr.pgwmr.sandbox320.opentlc.com/auth/realms/demo/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'client_id=demoapp' \
--data-urlencode 'username=user1' \
--data-urlencode 'password=password' \
--data-urlencode 'grant_type=password'

