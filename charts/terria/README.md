terria
======
A Helm chart for terria map

Current chart version is `0.24.1`

Source code can be found [here](https://terria.io/)



## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| authentication.enabled | bool | `false` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| clientConfig.initializationUrls[0] | string | `"terria"` |  |
| clientConfig.parameters.appName | string | `"Terria Map"` |  |
| clientConfig.parameters.brandBarElements[0] | string | `""` |  |
| clientConfig.parameters.brandBarElements[1] | string | `"<a target=\"_blank\" href=\"http://terria.io\"><img src=\"images/SI_high.png\" height=\"52\" title=\"Version: {{version}}\" /></a>"` |  |
| clientConfig.parameters.brandBarElements[2] | string | `""` |  |
| clientConfig.parameters.disclaimer.text | string | `"Disclaimer: This map must not be used for navigation or precise spatial analysis"` |  |
| clientConfig.parameters.disclaimer.url | string | `""` |  |
| clientConfig.parameters.experimentalFeatures | bool | `true` |  |
| clientConfig.parameters.googleAnalyticsKey | string | `nil` |  |
| clientConfig.parameters.googleAnalyticsOptions | string | `nil` |  |
| clientConfig.parameters.googleUrlShortenerKey | string | `nil` |  |
| clientConfig.parameters.mobileDefaultViewerMode | string | `"2d"` |  |
| clientConfig.parameters.proj4ServiceBaseUrl | string | `"proj4def/"` |  |
| clientConfig.parameters.supportEmail | string | `"help@example.com"` |  |
| clientConfig.parameters.useCesiumIonBingImagery | bool | `false` |  |
| clientConfig.parameters.useCesiumIonTerrain | bool | `false` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"satapps/terriamap"` |  |
| image.suffix | string | `"solomon"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations."kubernetes.io/ingress.class" | string | `"nginx"` |  |
| ingress.annotations."nginx.ingress.kubernetes.io/rewrite-target" | string | `"/$1"` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hosts[0].host | string | `"dev-csvs.sa-catapult.co.uk"` |  |
| ingress.hosts[0].paths[0].path | string | `"/terria-solomon/(.*)"` |  |
| ingress.tls | list | `[]` |  |
| initConfig.baseMapName | string | `"Positron (Light)"` |  |
| initConfig.catalog[0].description | string | `"This group contains DRR vector data for Solomon Island"` |  |
| initConfig.catalog[0].name | string | `"DRR"` |  |
| initConfig.catalog[0].type | string | `"wfs-getCapabilities"` |  |
| initConfig.catalog[0].url | string | `"http://geoserver:8080/geoserver/solomon/ows?service=wfs&version=2.0.0&request=GetCapabilities"` |  |
| initConfig.catalog[1].description | string | `"This group contains maps of Hazard for Solomon Island"` |  |
| initConfig.catalog[1].geoserverWorkspace | string | `"solomon_rasters"` |  |
| initConfig.catalog[1].name | string | `"Hazard data"` |  |
| initConfig.catalog[1].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[1].url | string | `"http://geoserver:8080/geoserver/solomon_rasters/wms?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[2].description | string | `"This group contains DEMs for Solomon Island provided by University of Portsmouth"` |  |
| initConfig.catalog[2].name | string | `"DEMs"` |  |
| initConfig.catalog[2].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[2].url | string | `"http://geoserver:8080/geoserver/solomon_dems/wms?service=WMS&version=1.3.0&request=GetCapabilities"` |  |
| initConfig.catalog[3].description | string | `"This group contains ERA5 30 years average climate data for Solomon Island provided by Met Office"` |  |
| initConfig.catalog[3].name | string | `"ERA5 30 years average Climate data"` |  |
| initConfig.catalog[3].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[3].url | string | `"http://geoserver:8080/geoserver/climate_30yrs/wms?service=WMS&version=1.3.0&TILED=true&request=GetCapabilities"` |  |
| initConfig.catalog[4].description | string | `"This group contains ERA5 monthly climate data for Solomon Island provided by Met Office"` |  |
| initConfig.catalog[4].name | string | `"ERA5 Monthly Climate data"` |  |
| initConfig.catalog[4].type | string | `"wms-getCapabilities"` |  |
| initConfig.catalog[4].url | string | `"http://geoserver:8080/geoserver/climate_monthly/wms?service=WMS&version=1.3.0&TILED=true&request=GetCapabilities"` |  |
| initConfig.homeCamera.east | int | `177` |  |
| initConfig.homeCamera.north | int | `-5` |  |
| initConfig.homeCamera.south | int | `-24` |  |
| initConfig.homeCamera.west | int | `152` |  |
| initConfig.viewerMode | string | `"2d"` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| serverConfig.allowProxyFor[0] | string | `"geoserver:8080"` |  |
| serverConfig.allowProxyFor[1] | string | `"thredds:8080"` |  |
| serverConfig.blacklistedAddresses | list | `[]` |  |
| serverConfig.port | int | `3001` |  |
| serverConfig.proxyAuth.geoserver:8080.authorization | string | `"Basic dGVzdDp0ZXN0"` |  |
| service.port | int | `3001` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
