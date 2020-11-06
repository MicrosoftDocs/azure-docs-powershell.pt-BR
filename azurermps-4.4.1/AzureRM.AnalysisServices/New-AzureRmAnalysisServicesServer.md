---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 0093393f926af257e07b7d697a7f267fa62b483a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427052"
---
# New-AzureRmAnalysisServicesServer

## Sinopse
Cria um novo servidor do Analysis Services

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzureRmAnalysisServicesServer cria um novo servidor do Analysis Services

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

Cria um servidor chamado TestServer na região do Azure West-US e no grupo de recursos testresrourcegroup. O nível de SKU do servidor será S1.

## OS

### -Administrador
Uma cadeia de caracteres que representa uma lista separada por vírgulas de usuários ou grupos a serem definidos como administradores no servidor. Os usuários ou grupos precisam ser do formato UPN especificado, por exemplo, user@contoso.com ou groups@contoso.com

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupBlobContainerUri
O URI do contêiner de BLOB para fazer backup do servidor do Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
A região do Azure na qual o servidor do Analysis Services está hospedado

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: North Central US, South Central US, Central US, West Europe, North Europe, West US, East US, East US 2, Japan East, Japan West, Brazil South, Southeast Asia, East Asia, Australia East, Australia Southeast

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Nome do servidor do Analysis Services

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos do Azure ao qual o servidor pertence

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
O nome da SKU do servidor.
Os valores compatíveis são 0 ', 1 ', 2 ' são 4 ' para o nível padrão; ' B1 ', ' B2 ' para a camada básica e 1 ' para o nível de desenvolvimento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita que o usuário confirme se deseja executar a operação

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
Descreve as ações que a operação atual executará sem realmente executá-las

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

## EXIBE

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer

## INFORMA
Alias: New-AzureAs

## LINKS RELACIONADOS

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[Remove-AzureRmAnalysisServicesServer](./Remove-AzureRmAnalysisServicesServer.md)
