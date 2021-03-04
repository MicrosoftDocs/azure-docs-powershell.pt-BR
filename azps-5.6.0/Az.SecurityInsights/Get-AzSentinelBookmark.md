---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelBookmark.md
ms.openlocfilehash: 5093f924f87f146550b13e3858f9a93b3f193ca0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892359"
---
# <span data-ttu-id="aac5a-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="aac5a-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="aac5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac5a-102">SYNOPSIS</span></span>
<span data-ttu-id="aac5a-103">Obter um Indicador.</span><span class="sxs-lookup"><span data-stu-id="aac5a-103">Get a Bookmark.</span></span>

## <span data-ttu-id="aac5a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aac5a-104">SYNTAX</span></span>

### <span data-ttu-id="aac5a-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aac5a-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac5a-106">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="aac5a-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aac5a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aac5a-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aac5a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aac5a-108">DESCRIPTION</span></span>
<span data-ttu-id="aac5a-109">O cmdlet **Get-AzSentinelBookmark** obtém um Indicador do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="aac5a-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="aac5a-110">Se você especificar o *parâmetro BookmarkId,* um único **objeto Bookmark** será retornado.</span><span class="sxs-lookup"><span data-stu-id="aac5a-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="aac5a-111">Se você não especificar o parâmetro *BookmarkId,* uma matriz contendo todos os Indicadores no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="aac5a-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="aac5a-112">Você pode usar o **objeto Bookmark** para atualizar o Indicador, por exemplo, você pode adicionar Anotações do **Indicador**.</span><span class="sxs-lookup"><span data-stu-id="aac5a-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="aac5a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aac5a-113">EXAMPLES</span></span>

### <span data-ttu-id="aac5a-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aac5a-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="aac5a-115">Este exemplo obtém todos os **Indicadores** no espaço de trabalho especificado e o armazena na variável $Bookmarks.</span><span class="sxs-lookup"><span data-stu-id="aac5a-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="aac5a-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="aac5a-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="aac5a-117">Este exemplo obtém **um Indicador** no espaço de trabalho especificado e o armazena na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="aac5a-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="aac5a-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aac5a-118">PARAMETERS</span></span>

### <span data-ttu-id="aac5a-119">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="aac5a-119">-BookmarkId</span></span>
<span data-ttu-id="aac5a-120">Id do indicador,</span><span class="sxs-lookup"><span data-stu-id="aac5a-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="aac5a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac5a-121">-DefaultProfile</span></span>
<span data-ttu-id="aac5a-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aac5a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="aac5a-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aac5a-124">Resource group name.</span></span>

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

### <span data-ttu-id="aac5a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aac5a-125">-ResourceId</span></span>
<span data-ttu-id="aac5a-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="aac5a-126">Resource Id.</span></span>

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

### <span data-ttu-id="aac5a-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aac5a-127">-WorkspaceName</span></span>
<span data-ttu-id="aac5a-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="aac5a-128">Workspace Name.</span></span>

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

### <span data-ttu-id="aac5a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac5a-129">CommonParameters</span></span>
<span data-ttu-id="aac5a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aac5a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac5a-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aac5a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac5a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aac5a-132">INPUTS</span></span>

### <span data-ttu-id="aac5a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="aac5a-133">System.String</span></span>
## <span data-ttu-id="aac5a-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aac5a-134">OUTPUTS</span></span>

### <span data-ttu-id="aac5a-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="aac5a-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="aac5a-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="aac5a-136">NOTES</span></span>

## <span data-ttu-id="aac5a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aac5a-137">RELATED LINKS</span></span>
