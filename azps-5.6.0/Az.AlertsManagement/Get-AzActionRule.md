---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: c90c4ba559bfe6e453a984546217692181f40597
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886516"
---
# <span data-ttu-id="b61c9-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="b61c9-101">Get-AzActionRule</span></span>

## <span data-ttu-id="b61c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b61c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b61c9-103">Obter informações sobre regras de ação</span><span class="sxs-lookup"><span data-stu-id="b61c9-103">Get Action Rules Information</span></span>

## <span data-ttu-id="b61c9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b61c9-104">SYNTAX</span></span>

### <span data-ttu-id="b61c9-105">ListActionRules (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b61c9-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b61c9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b61c9-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b61c9-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="b61c9-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b61c9-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b61c9-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b61c9-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b61c9-109">DESCRIPTION</span></span>
<span data-ttu-id="b61c9-110">O cmdlet **Get-AzActionRule** obtém regras de ação configuradas.</span><span class="sxs-lookup"><span data-stu-id="b61c9-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="b61c9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b61c9-111">EXAMPLES</span></span>

### <span data-ttu-id="b61c9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b61c9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="b61c9-113">Listar todas as regras de ação configuradas no grupo de recursos test-rg filtrada em Sev2 severity e Platform Monitor Service.</span><span class="sxs-lookup"><span data-stu-id="b61c9-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="b61c9-114">Use Format-List para obter os detalhes de cada regra de ação na lista.</span><span class="sxs-lookup"><span data-stu-id="b61c9-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="b61c9-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b61c9-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="b61c9-116">Obter a regra de ação com o nome Test-Action-Rule no grupo de recursos test-rg.</span><span class="sxs-lookup"><span data-stu-id="b61c9-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="b61c9-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b61c9-117">PARAMETERS</span></span>

### <span data-ttu-id="b61c9-118">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="b61c9-118">-ActionGroup</span></span>
<span data-ttu-id="b61c9-119">Grupo de ações</span><span class="sxs-lookup"><span data-stu-id="b61c9-119">Action group</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="b61c9-120">-AlertRuleId</span></span>
<span data-ttu-id="b61c9-121">Filtrar na ID da Regra de Alerta</span><span class="sxs-lookup"><span data-stu-id="b61c9-121">Filter on Alert Rule Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61c9-122">-DefaultProfile</span></span>
<span data-ttu-id="b61c9-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b61c9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61c9-124">-Description</span><span class="sxs-lookup"><span data-stu-id="b61c9-124">-Description</span></span>
<span data-ttu-id="b61c9-125">Filtrar todos os alertas com a ID do Grupo Inteligente</span><span class="sxs-lookup"><span data-stu-id="b61c9-125">Filter all the alerts having the Smart Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="b61c9-126">-ImpactedScope</span></span>
<span data-ttu-id="b61c9-127">Filtrar no escopo afetado</span><span class="sxs-lookup"><span data-stu-id="b61c9-127">Filter on Impacted scope</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="b61c9-128">-MonitorService</span></span>
<span data-ttu-id="b61c9-129">Filtrar no serviço Moniter</span><span class="sxs-lookup"><span data-stu-id="b61c9-129">Filter on Moniter Service</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="b61c9-130">-Name</span></span>
<span data-ttu-id="b61c9-131">Nome da regra de ação.</span><span class="sxs-lookup"><span data-stu-id="b61c9-131">Name of action rule.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61c9-132">-ResourceGroupName</span></span>
<span data-ttu-id="b61c9-133">Nome do Grupo de Recursos no qual a regra de ação reside.</span><span class="sxs-lookup"><span data-stu-id="b61c9-133">Resource Group Name in which action rule resides.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ActionRuleByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b61c9-134">-ResourceId</span></span>
<span data-ttu-id="b61c9-135">Get Action rule by resource id.</span><span class="sxs-lookup"><span data-stu-id="b61c9-135">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-136">-Severity</span><span class="sxs-lookup"><span data-stu-id="b61c9-136">-Severity</span></span>
<span data-ttu-id="b61c9-137">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="b61c9-137">Filter on Severity of alert</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules, ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b61c9-138">-TargetResourceGroup</span></span>
<span data-ttu-id="b61c9-139">Filtrar o nome do grupo de recursos do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="b61c9-139">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b61c9-140">-TargetResourceId</span></span>
<span data-ttu-id="b61c9-141">Filtrar na ID de Recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="b61c9-141">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRulesByTargetResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="b61c9-142">-TargetResourceType</span></span>
<span data-ttu-id="b61c9-143">Filtrar o tipo de recurso do recurso de destino de alerta.</span><span class="sxs-lookup"><span data-stu-id="b61c9-143">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ListActionRules
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61c9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61c9-144">CommonParameters</span></span>
<span data-ttu-id="b61c9-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61c9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61c9-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b61c9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61c9-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b61c9-147">INPUTS</span></span>

### <span data-ttu-id="b61c9-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b61c9-148">None</span></span>

## <span data-ttu-id="b61c9-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b61c9-149">OUTPUTS</span></span>

### <span data-ttu-id="b61c9-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="b61c9-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="b61c9-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="b61c9-151">NOTES</span></span>

## <span data-ttu-id="b61c9-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b61c9-152">RELATED LINKS</span></span>
