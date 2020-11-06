---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 8856a2f9f1a65d6d312571d75e2400a7dcf30bc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432158"
---
# Set-AzureRmTrafficManagerEndpoint

## Sinopse
Atualiza um ponto de extremidade do Gerenciador de tráfego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmTrafficManagerEndpoint** atualiza um ponto de extremidade no Gerenciador de tráfego do Azure.
Esse cmdlet atualiza as configurações de um objeto de ponto de extremidade local.
Você pode especificar o objeto de ponto de extremidade usando o parâmetro *TrafficManagerEndpoint* ou usando o pipeline.

Você pode obter um objeto local que representa um ponto de extremidade usando o cmdlet Get-AzureRmTrafficManagerEndpoint.
Modifique o objeto localmente e use **set-AzureRmTrafficManagerEndpoint** para confirmar as alterações.

## EXEMPLOS

### Exemplo 1: atualizar um ponto de extremidade
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

O primeiro comando obtém um ponto de extremidade do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerEndpoint** .
O comando armazena o ponto de extremidade localmente na variável $TrafficManagerEndpoint.

O segundo comando altera esse ponto de extremidade localmente.
Esse comando altera a espessura do ponto de extremidade para 20.

O terceiro comando atualiza o ponto de extremidade no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerEndpoint.

## OS

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Esse cmdlet aceita um objeto **TrafficManagerEndpoint** .

## EXIBE

### Microsoft. Azure. Commands. Network. TrafficManagerEndpoint
Esse cmdlet retorna um objeto **TrafficManagerEndpoint** .

## INFORMA

## LINKS RELACIONADOS

