---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432607"
---
# Set-AzureRmMediaService

## Sinopse
Modifica as propriedades especificadas de um serviço de mídia existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmMediaService** modifica as propriedades especificadas de um serviço de mídia existente.

## EXEMPLOS

### Exemplo 1: modificar um serviço de mídia existente
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

O primeiro comando cria uma série de marcas e armazena essas marcas na variável chamada $Tags.

Este segundo comando atualiza o serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup123 com as marcas armazenadas na variável $Tags.
O comando também usa uma matriz de objetos de configuração de armazenamento armazenados na variável $StorageAccounts.

## OS

### -AccountName
Especifica o nome do serviço de mídia que esse cmdlet modifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém o serviço de mídia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccounts
Especifica uma matriz de contas de armazenamento que este cmdlet associa ao serviço de mídia.

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marcas
Especifica as marcas do serviço de mídia.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Media. Models. PSMediaService

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmMediaService](./Get-AzureRmMediaService.md)

[New-AzureRmMediaService](./New-AzureRmMediaService.md)

[Remove-AzureRmMediaService](./Remove-AzureRmMediaService.md)


