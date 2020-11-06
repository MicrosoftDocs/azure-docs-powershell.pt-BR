---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: EFBBFB60-D972-47B8-997E-B737F0CA007E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResourceGroup.md
ms.openlocfilehash: 029404938ba7a253b5130f5c807e4b66c3847d43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429127"
---
# Find-AzureRmResourceGroup

## Sinopse
Procura por grupos de recursos.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Find-AzureRmResourceGroup [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Find-AzureRmResourceGroup** procura por grupos de recursos usando os parâmetros especificados.

## EXEMPLOS

### Exemplo 1: localizar todos os grupos de recursos
```
PS C:\>Find-AzureRmResourceGroup
```

Esse comando localiza todos os grupos de recursos.

### Exemplo 2: localizar grupos de recursos por nome da marca
```
PS C:\>Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
```

Esse comando localiza todos os grupos de recursos que têm uma marca chamada testtag.

### Exemplo 3: localizar grupos de recursos por nome e valor da marca
```
PS C:\>Find-AzureRmResourceGroup -Tag @{"testtag" = "testval" }
```

Esse comando localiza todos os grupos de recursos que têm uma marca chamada testtag e o valor testval.

## OS

### -ApiVersion
Especifica a versão da API do provedor de recursos a ser usada. Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre
Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Especifica as informações de marca como uma tabela de hash para filtrar seus resultados. Use os seguintes formatos:

@ {tagName = $null} ou @ {tagName = ' tagValue '}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
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

## EXIBE

### System. Management. Automation. PSObject

## INFORMA

## LINKS RELACIONADOS

