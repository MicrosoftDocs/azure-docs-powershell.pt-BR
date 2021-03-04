---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/get-azcloudserviceinstanceview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceInstanceView.md
ms.openlocfilehash: cb077b2bdc6c91ccb3dc1c9099490c1d8bf6bea6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893239"
---
# Get-AzCloudServiceInstanceView

## SYNOPSIS
Obtém o status de um serviço de nuvem.

## SINTAXE

```
Get-AzCloudServiceInstanceView -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRIPTION
Obtém o status de um serviço de nuvem.

## EXEMPLOS

### Exemplo 1: Obter exibição de instância do serviço de nuvem
```powershell
PS C:\>$cloudServiceInstanceView = Get-AzCloudServiceInstanceView -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

PS C:\>$cloudServiceInstanceView
RoleInstanceStatusesSummary                                   Statuses
---------------------------                                   --------
{{ProvisioningState/succeeded : 4}, {PowerState/started : 4}} {Provisioning succeeded, Started, Current Upgrade Domain of cloud service is -1., Max Upgrade Domain of cloud service is 1.}

PS C:\>$cloudServiceInstanceView.ToJsonString()
{
  "roleInstance": {
    "statusesSummary": [
      {
        "code": "ProvisioningState/succeeded",
        "count": 4
      },
      {
        "code": "PowerState/started",
        "count": 4
      }
    ]
  },
  "statuses": [
    {
      "code": "ProvisioningState/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "PowerState/started",
      "displayStatus": "Started",
      "level": "Info",
      "time": "2020-10-28T13:26:48.8109686Z"
    },
    {
      "code": "CurrentUpgradeDomain/-1",
      "displayStatus": "Current Upgrade Domain of cloud service is -1.",
      "level": "Info"
    },
    {
      "code": "MaxUpgradeDomain/1",
      "displayStatus": "Max Upgrade Domain of cloud service is 1.",
      "level": "Info"
    }
  ]
}
```

Este cmdlet obtém a exibição de instância do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.

## PARÂMETROS

### -CloudServiceName
Nome do serviço de nuvem.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudServiceInstanceView

## NOTES

ALIASES

## LINKS RELACIONADOS

