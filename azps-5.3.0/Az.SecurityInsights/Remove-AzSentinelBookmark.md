---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433191"
---
# <span data-ttu-id="d96c3-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d96c3-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="d96c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d96c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d96c3-103">Excluir um indicador.</span><span class="sxs-lookup"><span data-stu-id="d96c3-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="d96c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d96c3-104">SYNTAX</span></span>

### <span data-ttu-id="d96c3-105">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="d96c3-105">BookmarkId.</span></span> <span data-ttu-id="d96c3-106">Assume</span><span class="sxs-lookup"><span data-stu-id="d96c3-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d96c3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d96c3-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d96c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d96c3-108">DESCRIPTION</span></span>
<span data-ttu-id="d96c3-109">O cmdlet **Remove-AzSentinelBookmark** exclui permanentemente um indicador de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d96c3-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="d96c3-110">Você pode passar um objeto **Bookmark** usando o operador pipeline ou, como alternativa, pode especificar os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d96c3-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d96c3-111">Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d96c3-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d96c3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d96c3-112">EXAMPLES</span></span>

### <span data-ttu-id="d96c3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d96c3-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="d96c3-114">Este comando Remove o indicador do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d96c3-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="d96c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="d96c3-115">PARAMETERS</span></span>

### <span data-ttu-id="d96c3-116">-BookmarkID</span><span class="sxs-lookup"><span data-stu-id="d96c3-116">-BookmarkId</span></span>
<span data-ttu-id="d96c3-117">Identificação do indicador,</span><span class="sxs-lookup"><span data-stu-id="d96c3-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="d96c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d96c3-118">-DefaultProfile</span></span>
<span data-ttu-id="d96c3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d96c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d96c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d96c3-120">-InputObject</span></span>
<span data-ttu-id="d96c3-121">InputObject.</span><span class="sxs-lookup"><span data-stu-id="d96c3-121">InputObject.</span></span>

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

### <span data-ttu-id="d96c3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d96c3-122">-PassThru</span></span>
<span data-ttu-id="d96c3-123">PassThru</span><span class="sxs-lookup"><span data-stu-id="d96c3-123">PassThru</span></span>

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

### <span data-ttu-id="d96c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d96c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="d96c3-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d96c3-125">Resource group name.</span></span>

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

### <span data-ttu-id="d96c3-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d96c3-126">-WorkspaceName</span></span>
<span data-ttu-id="d96c3-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d96c3-127">Workspace Name.</span></span>

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

### <span data-ttu-id="d96c3-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d96c3-128">-Confirm</span></span>
<span data-ttu-id="d96c3-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d96c3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d96c3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d96c3-130">-WhatIf</span></span>
<span data-ttu-id="d96c3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d96c3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d96c3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d96c3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d96c3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d96c3-133">CommonParameters</span></span>
<span data-ttu-id="d96c3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d96c3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d96c3-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d96c3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d96c3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d96c3-136">INPUTS</span></span>

### <span data-ttu-id="d96c3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d96c3-137">System.String</span></span>
### <span data-ttu-id="d96c3-138">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d96c3-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="d96c3-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d96c3-139">OUTPUTS</span></span>

### <span data-ttu-id="d96c3-140">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="d96c3-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="d96c3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d96c3-141">NOTES</span></span>

## <span data-ttu-id="d96c3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d96c3-142">RELATED LINKS</span></span>
