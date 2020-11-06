---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 82fdec48f2e021e33490f84a05a064fb007ac8d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428159"
---
# New-AzureRmApplicationSecurityGroup

## Sinopse
Cria um grupo de segurança do aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmApplicationSecurityGroup** cria um grupo de segurança de aplicativo.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

Este exemplo cria um grupo de segurança de aplicativo sem associações. Após a criação, as configurações de IP na interface de rede podem ser incluídas no grupo. As regras de segurança também podem se referir ao grupo como suas origens ou destinos.

## OS

### -AsJob
Executar o cmdlet em segundo plano

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Não peça confirmação se quiser substituir um recurso.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
O nome do grupo de segurança do aplicativo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos do grupo de segurança do aplicativo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Uma Hashtable que representa as marcas de recursos.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
System. Collections. Hashtable

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApplicationSecurityGroup](./Get-AzureRmApplicationSecurityGroup.md)

[Remove-AzureRmApplicationSecurityGroup](./Remove-AzureRmApplicationSecurityGroup.md)

[New-AzureRmNetworkSecurityRuleConfig](./New-AzureRmNetworkSecurityRuleConfig.md)

[Add-AzureRmNetworkSecurityRuleConfig](./Add-AzureRmNetworkSecurityRuleConfig.md)

[Set-AzureRmNetworkSecurityRuleConfig](./Set-AzureRmNetworkSecurityRuleConfig.md)

[New-AzureRmNetworkInterfaceIpConfig](./New-AzureRmNetworkInterfaceIpConfig.md)

[Add-AzureRmNetworkInterfaceIpConfig](./Add-AzureRmNetworkInterfaceIpConfig.md)

[Set-AzureRmNetworkInterfaceIpConfig](./Set-AzureRmNetworkInterfaceIpConfig.md)
