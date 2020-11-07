---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
ms.openlocfilehash: 52050426c34b30bcab867643fbb3e5b9c373f3f2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785335"
---
# Get-AzureRmApplicationSecurityGroup

## Sinopse
Obtém um grupo de segurança do aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmApplicationSecurityGroup** Obtém um grupo de segurança do aplicativo.

## EXEMPLOS

### Exemplo 1: recuperar todos os grupos de segurança do aplicativo.
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

O comando acima retorna todos os grupos de segurança do aplicativo na assinatura.

### Exemplo 2: recuperar grupos de segurança do aplicativo em um grupo de recursos.
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

O comando acima retorna todos os grupos de segurança do aplicativo que pertencem ao grupo MyResource do grupo de recursos.

### Exemplo 3: recuperar um grupo de segurança de aplicativo específico.
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

O comando acima retorna o grupo de segurança do aplicativo MyApplicationSecurityGroup sob o grupo MyResource do grupo de recursos.

## OS

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

### -Nome
O nome do recurso.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmApplicationSecurityGroup](./New-AzureRmApplicationSecurityGroup.md)

[Remove-AzureRmApplicationSecurityGroup](./Remove-AzureRmApplicationSecurityGroup.md)

[Get-AzureRmNetworkSecurityRuleConfig](./Get-AzureRmNetworkSecurityRuleConfig.md)

[Get-AzureRmNetworkInterfaceIpConfig](./Get-AzureRmNetworkInterfaceIpConfig.md)
