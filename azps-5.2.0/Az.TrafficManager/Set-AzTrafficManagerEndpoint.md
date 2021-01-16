---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260448"
---
# Set-AzTrafficManagerEndpoint

## Sinopse
Atualiza um ponto de extremidade do Gerenciador de tráfego.

## SYNTAX

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de tráfego do Azure.
Esse cmdlet atualiza as configurações de um objeto de ponto de extremidade local.
Você pode especificar o objeto de ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.

Você pode obter um objeto local que representa um ponto de extremidade usando o cmdlet Get-AzTrafficManagerEndpoint.
Modifique o objeto localmente e use **set-AzTrafficManagerEndpoint** para confirmar as alterações.

## EXEMPLOS

### Exemplo 1: atualizar um ponto de extremidade
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

O primeiro comando obtém um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzTrafficManagerEndpoint** .
O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint.

O segundo comando altera esse ponto de extremidade localmente.
Esse comando altera a espessura do ponto de extremidade para 20.

O terceiro comando atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Especifica um objeto **TrafficManagerEndpoint** local.
Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## EXIBE

### Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint

## INFORMA

## LINKS RELACIONADOS
