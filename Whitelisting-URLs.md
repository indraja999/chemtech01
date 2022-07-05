# This is a list of urls to be authentication whitelisted with our proxy/firewalls. Please extend if needed:
(All Port 80/443)

##Azure:
https://docs.microsoft.com/en-us/azure/azure-portal/azure-portal-safelist-urls?tabs=public-cloud
```
*.aadcdn.microsoftonline-p.com
*.aka.ms
*.applicationinsights.io
*.azure.com
*.azure.net
*.azurefd.net
*.azure-api.net
*.azuredatalakestore.net
*.azureedge.net
*.loganalytics.io
*.microsoft.com
*.microsoftonline.com
*.microsoftonline-p.com
*.msauth.net
*.msftauth.net
*.trafficmanager.net
*.visualstudio.com
*.windows.net
*.windows-int.net
*.azurecr.io
```
##Azure China:
```
*.azure.cn
*.microsoft.cn
*.microsoftonline.cn
*.chinacloudapi.cn
*.trafficmanager.cn
*.chinacloudsites.cn
*.windowsazure.cn
```
##Azure DevOps
https://docs.microsoft.com/en-us/azure/devops/organizations/security/allow-list-ip-url?view=azure-devops&tabs=IP-V4
```
https://*.dev.azure.com
https://*.vsassets.io
https://*gallerycdn.vsassets.io
https://*vstmrblob.vsassets.io
https://aadcdn.msauth.net
https://aadcdn.msftauth.net
https://aex.dev.azure.com
https://aexprodea1.vsaex.visualstudio.com
https://amcdn.msftauth.net
https://amp.azure.net
https://app.vssps.dev.azure.com
https://app.vssps.visualstudio.com
https://azure.microsoft.com
https://azurecomcdn.azureedge.net
https://cdn.vsassets.io
https://dev.azure.com
https://go.microsoft.com
https://graph.microsoft.com
https://live.com
https://login.live.com
https://login.microsoftonline.com
https://management.azure.com
https://management.core.windows.net
https://microsoft.com
https://microsoftonline.com
https://static2.sharepointonline.com
https://visualstudio.com
https://vsrm.dev.azure.com
https://vstsagentpackage.azureedge.net
https://windows.net
https://login.microsoftonline.com
https://app.vssps.visualstudio.com 
https://{organization_name}.visualstudio.com
https://{organization_name}.vsrm.visualstudio.com
https://{organization_name}.vstmr.visualstudio.com
https://{organization_name}.pkgs.visualstudio.com
https://{organization_name}.vssps.visualstudio.com
```

##Container Registries:
This is the most imporant URL! It is the security proxy and package repository for all our systems.
Should always be accessible through the VPN (EMEA-CH-3)
```
sulzerct.jfrog.io
```
###Dockerhub
(Proxy Implemented)
```
auth.docker.io
registry-1.docker.io
registry.cn-hangzhou.aliyuncs.com
index.docker.io/
dseasb33srnrn.cloudfront.net/
production.cloudflare.docker.com/
download.docker.com/
```
###Google Container Registry:
(Proxy Implemented)
```
gcr.io
storage.googleapis.com/
```
###Quay Container Registry:
(Proxy Implemented)
```
quay.io
```
###Github:
```
github.com/
*.githubusercontent.com/
```
###Chocolatey
(Proxy Implemented)
```
chocolatey.org
```
###Visual Studio Liveshare
https://docs.microsoft.com/en-us/visualstudio/liveshare/reference/connectivity
```
*.liveshare.vsengsaas.visualstudio.com:443
download.microsoft.com:443
*.servicebus.windows.net:443
```
###Ubuntu WSL Distribution
(Proxy Implemented)
```
http://archive.ubuntu.com
http://security.ubuntu.com
https://*.hashicorp.com
https://*.sublimetext.com
https://*.kubernetes.io
https://baltocdn.com
http://*.launchpad.net
```
###Elastic Cloud
https://slzelasticdev.kb.westeurope.azure.elastic-cloud.com:9243
https://slzelasticprd.kb.westeurope.azure.elastic-cloud.com:9243

###Machine Names:

| Machine Name | User | Team |
|--|--|--|
| N1014711| @<36EE8E94-42DD-626B-9F94-21E50CBCBEBE>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1015041 | @<946F22AB-7449-67DE-8C16-DAF9074FD02B>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1006653 | @<39A4F0A4-7CCB-6179-A9A4-E10016DA2EF7>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1008100 + N1030976 | @<031A927E-3A88-65DC-817B-56A0C1632AAC>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1015335 | @<7AB8FE55-5FF6-6B2B-9EB7-80FBB6C67577>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1014886 | @<13136036-1A52-67E9-95BC-31054253A078>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| N1027215 | @<13136036-1A52-67E9-95BC-31054253A078>  | @<A320825A-3C11-4244-AF54-E26D540783C4> |
| T1025668 + N1028232 | @<FDD14A11-8447-6735-9C84-935F75995031> | @<46C490E3-6C57-4DC8-A795-B506BD85CAFC> |
| N1028771 | @<D18638D8-7F1C-6994-8E2F-FFE7723624E0> | @<3FA49343-F58E-46FD-9F75-63D9382CE7BE> |
