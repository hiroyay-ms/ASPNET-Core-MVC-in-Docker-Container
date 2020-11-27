# ASPNET-Core-MVC-in-Docker-Container

<br />

## リソース グループのプロビジョニング

### パラメーター
- **resourceGroupName**: リソース グループ名
- **location**: リージョン

<br />

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhiroyay-ms%2FASPNET-Core-MVC-in-Docker-Container%2Fmain%2Farm%2Ftemplates%2Fdeploy-resource-group.json)

<br />

## Azure Kubernetes Service のプロビジョニング

### パラメーター
- **aksClusterName**: Kubernetes クラスター名
- **kubernetesVersion**: Kubernetes バージョン (1.16.13, 1.16.15, 1.17.9, 1.17.11, 1.18.6, 1.18.8 から指定)
- **nodeCount**: ノード数
- **nodeSize**: ノードのインスタンス サイズ
- **servicePrincipalClientId**: サービス プリンシパル ID
- **servicePrincipalClientSecret**: サービス プリンシパル ID のシークレット

＊事前にサービス プリンシパルの作成が必要

<br />

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhiroyay-ms%2FASPNET-Core-MVC-in-Docker-Container%2Fmain%2Farm%2Ftemplates%2Fdeply-aks-cluster.json)

<br />

## Web App for Containers のプロビジョニング

### パラメーター
- **hostingPlanName**: App Service プラン名
- **planSkuName**: 価格レベル (S1-3, P1-3V2, P1-3V3 から選択)
- **webSiteName**: Web アプリ名
- **subscriptionId**: Azure Container Registry のサブスクリプション Id
- **azureContainerRegistry**: Azure Container Registry レジストリ名
- **acrResourceGroupName**: Azure Container Registry が所属するリソース グループ名
- **imageTag**: 展開するイメージ (リポジトリ名：イメージ タグで指定)

<br />

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhiroyay-ms%2FASPNET-Core-MVC-in-Docker-Container%2Fmain%2Farm%2Ftemplates%2Fdeploy-webapps-for-container.json)
