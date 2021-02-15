---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118107"
---
# <span data-ttu-id="2562a-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="2562a-101">Update-AzActionRule</span></span>

## <span data-ttu-id="2562a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2562a-102">SYNOPSIS</span></span>
<span data-ttu-id="2562a-103">Atualiza as propriedades da regra de ação.</span><span class="sxs-lookup"><span data-stu-id="2562a-103">Updates action rule properties.</span></span>

## <span data-ttu-id="2562a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2562a-104">SYNTAX</span></span>

### <span data-ttu-id="2562a-105">ByNameSimplifiedPatch (Default)</span><span class="sxs-lookup"><span data-stu-id="2562a-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2562a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2562a-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2562a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2562a-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2562a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2562a-108">DESCRIPTION</span></span>
<span data-ttu-id="2562a-109">**O cmdlet Update-AzActionRule** atualiza as propriedades da regra de ação - status e marcas.</span><span class="sxs-lookup"><span data-stu-id="2562a-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="2562a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2562a-110">EXAMPLES</span></span>

### <span data-ttu-id="2562a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2562a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="2562a-112">Este cmdlet desabilita a regra de ação.</span><span class="sxs-lookup"><span data-stu-id="2562a-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="2562a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2562a-113">PARAMETERS</span></span>

### <span data-ttu-id="2562a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2562a-114">-DefaultProfile</span></span>
<span data-ttu-id="2562a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2562a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2562a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2562a-116">-InputObject</span></span>
<span data-ttu-id="2562a-117">O recurso de regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-117">The action rule resource</span></span>

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

### <span data-ttu-id="2562a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2562a-118">-Name</span></span>
<span data-ttu-id="2562a-119">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-119">Action rule name</span></span>

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

### <span data-ttu-id="2562a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2562a-120">-ResourceGroupName</span></span>
<span data-ttu-id="2562a-121">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-121">Action rule name</span></span>

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

### <span data-ttu-id="2562a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2562a-122">-ResourceId</span></span>
<span data-ttu-id="2562a-123">A ID de recurso da regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="2562a-124">-Status</span><span class="sxs-lookup"><span data-stu-id="2562a-124">-Status</span></span>
<span data-ttu-id="2562a-125">Status da regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-125">Action rule status</span></span>

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

### <span data-ttu-id="2562a-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2562a-126">-Tag</span></span>
<span data-ttu-id="2562a-127">Marcas de regra de ação</span><span class="sxs-lookup"><span data-stu-id="2562a-127">Action rule tags</span></span>

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

### <span data-ttu-id="2562a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2562a-128">-Confirm</span></span>
<span data-ttu-id="2562a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2562a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2562a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2562a-130">-WhatIf</span></span>
<span data-ttu-id="2562a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2562a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2562a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2562a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2562a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2562a-133">CommonParameters</span></span>
<span data-ttu-id="2562a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2562a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2562a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2562a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2562a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="2562a-136">INPUTS</span></span>

### <span data-ttu-id="2562a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2562a-137">System.String</span></span>

### <span data-ttu-id="2562a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2562a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2562a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="2562a-139">OUTPUTS</span></span>

### <span data-ttu-id="2562a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="2562a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="2562a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="2562a-141">NOTES</span></span>

## <span data-ttu-id="2562a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2562a-142">RELATED LINKS</span></span>
