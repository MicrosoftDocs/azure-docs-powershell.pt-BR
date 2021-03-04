---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: ab8afdb01a2993330c75b23b02392ee583cad297
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891160"
---
# Remove-AzApplicationGatewaySslProfile

## SYNOPSIS
Remove o perfil ssl de um gateway de aplicativo.

## SINTAXE

```
Remove-AzApplicationGatewaySslProfile -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzApplicationGatewaySslProfile** remove o perfil ssl de um gateway de aplicativo.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "SslProfile01"
```

O primeiro comando obtém um gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando remove o perfil ssl chamado SslProfile01 do gateway de aplicativo armazenado em $AppGw.

## PARÂMETROS

### -ApplicationGateway
ApplicationGateway

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -Name
O nome do perfil ssl

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTES

## LINKS RELACIONADOS

[New-AzApplicationGatewaySslProfile](./New-AzApplicationGatewaySslProfile.md)

[Add-AzApplicationGatewaySslProfile](./Add-AzApplicationGatewaySslProfile.md)

[Get-AzApplicationGatewaySslProfile](./Get-AzApplicationGatewaySslProfile.md)

[Set-AzApplicationGatewaySslProfile](./Set-AzApplicationGatewaySslProfile.md)