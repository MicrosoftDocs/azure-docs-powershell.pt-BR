---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysku
schema: 2.0.0
ms.openlocfilehash: cda4281b1bf52b9f0b94926bc66590d1bd741c44
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785489"
---
# New-AzureRmApplicationGatewaySku

## Sinopse
Cria uma SKU para um gateway de aplicativo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmApplicationGatewaySku** cria uma SKU (unidade de manutenção de estoque) para um gateway do aplicativo do Azure.

## EXEMPLOS

### Exemplo 1: criar uma SKU para um gateway do aplicativo do Azure
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

Esse comando cria uma SKU chamada Standard_Small para um gateway do aplicativo do Azure e armazena o resultado na variável chamada $SKU.

## OS

### -Capacidade
Especifica o número de instâncias de um gateway de aplicativo.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Nome
Especifica o nome do SKU.

Os valores aceitáveis para esse parâmetro são:

- Standard_Small
- Standard_Medium
- Standard_Large
- WAF_Medium
- WAF_Large

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tier
Especifica o nível da SKU.
Os valores aceitáveis para esse parâmetro são:

- Oficial
- WAF

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
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

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmApplicationGatewaySku](./Get-AzureRmApplicationGatewaySku.md)

[Set-AzureRmApplicationGatewaySku](./Set-AzureRmApplicationGatewaySku.md)


