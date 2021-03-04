---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 24ad63f1422a829a0cef3ed0c4907ea5687b6151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890615"
---
# <span data-ttu-id="01741-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="01741-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="01741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01741-102">SYNOPSIS</span></span>
<span data-ttu-id="01741-103">Remove uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="01741-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="01741-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="01741-104">SYNTAX</span></span>

### <span data-ttu-id="01741-105">ByRuleName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="01741-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01741-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="01741-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01741-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01741-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01741-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="01741-108">DESCRIPTION</span></span>
<span data-ttu-id="01741-109">Remove uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="01741-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="01741-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01741-110">EXAMPLES</span></span>

### <span data-ttu-id="01741-111">Exemplo 1: Remover pelo nome da regra</span><span class="sxs-lookup"><span data-stu-id="01741-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="01741-112">Exemplo 2: Remover por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="01741-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="01741-113">Exemplo 3: Remover por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="01741-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="01741-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="01741-114">PARAMETERS</span></span>

### <span data-ttu-id="01741-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01741-115">-DefaultProfile</span></span>
<span data-ttu-id="01741-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01741-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01741-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01741-117">-InputObject</span></span>
<span data-ttu-id="01741-118">O recurso Regra de Consulta Agendada</span><span class="sxs-lookup"><span data-stu-id="01741-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01741-119">-Name</span><span class="sxs-lookup"><span data-stu-id="01741-119">-Name</span></span>
<span data-ttu-id="01741-120">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="01741-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01741-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01741-121">-PassThru</span></span>
<span data-ttu-id="01741-122">Retornar um valor que indica sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="01741-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="01741-123">Este cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="01741-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01741-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01741-124">-ResourceGroupName</span></span>
<span data-ttu-id="01741-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="01741-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01741-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01741-126">-ResourceId</span></span>
<span data-ttu-id="01741-127">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="01741-127">The resource Id</span></span>

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

### <span data-ttu-id="01741-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01741-128">-Confirm</span></span>
<span data-ttu-id="01741-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01741-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01741-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01741-130">-WhatIf</span></span>
<span data-ttu-id="01741-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01741-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01741-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01741-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01741-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01741-133">CommonParameters</span></span>
<span data-ttu-id="01741-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01741-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01741-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01741-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01741-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01741-136">INPUTS</span></span>

### <span data-ttu-id="01741-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="01741-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="01741-138">System.String</span><span class="sxs-lookup"><span data-stu-id="01741-138">System.String</span></span>

## <span data-ttu-id="01741-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="01741-139">OUTPUTS</span></span>

### <span data-ttu-id="01741-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01741-140">System.Boolean</span></span>

## <span data-ttu-id="01741-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="01741-141">NOTES</span></span>

## <span data-ttu-id="01741-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01741-142">RELATED LINKS</span></span>
