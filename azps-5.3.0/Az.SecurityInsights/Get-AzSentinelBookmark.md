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
# <span data-ttu-id="82a83-101">Get-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="82a83-101">Get-AzSentinelBookmark</span></span>

## <span data-ttu-id="82a83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="82a83-102">SYNOPSIS</span></span>
<span data-ttu-id="82a83-103">Obter um indicador.</span><span class="sxs-lookup"><span data-stu-id="82a83-103">Get a Bookmark.</span></span>

## <span data-ttu-id="82a83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82a83-104">SYNTAX</span></span>

### <span data-ttu-id="82a83-105">WorkspaceScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="82a83-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a83-106">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="82a83-106">BookmarkId.</span></span>
```
Get-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82a83-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="82a83-107">ResourceId</span></span>
```
Get-AzSentinelBookmark -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82a83-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="82a83-108">DESCRIPTION</span></span>
<span data-ttu-id="82a83-109">O cmdlet **Get-AzSentinelBookmark** Obtém um indicador do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="82a83-109">The **Get-AzSentinelBookmark** cmdlet gets a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="82a83-110">Se você especificar o parâmetro *BookmarkID* , um único objeto **Bookmark** será retornado.</span><span class="sxs-lookup"><span data-stu-id="82a83-110">If you specify the *BookmarkId* parameter, a single **Bookmark** object is returned.</span></span>
<span data-ttu-id="82a83-111">Se você não especificar o parâmetro *BookmarkID* , uma matriz que contenha todos os indicadores no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="82a83-111">If you do not specify the *BookmarkId* parameter, an array containing all of the Bookmarks in the specified workspace are returned.</span></span>
<span data-ttu-id="82a83-112">Você pode usar o objeto **Bookmark** para atualizar o indicador, por exemplo, você pode adicionar anotações ao **indicador**.</span><span class="sxs-lookup"><span data-stu-id="82a83-112">You can use the **Bookmark** object to update the Bookmark, for example you can add Notes the **Bookmark**.</span></span>

## <span data-ttu-id="82a83-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82a83-113">EXAMPLES</span></span>

### <span data-ttu-id="82a83-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="82a83-114">Example 1</span></span>
```powershell
PS C:\> $Bookmarks = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="82a83-115">Este exemplo obtém todos os **indicadores** do espaço de trabalho especificado e, em seguida, armazena-os na variável $bookmarks.</span><span class="sxs-lookup"><span data-stu-id="82a83-115">This example gets all of the **Bookmarks** in the specified workspace, and then stores it in the $Bookmarks variable.</span></span>

### <span data-ttu-id="82a83-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="82a83-116">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="82a83-117">Este exemplo obtém um **indicador** no espaço de trabalho especificado e, em seguida, armazena-o na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="82a83-117">This example gets an **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="82a83-118">OS</span><span class="sxs-lookup"><span data-stu-id="82a83-118">PARAMETERS</span></span>

### <span data-ttu-id="82a83-119">-BookmarkID</span><span class="sxs-lookup"><span data-stu-id="82a83-119">-BookmarkId</span></span>
<span data-ttu-id="82a83-120">Identificação do indicador,</span><span class="sxs-lookup"><span data-stu-id="82a83-120">Bookmark Id,</span></span>

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

### <span data-ttu-id="82a83-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a83-121">-DefaultProfile</span></span>
<span data-ttu-id="82a83-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="82a83-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a83-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a83-123">-ResourceGroupName</span></span>
<span data-ttu-id="82a83-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="82a83-124">Resource group name.</span></span>

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

### <span data-ttu-id="82a83-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82a83-125">-ResourceId</span></span>
<span data-ttu-id="82a83-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="82a83-126">Resource Id.</span></span>

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

### <span data-ttu-id="82a83-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="82a83-127">-WorkspaceName</span></span>
<span data-ttu-id="82a83-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="82a83-128">Workspace Name.</span></span>

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

### <span data-ttu-id="82a83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a83-129">CommonParameters</span></span>
<span data-ttu-id="82a83-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82a83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a83-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82a83-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a83-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="82a83-132">INPUTS</span></span>

### <span data-ttu-id="82a83-133">System. String</span><span class="sxs-lookup"><span data-stu-id="82a83-133">System.String</span></span>
## <span data-ttu-id="82a83-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="82a83-134">OUTPUTS</span></span>

### <span data-ttu-id="82a83-135">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="82a83-135">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="82a83-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="82a83-136">NOTES</span></span>

## <span data-ttu-id="82a83-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82a83-137">RELATED LINKS</span></span>
