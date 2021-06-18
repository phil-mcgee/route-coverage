# route-coverage
Parse expected and observed routes and compare

The expected and observed route files should look like the data copied from the Intellij debug values of the two arrays in a `it_tests_route_observation` acceptance test.  

Sample observed routes data
```
0 = {ObservedRoute@7281} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.faces', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
1 = {ObservedRoute@7282} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.jsf', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
2 = {ObservedRoute@7283} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
3 = {ObservedRoute@7284} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/faces/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
4 = {ObservedRoute@7285} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.faces', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
5 = {ObservedRoute@7286} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.jsf', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
6 = {ObservedRoute@7287} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
7 = {ObservedRoute@7288} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/faces/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}]}"
8 = {ObservedRoute@7289} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.faces', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}, EventSource{type=HEADER, name='Content-Type'}]}"
9 = {ObservedRoute@7290} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.jsf', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}, EventSource{type=HEADER, name='Content-Type'}]}"
10 = {ObservedRoute@7291} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}, EventSource{type=HEADER, name='Content-Type'}]}"
11 = {ObservedRoute@7292} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/faces/ping.xhtml', signature='/usr/local/tomcat/webapps/jsf-2.2-mojarra-route-coverage/ping.xhtml', sources=[EventSource{type=PARAMETER_KEY, name='null'}, EventSource{type=URI, name='null'}, EventSource{type=HEADER, name='null'}, EventSource{type=HEADER, name='Content-Type'}]}"
```

Sample expected routes data
```
0 = {ObservedRoute@6752} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.faces', signature='/ping.xhtml', sources=[]}"
1 = {ObservedRoute@6753} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.jsf', signature='/ping.xhtml', sources=[]}"
2 = {ObservedRoute@6754} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/ping.xhtml', signature='/ping.xhtml', sources=[]}"
3 = {ObservedRoute@6755} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='GET', url='/faces/ping.xhtml', signature='/ping.xhtml', sources=[]}"
4 = {ObservedRoute@6756} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.faces', signature='/ping.xhtml', sources=[]}"
5 = {ObservedRoute@6757} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.jsf', signature='/ping.xhtml', sources=[]}"
6 = {ObservedRoute@6758} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/ping.xhtml', signature='/ping.xhtml', sources=[]}"
7 = {ObservedRoute@6759} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='HEAD', url='/faces/ping.xhtml', signature='/ping.xhtml', sources=[]}"
8 = {ObservedRoute@6760} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.faces', signature='/ping.xhtml', sources=[]}"
9 = {ObservedRoute@6761} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.jsf', signature='/ping.xhtml', sources=[]}"
10 = {ObservedRoute@6762} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/ping.xhtml', signature='/ping.xhtml', sources=[]}"
11 = {ObservedRoute@6763} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='PUT', url='/faces/ping.xhtml', signature='/ping.xhtml', sources=[]}"
12 = {ObservedRoute@6764} "ObservedRoute{sessionId='AcceptanceTestSessionId', verb='DELETE', url='/ping.faces', signature='/ping.xhtml', sources=[]}"
```
