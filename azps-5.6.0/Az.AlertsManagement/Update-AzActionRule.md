---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890679"
---
# <span data-ttu-id="4c9a9-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="4c9a9-101">Update-AzActionRule</span></span>

## <span data-ttu-id="4c9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9a9-103">Atualiza as propriedades da regra de ação.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-103">Updates action rule properties.</span></span>

## <span data-ttu-id="4c9a9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c9a9-104">SYNTAX</span></span>

### <span data-ttu-id="4c9a9-105">ByNameSimplifiedPatch (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c9a9-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9a9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c9a9-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c9a9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c9a9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c9a9-108">DESCRIPTION</span></span>
<span data-ttu-id="4c9a9-109">O cmdlet **Update-AzActionRule** atualiza as propriedades da regra de ação - status e marcas.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="4c9a9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-110">EXAMPLES</span></span>

### <span data-ttu-id="4c9a9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c9a9-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="4c9a9-112">Este cmdlet desabilita a regra de ação.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="4c9a9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-113">PARAMETERS</span></span>

### <span data-ttu-id="4c9a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9a9-114">-DefaultProfile</span></span>
<span data-ttu-id="4c9a9-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c9a9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c9a9-116">-InputObject</span></span>
<span data-ttu-id="4c9a9-117">O recurso de regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4c9a9-118">-Name</span></span>
<span data-ttu-id="4c9a9-119">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="4c9a9-121">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c9a9-122">-ResourceId</span></span>
<span data-ttu-id="4c9a9-123">A id de recurso da regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-124">-Status</span><span class="sxs-lookup"><span data-stu-id="4c9a9-124">-Status</span></span>
<span data-ttu-id="4c9a9-125">Status da regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-125">Action rule status</span></span>

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

### <span data-ttu-id="4c9a9-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c9a9-126">-Tag</span></span>
<span data-ttu-id="4c9a9-127">Marcas de regra de ação</span><span class="sxs-lookup"><span data-stu-id="4c9a9-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c9a9-128">-Confirm</span></span>
<span data-ttu-id="4c9a9-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c9a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c9a9-130">-WhatIf</span></span>
<span data-ttu-id="4c9a9-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c9a9-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c9a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9a9-133">CommonParameters</span></span>
<span data-ttu-id="4c9a9-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9a9-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c9a9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9a9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-136">INPUTS</span></span>

### <span data-ttu-id="4c9a9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4c9a9-137">System.String</span></span>

### <span data-ttu-id="4c9a9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="4c9a9-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="4c9a9-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-139">OUTPUTS</span></span>

### <span data-ttu-id="4c9a9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="4c9a9-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="4c9a9-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c9a9-141">NOTES</span></span>

## <span data-ttu-id="4c9a9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c9a9-142">RELATED LINKS</span></span>
