---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelbookmark
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelBookmark.md
ms.openlocfilehash: 31c9728a95e5cfc52b283a8dddc0e24ffffe1630
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888430"
---
# <span data-ttu-id="4d0ca-101">New-AzSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="4d0ca-101">New-AzSentinelBookmark</span></span>

## <span data-ttu-id="4d0ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0ca-103">Criar um Indicador.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-103">Create a Bookmark.</span></span>

## <span data-ttu-id="4d0ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d0ca-104">SYNTAX</span></span>

```
New-AzSentinelBookmark -ResourceGroupName <String> -WorkspaceName <String> [-BookmarkId <String>]
 -DisplayName <String> [-IncidentInfo <PSSentinelBookmarkIncidentInfo>]
 [-Label <System.Collections.Generic.IList`1[System.String]>] [-Notes <String>] -Query <String>
 [-QueryResult <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d0ca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="4d0ca-106">O cmdlet **New-AzSentinelBookmark** cria um Indicador do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-106">The **New-AzSentinelBookmark** cmdlet creates a Bookmark from the specified workspace.</span></span>
<span data-ttu-id="4d0ca-107">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4d0ca-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-108">EXAMPLES</span></span>

### <span data-ttu-id="4d0ca-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d0ca-109">Example 1</span></span>
```powershell
PS C:\> $Bookmark = New-AzSentinelBookmark -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DisplayName "MyBookmark" -Query "SecurityAlert | take 1"
```

<span data-ttu-id="4d0ca-110">Este exemplo cria **um Indicador** no espaço de trabalho especificado e o armazena na variável $Bookmark.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-110">This example creates a **Bookmark** in the specified workspace, and then stores it in the $Bookmark variable.</span></span>

## <span data-ttu-id="4d0ca-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-111">PARAMETERS</span></span>

### <span data-ttu-id="4d0ca-112">-BookmarkId</span><span class="sxs-lookup"><span data-stu-id="4d0ca-112">-BookmarkId</span></span>
<span data-ttu-id="4d0ca-113">Id do indicador,</span><span class="sxs-lookup"><span data-stu-id="4d0ca-113">Bookmark Id,</span></span>

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

### <span data-ttu-id="4d0ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0ca-114">-DefaultProfile</span></span>
<span data-ttu-id="4d0ca-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d0ca-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4d0ca-116">-DisplayName</span></span>
<span data-ttu-id="4d0ca-117">Nome de exibição da regra do indicador.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-117">Bookmark Rule Display Name.</span></span>

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

### <span data-ttu-id="4d0ca-118">-IncidentInfo</span><span class="sxs-lookup"><span data-stu-id="4d0ca-118">-IncidentInfo</span></span>
<span data-ttu-id="4d0ca-119">Informações sobre incidentes do indicador.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-119">Bookmark Incident Info.</span></span>

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

### <span data-ttu-id="4d0ca-120">-Label</span><span class="sxs-lookup"><span data-stu-id="4d0ca-120">-Label</span></span>
<span data-ttu-id="4d0ca-121">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-121">Incident Labels.</span></span>

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

### <span data-ttu-id="4d0ca-122">-Notes</span><span class="sxs-lookup"><span data-stu-id="4d0ca-122">-Notes</span></span>
<span data-ttu-id="4d0ca-123">Notas de indicador.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-123">Bookmark Notes.</span></span>

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

### <span data-ttu-id="4d0ca-124">-Query</span><span class="sxs-lookup"><span data-stu-id="4d0ca-124">-Query</span></span>
<span data-ttu-id="4d0ca-125">Consulta bookmark.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-125">Bookmark Query.</span></span>

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

### <span data-ttu-id="4d0ca-126">-QueryResult</span><span class="sxs-lookup"><span data-stu-id="4d0ca-126">-QueryResult</span></span>
<span data-ttu-id="4d0ca-127">Resultado da consulta de indicador.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-127">Bookmark Query Result.</span></span>

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

### <span data-ttu-id="4d0ca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d0ca-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d0ca-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-129">Resource group name.</span></span>

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

### <span data-ttu-id="4d0ca-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d0ca-130">-WorkspaceName</span></span>
<span data-ttu-id="4d0ca-131">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-131">Workspace Name.</span></span>

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

### <span data-ttu-id="4d0ca-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d0ca-132">-Confirm</span></span>
<span data-ttu-id="4d0ca-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d0ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d0ca-134">-WhatIf</span></span>
<span data-ttu-id="4d0ca-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d0ca-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d0ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0ca-137">CommonParameters</span></span>
<span data-ttu-id="4d0ca-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0ca-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d0ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0ca-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-140">INPUTS</span></span>

### <span data-ttu-id="4d0ca-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span><span class="sxs-lookup"><span data-stu-id="4d0ca-141">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmarkIncidentInfo</span></span>
## <span data-ttu-id="4d0ca-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-142">OUTPUTS</span></span>

### <span data-ttu-id="4d0ca-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span><span class="sxs-lookup"><span data-stu-id="4d0ca-143">Microsoft.Azure.Commands.SecurityInsights.Models.Bookmarks.PSSentinelBookmark</span></span>
## <span data-ttu-id="4d0ca-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d0ca-144">NOTES</span></span>

## <span data-ttu-id="4d0ca-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d0ca-145">RELATED LINKS</span></span>
