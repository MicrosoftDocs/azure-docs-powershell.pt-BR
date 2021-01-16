---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259020"
---
# Get-AzApplicationGatewaySslProfilePolicy

## Sinopse
Obtém a política SSL de um perfil de SSL do gateway do aplicativo.

## SYNTAX

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzApplicationGatewaySslProfilePolicy** Obtém a política SSL de um perfil SSL do gateway do aplicativo.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e o armazena $SslProfile variável. O último comando obtém a política SSL do perfil SSL $SslProfile e a armazena na variável $sslpolicy.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslProfile
O perfil SSL do Application Gateway

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy

## INFORMA

## LINKS RELACIONADOS

[New-AzApplicationGatewaySslProfilePolicy](./New-AzApplicationGatewaySslProfilePolicy.md)

[Add-AzApplicationGatewaySslProfilePolicy](./Add-AzApplicationGatewaySslProfilePolicy.md)

[Remove-AzApplicationGatewaySslProfilePolicy](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[Set-AzApplicationGatewaySslProfilePolicy](./Set-AzApplicationGatewaySslProfilePolicy.md)