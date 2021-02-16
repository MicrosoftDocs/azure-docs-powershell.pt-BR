---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelBookmark.md
ms.openlocfilehash: ebc0ffd78f653276e66b85d263db41803a48c356
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116395"
---
# <span data-ttu-id="9a4a8-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9a4a8-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="9a4a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4a8-103">Atualizar um Indicador.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-103">Update a Bookmark.</span></span>

## <span data-ttu-id="9a4a8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a4a8-104">SYNTAX</span></span>

### <span data-ttu-id="9a4a8-105">Bookmarkid.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-105">BookmarkId.</span></span> <span data-ttu-id="9a4a8-106">(Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4a8-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9a4a8-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a4a8-108">Resourceid</span><span class="sxs-lookup"><span data-stu-id="9a4a8-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a4a8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a4a8-109">DESCRIPTION</span></span>
<span data-ttu-id="9a4a8-110">O cmdlet **Update-AzSentinelBookmark** atualiza o indicador no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="9a4a8-111">Você pode  passar um objeto indicador como um parâmetro ou usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros *indicadores necessários.*</span><span class="sxs-lookup"><span data-stu-id="9a4a8-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="9a4a8-112">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9a4a8-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a4a8-113">EXAMPLES</span></span>

### <span data-ttu-id="9a4a8-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9a4a8-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="9a4a8-115">O comando atualiza o Indicador configurando a *propriedade Anotações.*</span><span class="sxs-lookup"><span data-stu-id="9a4a8-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="9a4a8-116">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="9a4a8-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9a4a8-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="9a4a8-118">O primeiro comando obtém o Indicador por *BookmarkId* do espaço de trabalho especificado e o armazena na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="9a4a8-119">O segundo comando atualiza a propriedade Anotações.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="9a4a8-120">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="9a4a8-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a4a8-121">PARAMETERS</span></span>

### <span data-ttu-id="9a4a8-122">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="9a4a8-122">-BookmarkId</span></span>
<span data-ttu-id="9a4a8-123">ID do Indicador,</span><span class="sxs-lookup"><span data-stu-id="9a4a8-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="9a4a8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4a8-124">-DefaultProfile</span></span>
<span data-ttu-id="9a4a8-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a4a8-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a4a8-126">-DisplayName</span></span>
<span data-ttu-id="9a4a8-127">Nome de exibição da regra de indicador.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="9a4a8-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-128">-IncidentInfo</span></span>
<span data-ttu-id="9a4a8-129">Informações sobre incidentes de indicadores.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="9a4a8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a4a8-130">-InputObject</span></span>
<span data-ttu-id="9a4a8-131">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-131">InputObject.</span></span>

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

### <span data-ttu-id="9a4a8-132">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-132">-Label</span></span>
<span data-ttu-id="9a4a8-133">Rótulos de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-133">Incident Labels.</span></span>

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

### <span data-ttu-id="9a4a8-134">-Anotações</span><span class="sxs-lookup"><span data-stu-id="9a4a8-134">-Notes</span></span>
<span data-ttu-id="9a4a8-135">Anotações do Indicador.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="9a4a8-136">-Consulta</span><span class="sxs-lookup"><span data-stu-id="9a4a8-136">-Query</span></span>
<span data-ttu-id="9a4a8-137">Consulta de Indicadores.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="9a4a8-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="9a4a8-138">-QueryResult</span></span>
<span data-ttu-id="9a4a8-139">Resultado da Consulta de Indicadores.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="9a4a8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a4a8-140">-ResourceGroupName</span></span>
<span data-ttu-id="9a4a8-141">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-141">Resource group name.</span></span>

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

### <span data-ttu-id="9a4a8-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a4a8-142">-ResourceId</span></span>
<span data-ttu-id="9a4a8-143">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-143">Resource Id.</span></span>

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

### <span data-ttu-id="9a4a8-144">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="9a4a8-144">-WorkspaceName</span></span>
<span data-ttu-id="9a4a8-145">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-145">Workspace Name.</span></span>

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

### <span data-ttu-id="9a4a8-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9a4a8-146">-Confirm</span></span>
<span data-ttu-id="9a4a8-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a4a8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a4a8-148">-WhatIf</span></span>
<span data-ttu-id="9a4a8-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a4a8-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a4a8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4a8-151">CommonParameters</span></span>
<span data-ttu-id="9a4a8-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4a8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4a8-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a4a8-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4a8-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a4a8-154">INPUTS</span></span>

### <span data-ttu-id="9a4a8-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9a4a8-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="9a4a8-156">System.String</span><span class="sxs-lookup"><span data-stu-id="9a4a8-156">System.String</span></span>

### <span data-ttu-id="9a4a8-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="9a4a8-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="9a4a8-158">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a4a8-158">OUTPUTS</span></span>

### <span data-ttu-id="9a4a8-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="9a4a8-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="9a4a8-160">Notas</span><span class="sxs-lookup"><span data-stu-id="9a4a8-160">NOTES</span></span>

## <span data-ttu-id="9a4a8-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a4a8-161">RELATED LINKS</span></span>
