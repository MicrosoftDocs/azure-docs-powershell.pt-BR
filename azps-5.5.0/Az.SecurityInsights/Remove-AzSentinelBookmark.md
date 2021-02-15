---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelBookmark.md
ms.openlocfilehash: 544c019fd52c0cb5723cbeafb5a82df072ac284e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114519"
---
# <span data-ttu-id="c8026-101">Remove-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c8026-101">Remove-AzSentinelBookmark</span></span>

## <span data-ttu-id="c8026-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8026-102">SYNOPSIS</span></span>
<span data-ttu-id="c8026-103">Excluir um Indicador.</span><span class="sxs-lookup"><span data-stu-id="c8026-103">Delete a Bookmark.</span></span>

## <span data-ttu-id="c8026-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8026-104">SYNTAX</span></span>

### <span data-ttu-id="c8026-105">Bookmarkid.</span><span class="sxs-lookup"><span data-stu-id="c8026-105">BookmarkId.</span></span> <span data-ttu-id="c8026-106">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8026-106">(Default)</span></span>
```
Remove-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8026-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8026-107">InputObject</span></span>
```
Remove-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8026-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8026-108">DESCRIPTION</span></span>
<span data-ttu-id="c8026-109">O **cmdlet Remove-AzSentinelBookmark** exclui permanentemente um Indicador de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="c8026-109">The **Remove-AzSentinelBookmark** cmdlet permanently deletes a Bookmark from a specified workspace.</span></span>
<span data-ttu-id="c8026-110">Você pode passar um **objeto indicador** usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="c8026-110">You can pass an **Bookmark** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="c8026-111">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="c8026-111">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c8026-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8026-112">EXAMPLES</span></span>

### <span data-ttu-id="c8026-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8026-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -BookmarkId "MyBookmarkId"
```

<span data-ttu-id="c8026-114">Esse comando remove o Indicador do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8026-114">This command removes the Bookmark from the workspace.</span></span>

## <span data-ttu-id="c8026-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8026-115">PARAMETERS</span></span>

### <span data-ttu-id="c8026-116">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="c8026-116">-BookmarkId</span></span>
<span data-ttu-id="c8026-117">ID do Indicador,</span><span class="sxs-lookup"><span data-stu-id="c8026-117">Bookmark Id,</span></span>

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

### <span data-ttu-id="c8026-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8026-118">-DefaultProfile</span></span>
<span data-ttu-id="c8026-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8026-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8026-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8026-120">-InputObject</span></span>
<span data-ttu-id="c8026-121">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="c8026-121">InputObject.</span></span>

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

### <span data-ttu-id="c8026-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8026-122">-PassThru</span></span>
<span data-ttu-id="c8026-123">Passthru</span><span class="sxs-lookup"><span data-stu-id="c8026-123">PassThru</span></span>

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

### <span data-ttu-id="c8026-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8026-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8026-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8026-125">Resource group name.</span></span>

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

### <span data-ttu-id="c8026-126">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c8026-126">-WorkspaceName</span></span>
<span data-ttu-id="c8026-127">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8026-127">Workspace Name.</span></span>

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

### <span data-ttu-id="c8026-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8026-128">-Confirm</span></span>
<span data-ttu-id="c8026-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8026-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8026-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8026-130">-WhatIf</span></span>
<span data-ttu-id="c8026-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8026-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8026-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8026-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8026-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8026-133">CommonParameters</span></span>
<span data-ttu-id="c8026-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8026-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8026-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8026-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8026-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8026-136">INPUTS</span></span>

### <span data-ttu-id="c8026-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c8026-137">System.String</span></span>
### <span data-ttu-id="c8026-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c8026-138">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="c8026-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8026-139">OUTPUTS</span></span>

### <span data-ttu-id="c8026-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="c8026-140">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="c8026-141">Notas</span><span class="sxs-lookup"><span data-stu-id="c8026-141">NOTES</span></span>

## <span data-ttu-id="c8026-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8026-142">RELATED LINKS</span></span>
