---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: ed75d128053a4b08fc7d63a4ef8b02254d868408
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888654"
---
# <span data-ttu-id="52b17-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="52b17-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="52b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b17-102">SYNOPSIS</span></span>
<span data-ttu-id="52b17-103">Excluir um Indicador.</span><span class="sxs-lookup"><span data-stu-id="52b17-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="52b17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52b17-104">SYNTAX</span></span>

### <span data-ttu-id="52b17-105">BookmarkId.</span><span class="sxs-lookup"><span data-stu-id="52b17-105">BookmarkId.</span></span> <span data-ttu-id="52b17-106">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="52b17-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52b17-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="52b17-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52b17-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52b17-108">DESCRIPTION</span></span>
<span data-ttu-id="52b17-109">O cmdlet **Remove-AzSentinelBookmark** exclui permanentemente um Indicador de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="52b17-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="52b17-110">Você pode passar um **objeto Bookmark** usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="52b17-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="52b17-111">Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="52b17-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="52b17-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52b17-112">EXAMPLES</span></span>

### <span data-ttu-id="52b17-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52b17-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="52b17-114">Este comando remove o Indicador do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="52b17-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="52b17-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52b17-115">PARAMETERS</span></span>

### <span data-ttu-id="52b17-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="52b17-116">-BookmarkId</span></span>
<span data-ttu-id="52b17-117">Id do indicador,</span><span class="sxs-lookup"><span data-stu-id="52b17-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="52b17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b17-118">-DefaultProfile</span></span>
<span data-ttu-id="52b17-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52b17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b17-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52b17-120">-InputObject</span></span>
<span data-ttu-id="52b17-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="52b17-121">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b17-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52b17-122">-PassThru</span></span>
<span data-ttu-id="52b17-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="52b17-123">PassThru</span></span>

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

### <span data-ttu-id="52b17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b17-124">-ResourceGroupName</span></span>
<span data-ttu-id="52b17-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52b17-125">Resource group name.</span></span>

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

### <span data-ttu-id="52b17-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="52b17-126">-WorkspaceName</span></span>
<span data-ttu-id="52b17-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="52b17-127">Workspace Name.</span></span>

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

### <span data-ttu-id="52b17-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52b17-128">-Confirm</span></span>
<span data-ttu-id="52b17-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52b17-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b17-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52b17-130">-WhatIf</span></span>
<span data-ttu-id="52b17-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52b17-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52b17-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52b17-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b17-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b17-133">CommonParameters</span></span>
<span data-ttu-id="52b17-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b17-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b17-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52b17-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b17-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52b17-136">INPUTS</span></span>

### <span data-ttu-id="52b17-137">System.String</span><span class="sxs-lookup"><span data-stu-id="52b17-137">System.String</span></span>
### <span data-ttu-id="52b17-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="52b17-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="52b17-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52b17-139">OUTPUTS</span></span>

### <span data-ttu-id="52b17-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="52b17-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="52b17-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="52b17-141">NOTES</span></span>

## <span data-ttu-id="52b17-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52b17-142">RELATED LINKS</span></span>
