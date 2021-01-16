---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263364"
---
# <span data-ttu-id="c1f0d-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="c1f0d-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="c1f0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f0d-103">Exclui uma regra de ação</span><span class="sxs-lookup"><span data-stu-id="c1f0d-103">Deletes a action rule</span></span>

## <span data-ttu-id="c1f0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1f0d-104">SYNTAX</span></span>

### <span data-ttu-id="c1f0d-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1f0d-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f0d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f0d-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1f0d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1f0d-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1f0d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1f0d-108">DESCRIPTION</span></span>
<span data-ttu-id="c1f0d-109">O cmdlet **Remove-AzActionRule** exclui uma regra de ação.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="c1f0d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1f0d-110">EXAMPLES</span></span>

### <span data-ttu-id="c1f0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1f0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="c1f0d-112">Este cmdlet exclui a regra de ação com o nome ActionRuleName no teste do grupo de recursos-RG</span><span class="sxs-lookup"><span data-stu-id="c1f0d-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="c1f0d-113">OS</span><span class="sxs-lookup"><span data-stu-id="c1f0d-113">PARAMETERS</span></span>

### <span data-ttu-id="c1f0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f0d-114">-DefaultProfile</span></span>
<span data-ttu-id="c1f0d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1f0d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1f0d-116">-InputObject</span></span>
<span data-ttu-id="c1f0d-117">O recurso regra de ação</span><span class="sxs-lookup"><span data-stu-id="c1f0d-117">The action rule resource</span></span>

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

### <span data-ttu-id="c1f0d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1f0d-118">-Name</span></span>
<span data-ttu-id="c1f0d-119">Nome da regra de ação</span><span class="sxs-lookup"><span data-stu-id="c1f0d-119">Name of action rule</span></span>

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

### <span data-ttu-id="c1f0d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1f0d-120">-PassThru</span></span>
<span data-ttu-id="c1f0d-121">PassThru retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c1f0d-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1f0d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f0d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1f0d-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c1f0d-124">Resource Group name</span></span>

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

### <span data-ttu-id="c1f0d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f0d-125">-ResourceId</span></span>
<span data-ttu-id="c1f0d-126">Obter regra de ação por ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="c1f0d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c1f0d-127">-Confirm</span></span>
<span data-ttu-id="c1f0d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f0d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f0d-129">-WhatIf</span></span>
<span data-ttu-id="c1f0d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f0d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1f0d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f0d-132">CommonParameters</span></span>
<span data-ttu-id="c1f0d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f0d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f0d-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1f0d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f0d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1f0d-135">INPUTS</span></span>

### <span data-ttu-id="c1f0d-136">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c1f0d-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c1f0d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1f0d-137">OUTPUTS</span></span>

### <span data-ttu-id="c1f0d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1f0d-138">System.Boolean</span></span>

## <span data-ttu-id="c1f0d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1f0d-139">NOTES</span></span>

## <span data-ttu-id="c1f0d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1f0d-140">RELATED LINKS</span></span>
