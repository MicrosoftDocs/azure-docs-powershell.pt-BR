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
# <span data-ttu-id="44984-101">Update-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="44984-101">Update-AzSentinelBookmark</span></span>

## <span data-ttu-id="44984-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44984-102">SYNOPSIS</span></span>
<span data-ttu-id="44984-103">Atualizar um indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-103">Update a Bookmark.</span></span>

## <span data-ttu-id="44984-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44984-104">SYNTAX</span></span>

### <span data-ttu-id="44984-105">BookmarkID.</span><span class="sxs-lookup"><span data-stu-id="44984-105">BookmarkId.</span></span> <span data-ttu-id="44984-106">Assume</span><span class="sxs-lookup"><span data-stu-id="44984-106">(Default)</span></span>
```
Update-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> -BookmarkId <String>
 [-DisplayName <String>] [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] [-Query <String>]
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44984-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="44984-107">InputObject</span></span>
```
Update-AzSentinelBookmark -InputObject <PSSentinelBookmark> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44984-108">Identificação</span><span class="sxs-lookup"><span data-stu-id="44984-108">ResourceId</span></span>
```
Update-AzSentinelBookmark -ResourceId <String> [-DisplayName <String>]
 [-IncidentInfo <PSSentinelBookmarkIncidentInfo>] [-Label <System.Collections.Generic.IList`1[System.String]>]
 [-Notes <String>] [-Query <String>] [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44984-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44984-109">DESCRIPTION</span></span>
<span data-ttu-id="44984-110">O cmdlet **Update-AzSentinelBookmark** atualiza o indicador no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="44984-110">The **Update-AzSentinelBookmark** cmdlet updates the bookmark in the specified workspace.</span></span>
<span data-ttu-id="44984-111">Você pode passar um objeto **Bookmark** como um parâmetro ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros *BookmarkID* obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="44984-111">You can pass an **Bookmark** object as a parameter or by using the pipeline operator, or alternatively you can specify the required *BookmarkId* parameters.</span></span>
<span data-ttu-id="44984-112">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="44984-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="44984-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44984-113">EXAMPLES</span></span>

### <span data-ttu-id="44984-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44984-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId" -Notes "Found something interesting"
```

<span data-ttu-id="44984-115">O comando atualiza o indicador definindo a propriedade *Notes* .</span><span class="sxs-lookup"><span data-stu-id="44984-115">The command updates the Bookmark by setting the *Notes* property.</span></span>  <span data-ttu-id="44984-116">Todas as outras Propreties permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="44984-116">All other propreties stay the same.</span></span>

### <span data-ttu-id="44984-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="44984-117">Example 2</span></span>
```powershell
PS C:\> $Bookmark = Get-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceNAme" -BookmarkId "MyBookmarkId"
PS C:\> $Bookmark | Set-AzSentinelBookmark -Notes "Found something interesting"
```

<span data-ttu-id="44984-118">O primeiro comando obtém o indicador por *BookmarkID* do espaço de trabalho especificado e, em seguida, armazena-o na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="44984-118">The first command gets the Bookmark by *BookmarkId* from the specified workspace, and then stores it in the $Bookmark variable.</span></span>
<span data-ttu-id="44984-119">O segundo comando atualiza a propriedade Notes.</span><span class="sxs-lookup"><span data-stu-id="44984-119">The second command updates the Notes property.</span></span>   <span data-ttu-id="44984-120">Todas as outras Propreties permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="44984-120">All other propreties stay the same.</span></span>

## <span data-ttu-id="44984-121">OS</span><span class="sxs-lookup"><span data-stu-id="44984-121">PARAMETERS</span></span>

### <span data-ttu-id="44984-122">-BookmarkID</span><span class="sxs-lookup"><span data-stu-id="44984-122">-BookmarkId</span></span>
<span data-ttu-id="44984-123">Identificação do indicador,</span><span class="sxs-lookup"><span data-stu-id="44984-123">Bookmark Id,</span></span>

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

### <span data-ttu-id="44984-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44984-124">-DefaultProfile</span></span>
<span data-ttu-id="44984-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44984-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44984-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="44984-126">-DisplayName</span></span>
<span data-ttu-id="44984-127">Nome de exibição da regra de indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-127">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="44984-128">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="44984-128">-IncidentInfo</span></span>
<span data-ttu-id="44984-129">Informações do incidente de indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-129">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="44984-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44984-130">-InputObject</span></span>
<span data-ttu-id="44984-131">InputObject.</span><span class="sxs-lookup"><span data-stu-id="44984-131">InputObject.</span></span>

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

### <span data-ttu-id="44984-132">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="44984-132">-Label</span></span>
<span data-ttu-id="44984-133">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="44984-133">Incident Labels.</span></span>

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

### <span data-ttu-id="44984-134">-Observações</span><span class="sxs-lookup"><span data-stu-id="44984-134">-Notes</span></span>
<span data-ttu-id="44984-135">Anotações de indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-135">Bookmark Notes.</span></span>

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

### <span data-ttu-id="44984-136">-Consulta</span><span class="sxs-lookup"><span data-stu-id="44984-136">-Query</span></span>
<span data-ttu-id="44984-137">Consulta de indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-137">Bookmark Query.</span></span>

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

### <span data-ttu-id="44984-138">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="44984-138">-QueryResult</span></span>
<span data-ttu-id="44984-139">Resultado da consulta de indicador.</span><span class="sxs-lookup"><span data-stu-id="44984-139">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="44984-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44984-140">-ResourceGroupName</span></span>
<span data-ttu-id="44984-141">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44984-141">Resource group name.</span></span>

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

### <span data-ttu-id="44984-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44984-142">-ResourceId</span></span>
<span data-ttu-id="44984-143">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="44984-143">Resource Id.</span></span>

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

### <span data-ttu-id="44984-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44984-144">-WorkspaceName</span></span>
<span data-ttu-id="44984-145">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="44984-145">Workspace Name.</span></span>

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

### <span data-ttu-id="44984-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44984-146">-Confirm</span></span>
<span data-ttu-id="44984-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44984-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44984-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44984-148">-WhatIf</span></span>
<span data-ttu-id="44984-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44984-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44984-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44984-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44984-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44984-151">CommonParameters</span></span>
<span data-ttu-id="44984-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44984-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44984-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44984-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44984-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44984-154">INPUTS</span></span>

### <span data-ttu-id="44984-155">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="44984-155">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

### <span data-ttu-id="44984-156">System. String</span><span class="sxs-lookup"><span data-stu-id="44984-156">System.String</span></span>

### <span data-ttu-id="44984-157">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="44984-157">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>

## <span data-ttu-id="44984-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44984-158">OUTPUTS</span></span>

### <span data-ttu-id="44984-159">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="44984-159">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>

## <span data-ttu-id="44984-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44984-160">NOTES</span></span>

## <span data-ttu-id="44984-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44984-161">RELATED LINKS</span></span>
