---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433526"
---
# <span data-ttu-id="fc08a-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="fc08a-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="fc08a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc08a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc08a-103">Remove uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="fc08a-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="fc08a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc08a-104">SYNTAX</span></span>

### <span data-ttu-id="fc08a-105">ByRuleName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc08a-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc08a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc08a-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc08a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fc08a-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc08a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc08a-108">DESCRIPTION</span></span>
<span data-ttu-id="fc08a-109">Remove uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="fc08a-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="fc08a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc08a-110">EXAMPLES</span></span>

### <span data-ttu-id="fc08a-111">Exemplo 1: remover por nome da regra</span><span class="sxs-lookup"><span data-stu-id="fc08a-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="fc08a-112">Exemplo 2: remover por objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="fc08a-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="fc08a-113">Exemplo 3: remover por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="fc08a-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="fc08a-114">OS</span><span class="sxs-lookup"><span data-stu-id="fc08a-114">PARAMETERS</span></span>

### <span data-ttu-id="fc08a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc08a-115">-DefaultProfile</span></span>
<span data-ttu-id="fc08a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc08a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc08a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc08a-117">-InputObject</span></span>
<span data-ttu-id="fc08a-118">O recurso de regra de consulta agendada</span><span class="sxs-lookup"><span data-stu-id="fc08a-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="fc08a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc08a-119">-Name</span></span>
<span data-ttu-id="fc08a-120">O nome do alerta</span><span class="sxs-lookup"><span data-stu-id="fc08a-120">The alert name</span></span>

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

### <span data-ttu-id="fc08a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc08a-121">-PassThru</span></span>
<span data-ttu-id="fc08a-122">Retorna um valor que indica sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="fc08a-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="fc08a-123">Esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="fc08a-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc08a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc08a-124">-ResourceGroupName</span></span>
<span data-ttu-id="fc08a-125">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fc08a-125">The resource group name</span></span>

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

### <span data-ttu-id="fc08a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc08a-126">-ResourceId</span></span>
<span data-ttu-id="fc08a-127">A ID do recurso</span><span class="sxs-lookup"><span data-stu-id="fc08a-127">The resource Id</span></span>

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

### <span data-ttu-id="fc08a-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc08a-128">-Confirm</span></span>
<span data-ttu-id="fc08a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc08a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc08a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc08a-130">-WhatIf</span></span>
<span data-ttu-id="fc08a-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc08a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc08a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc08a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc08a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc08a-133">CommonParameters</span></span>
<span data-ttu-id="fc08a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc08a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc08a-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc08a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc08a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc08a-136">INPUTS</span></span>

### <span data-ttu-id="fc08a-137">Microsoft. Azure. Commands. insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="fc08a-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="fc08a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fc08a-138">System.String</span></span>

## <span data-ttu-id="fc08a-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc08a-139">OUTPUTS</span></span>

### <span data-ttu-id="fc08a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc08a-140">System.Boolean</span></span>

## <span data-ttu-id="fc08a-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc08a-141">NOTES</span></span>

## <span data-ttu-id="fc08a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc08a-142">RELATED LINKS</span></span>
