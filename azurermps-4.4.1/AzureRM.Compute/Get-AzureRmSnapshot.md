---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428269"
---
# Get-AzureRmSnapshot

## Sinopse
Obtém as propriedades de um instantâneo

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmSnapshot** Obtém as propriedades de um instantâneo.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Get-AzureRmSnapshot
```

Este comando obtém as propriedades de todos os instantâneos da assinatura.

### Exemplo 2
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

Esse comando obtém as propriedades de todos os instantâneos no grupo de recursos chamado "ResourceGroupName1"

### Exemplo 3
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

Este comando obtém as propriedades do instantâneo chamado "SnapshotName1" no grupo de recursos chamado "ResourceGroupName1"

## OS

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

### -ResourceGroupName
Especifica o nome de um grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Instantâneoname
Especifica o nome de um instantâneo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### System. Object

## INFORMA

## LINKS RELACIONADOS

