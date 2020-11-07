---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
ms.openlocfilehash: b85d22d1030eaa12e58cded1c7225231c7e8b964
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785415"
---
# Get-AzureRmAppServicePlan

## Sinopse
Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Eles
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmAppServicePlan** Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.

## EXEMPLOS

### Exemplo 1: obter um plano do serviço de aplicativo de um grupo de recursos
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

Esse comando obtém o plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.

### Exemplo 2: obter todos os planos do serviço de aplicativo em um local
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

Esse comando obtém todos os planos do serviço de aplicativo localizado na região "oeste dos EUA".

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

### -Local
Ponto 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do plano do serviço de aplicativo

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku

### Microsoft. Azure. Management. WebSites. Models. ServerFarmCollection

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmAppServicePlan](./New-AzureRmAppServicePlan.md)

[Remove-AzureRmAppServicePlan](./Remove-AzureRmAppServicePlan.md)

[Set-AzureRmAppServicePlan](./Set-AzureRmAppServicePlan.md)


