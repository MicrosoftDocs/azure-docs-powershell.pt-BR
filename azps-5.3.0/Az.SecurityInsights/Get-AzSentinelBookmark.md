---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 53dfedcfe4e61deb5064b20134bf063921532aec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433215"
---
# Get-AzSentinelBookmark

## Sinopse
Obter um indicador.

## SYNTAX

### WorkspaceScope (padrão)
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BookmarkID.
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSentinelBookmark** Obtém um indicador do espaço de trabalho especificado.
Se você especificar o parâmetro *BookmarkID* , um único objeto **Bookmark** será retornado.
Se você não especificar o parâmetro *BookmarkID* , uma matriz que contenha todos os indicadores no espaço de trabalho especificado será retornada.
Você pode usar o objeto **Bookmark** para atualizar o indicador, por exemplo, você pode adicionar anotações ao **indicador**.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Este exemplo obtém todos os **indicadores** do espaço de trabalho especificado e, em seguida, armazena-os na variável $bookmarks.

### Exemplo 2
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

Este exemplo obtém um **indicador** no espaço de trabalho especificado e, em seguida, armazena-o na variável $Bookmark.

## OS

### -BookmarkID
Identificação do indicador,

```yaml
Type: System.String
Parameter Sets: BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
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
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Nome do espaço de trabalho.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, BookmarkId.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String
## EXIBE

### Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark
## INFORMA

## LINKS RELACIONADOS
