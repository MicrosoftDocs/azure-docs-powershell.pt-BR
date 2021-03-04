---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: b3bccc5d538c8ce5e3a79b621b48d75556ed0189
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889053"
---
# Get-AzEnvironment

## SYNOPSIS
Obter pontos de extremidade e metadados para uma instância dos serviços do Azure.

## SINTAXE

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O Get-AzEnvironment cmdlet obtém pontos de extremidade e metadados para uma instância dos serviços do Azure.

## EXEMPLOS

### Exemplo 1: Obter o ambiente do AzureCloud
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente do AzureCloud (padrão).

### Exemplo 2: Obter o ambiente do AzureChinaCloud
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente do AzureChinaCloud.

### Exemplo 3: Obter o ambiente do AzureUSGovernment
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente do AzureUSGovernment.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Especifica o nome da instância do Azure a ser obter.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## SAÍDAS

### Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment

## NOTES

## LINKS RELACIONADOS

[Add-AzEnvironment](./Add-AzEnvironment.md)

[Remove-AzEnvironment](./Remove-AzEnvironment.md)

[Set-AzEnvironment](./Set-AzEnvironment.md)

