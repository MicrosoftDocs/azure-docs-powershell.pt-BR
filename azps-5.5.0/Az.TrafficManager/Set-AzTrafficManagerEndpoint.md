---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112359"
---
# Set-AzTrafficManagerEndpoint

## Sinopse
Atualiza um ponto de extremidade do Gerenciador de Tráfego.

## Sintaxe

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de Tráfego do Azure.
Este cmdlet atualiza as configurações de um objeto de ponto de extremidade local.
Você pode especificar o objeto do ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.

Você pode obter um objeto local que representa um ponto de extremidade usando Get-AzTrafficManagerEndpoint cmdlet.
Modifique o objeto localmente e use **Set-AzTrafficManagerEndpoint** para comprometer suas alterações.

## Exemplos

### Exemplo 1: Atualizar um ponto de extremidade
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

O primeiro comando obtém um ponto de extremidade do Gerenciador de Tráfego do Azure usando o cmdlet **Get-AzTrafficManagerEndpoint.**
O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint dados.

O segundo comando altera esse ponto de extremidade localmente.
Esse comando altera a peso do ponto de extremidade para 20.

O terceiro comando atualiza o ponto de extremidade no Gerenciador de Tráfego para corresponder ao valor local no $TrafficManagerEndpoint.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -TrafficManagerEndpoint
Especifica um objeto **Local TrafficManagerEndpoint.**
Este cmdlet atualiza o Gerenciador de Tráfego para corresponder a este objeto local.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## Saídas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## Notas

## LINKS RELACIONADOS
