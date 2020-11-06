---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427162"
---
# Get-AzureRmSecurityPricing

## Sinopse
Obtém os dados da camada de preços do Azure Security Center para um escopo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### SubscriptionScope (padrão)
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelResource
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelResource
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O tipo de preço da central de segurança do Azure é decidido por escopo, com esse cmdlet você pode obter os tipos de preços configurados.
O tipo de preço da assinatura inclui todos os grupos de recursos abaixo dele.
O tipo de preço do grupo de recursos substituirá o tipo de preço da assinatura.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

Obtém todas as faixas de preços configuradas para a assinatura e os grupos de recursos abaixo dela.

### Exemplo 2
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

Obtém a camada de preços configurada para o recurso de gorup de recursos "myService1".

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
Nome do recurso.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
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

### Microsoft. Azure. Commands. Security. Models. pricings. PSSecurityPricing

## INFORMA

## LINKS RELACIONADOS
