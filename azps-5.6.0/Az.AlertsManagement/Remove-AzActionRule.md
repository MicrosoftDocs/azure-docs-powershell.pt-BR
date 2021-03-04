---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 7e34a37e0375c90fb5d36ce37c821c3b2c2fd69a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886504"
---
# <span data-ttu-id="07ce3-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="07ce3-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="07ce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="07ce3-103">Exclui uma regra de ação</span><span class="sxs-lookup"><span data-stu-id="07ce3-103">Deletes a action rule</span></span>

## <span data-ttu-id="07ce3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07ce3-104">SYNTAX</span></span>

### <span data-ttu-id="07ce3-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07ce3-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ce3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07ce3-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07ce3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07ce3-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07ce3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07ce3-108">DESCRIPTION</span></span>
<span data-ttu-id="07ce3-109">O cmdlet **Remove-AzActionRule** exclui uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="07ce3-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="07ce3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07ce3-110">EXAMPLES</span></span>

### <span data-ttu-id="07ce3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07ce3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="07ce3-112">Este cmdlet exclui a regra de ação com o nome ActionRuleName no grupo de recursos test-rg</span><span class="sxs-lookup"><span data-stu-id="07ce3-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="07ce3-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07ce3-113">PARAMETERS</span></span>

### <span data-ttu-id="07ce3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ce3-114">-DefaultProfile</span></span>
<span data-ttu-id="07ce3-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07ce3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07ce3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07ce3-116">-InputObject</span></span>
<span data-ttu-id="07ce3-117">O recurso de regra de ação</span><span class="sxs-lookup"><span data-stu-id="07ce3-117">The action rule resource</span></span>

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

### <span data-ttu-id="07ce3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="07ce3-118">-Name</span></span>
<span data-ttu-id="07ce3-119">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="07ce3-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ce3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07ce3-120">-PassThru</span></span>
<span data-ttu-id="07ce3-121">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="07ce3-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="07ce3-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="07ce3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07ce3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ce3-123">-ResourceGroupName</span></span>
<span data-ttu-id="07ce3-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="07ce3-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ce3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07ce3-125">-ResourceId</span></span>
<span data-ttu-id="07ce3-126">Get Action rule by resource id.</span><span class="sxs-lookup"><span data-stu-id="07ce3-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07ce3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07ce3-127">-Confirm</span></span>
<span data-ttu-id="07ce3-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07ce3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07ce3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07ce3-129">-WhatIf</span></span>
<span data-ttu-id="07ce3-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07ce3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07ce3-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07ce3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07ce3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ce3-132">CommonParameters</span></span>
<span data-ttu-id="07ce3-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07ce3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ce3-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07ce3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ce3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07ce3-135">INPUTS</span></span>

### <span data-ttu-id="07ce3-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="07ce3-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="07ce3-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07ce3-137">OUTPUTS</span></span>

### <span data-ttu-id="07ce3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07ce3-138">System.Boolean</span></span>

## <span data-ttu-id="07ce3-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="07ce3-139">NOTES</span></span>

## <span data-ttu-id="07ce3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07ce3-140">RELATED LINKS</span></span>
