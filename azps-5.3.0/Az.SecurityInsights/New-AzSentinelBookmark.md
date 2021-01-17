---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 3c30edd841eb2e773c5d813e798e63fc9858437d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433207"
---
# <span data-ttu-id="87c6b-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="87c6b-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="87c6b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="87c6b-103">Criar um indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-103">Create a Bookmark.</span></span>

## <span data-ttu-id="87c6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87c6b-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c6b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="87c6b-106">O cmdlet **New-AzSentinelBookmark** cria um indicador do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="87c6b-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="87c6b-107">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="87c6b-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="87c6b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87c6b-108">EXAMPLES</span></span>

### <span data-ttu-id="87c6b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87c6b-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="87c6b-110">Este exemplo cria um **indicador** no espaço de trabalho especificado e, em seguida, armazena-o na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="87c6b-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="87c6b-111">OS</span><span class="sxs-lookup"><span data-stu-id="87c6b-111">PARAMETERS</span></span>

### <span data-ttu-id="87c6b-112">-BookmarkID</span><span class="sxs-lookup"><span data-stu-id="87c6b-112">-BookmarkId</span></span>
<span data-ttu-id="87c6b-113">Identificação do indicador,</span><span class="sxs-lookup"><span data-stu-id="87c6b-113">Bookmark Id,</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c6b-114">-DefaultProfile</span></span>
<span data-ttu-id="87c6b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87c6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c6b-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="87c6b-116">-DisplayName</span></span>
<span data-ttu-id="87c6b-117">Nome de exibição da regra de indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-117">Bookmark Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="87c6b-118">-IncidentInfo</span></span>
<span data-ttu-id="87c6b-119">Informações do incidente de indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-119">Bookmark Incident Info.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-120">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="87c6b-120">-Label</span></span>
<span data-ttu-id="87c6b-121">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="87c6b-121">Incident Labels.</span></span>

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

### <span data-ttu-id="87c6b-122">-Observações</span><span class="sxs-lookup"><span data-stu-id="87c6b-122">-Notes</span></span>
<span data-ttu-id="87c6b-123">Anotações de indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-123">Bookmark Notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-124">-Consulta</span><span class="sxs-lookup"><span data-stu-id="87c6b-124">-Query</span></span>
<span data-ttu-id="87c6b-125">Consulta de indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-125">Bookmark Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="87c6b-126">-QueryResult</span></span>
<span data-ttu-id="87c6b-127">Resultado da consulta de indicador.</span><span class="sxs-lookup"><span data-stu-id="87c6b-127">Bookmark Query Result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="87c6b-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87c6b-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="87c6b-130">-WorkspaceName</span></span>
<span data-ttu-id="87c6b-131">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="87c6b-131">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87c6b-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87c6b-132">-Confirm</span></span>
<span data-ttu-id="87c6b-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87c6b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c6b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c6b-134">-WhatIf</span></span>
<span data-ttu-id="87c6b-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87c6b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="87c6b-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87c6b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c6b-137">CommonParameters</span></span>
<span data-ttu-id="87c6b-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c6b-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87c6b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c6b-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87c6b-140">INPUTS</span></span>

### <span data-ttu-id="87c6b-141">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="87c6b-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="87c6b-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87c6b-142">OUTPUTS</span></span>

### <span data-ttu-id="87c6b-143">Microsoft. Azure. Commands. SecurityInsights. Models. Bookmarks. PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="87c6b-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="87c6b-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87c6b-144">NOTES</span></span>

## <span data-ttu-id="87c6b-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87c6b-145">RELATED LINKS</span></span>
