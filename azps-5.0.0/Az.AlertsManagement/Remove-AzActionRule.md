---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117947"
---
# <span data-ttu-id="af86a-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="af86a-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="af86a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af86a-102">SYNOPSIS</span></span>
<span data-ttu-id="af86a-103">Exclui uma regra de ação</span><span class="sxs-lookup"><span data-stu-id="af86a-103">Deletes a action rule</span></span>

## <span data-ttu-id="af86a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af86a-104">SYNTAX</span></span>

### <span data-ttu-id="af86a-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="af86a-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af86a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af86a-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af86a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af86a-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af86a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="af86a-108">DESCRIPTION</span></span>
<span data-ttu-id="af86a-109">O cmdlet **Remove-AzActionRule** exclui uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="af86a-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="af86a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af86a-110">EXAMPLES</span></span>

### <span data-ttu-id="af86a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af86a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="af86a-112">Este cmdlet exclui a regra de ação com o nome ActionRuleName no teste do grupo de recursos-RG</span><span class="sxs-lookup"><span data-stu-id="af86a-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="af86a-113">OS</span><span class="sxs-lookup"><span data-stu-id="af86a-113">PARAMETERS</span></span>

### <span data-ttu-id="af86a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af86a-114">-DefaultProfile</span></span>
<span data-ttu-id="af86a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af86a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af86a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af86a-116">-InputObject</span></span>
<span data-ttu-id="af86a-117">O recurso regra de ação</span><span class="sxs-lookup"><span data-stu-id="af86a-117">The action rule resource</span></span>

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

### <span data-ttu-id="af86a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="af86a-118">-Name</span></span>
<span data-ttu-id="af86a-119">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="af86a-119">Name of action rule</span></span>

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

### <span data-ttu-id="af86a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af86a-120">-PassThru</span></span>
<span data-ttu-id="af86a-121">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="af86a-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="af86a-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="af86a-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af86a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af86a-123">-ResourceGroupName</span></span>
<span data-ttu-id="af86a-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="af86a-124">Resource Group name</span></span>

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

### <span data-ttu-id="af86a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af86a-125">-ResourceId</span></span>
<span data-ttu-id="af86a-126">Obter regra de ação por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="af86a-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="af86a-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="af86a-127">-Confirm</span></span>
<span data-ttu-id="af86a-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af86a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af86a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af86a-129">-WhatIf</span></span>
<span data-ttu-id="af86a-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af86a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af86a-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af86a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af86a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af86a-132">CommonParameters</span></span>
<span data-ttu-id="af86a-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af86a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af86a-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af86a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af86a-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="af86a-135">INPUTS</span></span>

### <span data-ttu-id="af86a-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="af86a-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="af86a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="af86a-137">OUTPUTS</span></span>

### <span data-ttu-id="af86a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af86a-138">System.Boolean</span></span>

## <span data-ttu-id="af86a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="af86a-139">NOTES</span></span>

## <span data-ttu-id="af86a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af86a-140">RELATED LINKS</span></span>
