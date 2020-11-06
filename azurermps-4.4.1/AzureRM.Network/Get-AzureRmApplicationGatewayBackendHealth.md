---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: d3f5114243828623ba6c55e9694cc4250ae12657
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427872"
---
# Get-AzureRmApplicationGatewayBackendHealth

## Sinopse
Obtém a integridade do backend do Application Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzureRmApplicationGatewayBackendHealth Obtém a integridade do backend do Application Gateway.

## EXEMPLOS

### --------------------------Exemplo 1: Obtém a integridade do back-end sem recursos expandidos.  --------------------------
@ {Paragraph = PS C: \\ \> }



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

Esse comando obtém a integridade de back-end do gateway do aplicativo chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $BackendHealth.

### --------------------------Exemplo 1: Obtém a integridade do back-end com recursos expandidos.  --------------------------
@ {Paragraph = PS C: \\ \> }



















```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

Esse comando obtém a integridade back-end (com recursos expandidos) do Application Gateway chamada ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $BackendHealth.

## OS

### -ExpandResource
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do aplicativo do gateway que este cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém o Application Gateway.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth

## INFORMA
Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede

## LINKS RELACIONADOS

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

