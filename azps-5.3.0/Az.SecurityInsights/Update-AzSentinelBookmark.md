---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433183"
---
# Update-AzSentinelBookmark

## Sinopse
Atualizar um indicador.

## SYNTAX

### BookmarkID. Assume
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identificação
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzSentinelBookmark** atualiza o indicador no espaço de trabalho especificado.
Você pode passar um objeto **Bookmark** como um parâmetro ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros *BookmarkID* obrigatórios.
Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

O comando atualiza o indicador definindo a propriedade *Notes* .  Todas as outras Propreties permanecem as mesmas.

### Exemplo 2
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

O primeiro comando obtém o indicador por *BookmarkID* do espaço de trabalho especificado e, em seguida, armazena-o na variável $Bookmark.
O segundo comando atualiza a propriedade Notes.   Todas as outras Propreties permanecem as mesmas.

## OS

### -BookmarkID
Identificação do indicador,

```yaml
Type: String
Parameter Sets: BookmarkId., ParentObject
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Nome de exibição da regra de indicador.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncidentInfo
Informações do incidente de indicador.

```yaml
Type: PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InputObject
InputObject.

```yaml
Type: PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Rótulo
Rótulos de incidentes.

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Observações
Anotações de indicador.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Consulta
Consulta de indicador.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QueryResult
Resultado da consulta de indicador.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: BookmarkId.
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
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WorkspaceName
Nome do espaço de trabalho.

```yaml
Type: String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark

### System. String

### Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmarkIncidentInfo

## EXIBE

### Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark

## INFORMA

## LINKS RELACIONADOS
