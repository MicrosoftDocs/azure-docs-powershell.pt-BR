---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: f3904826ef41f271086d048183b8b2035d1b11e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598194"
---
# <span data-ttu-id="8e13e-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="8e13e-101">Get-AzActionRule</span></span>

## <span data-ttu-id="8e13e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e13e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e13e-103">Obter informações sobre regras de ação</span><span class="sxs-lookup"><span data-stu-id="8e13e-103">Get Action Rules Information</span></span>

## <span data-ttu-id="8e13e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e13e-104">SYNTAX</span></span>

### <span data-ttu-id="8e13e-105">ListActionRules (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e13e-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e13e-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="8e13e-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e13e-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="8e13e-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e13e-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8e13e-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e13e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e13e-109">DESCRIPTION</span></span>
<span data-ttu-id="8e13e-110">O cmdlet **Get-AzActionRule** recebe regras de ação configuradas.</span><span class="sxs-lookup"><span data-stu-id="8e13e-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="8e13e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e13e-111">EXAMPLES</span></span>

### <span data-ttu-id="8e13e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e13e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="8e13e-113">Listar todas as regras de ação configuradas no teste de grupo de recursos-RG filtrado em gravidade Sev2 e serviço de monitor de plataforma.</span><span class="sxs-lookup"><span data-stu-id="8e13e-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="8e13e-114">Use Format-List para obter os detalhes de cada regra de ação na lista.</span><span class="sxs-lookup"><span data-stu-id="8e13e-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="8e13e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8e13e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="8e13e-116">Obter a regra de ação com o nome Test-Action-Rule no grupo de recursos Test-RG.</span><span class="sxs-lookup"><span data-stu-id="8e13e-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="8e13e-117">OS</span><span class="sxs-lookup"><span data-stu-id="8e13e-117">PARAMETERS</span></span>

### <span data-ttu-id="8e13e-118">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="8e13e-118">-ActionGroup</span></span>
<span data-ttu-id="8e13e-119">Grupo de ação</span><span class="sxs-lookup"><span data-stu-id="8e13e-119">Action group</span></span>

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

### <span data-ttu-id="8e13e-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="8e13e-120">-AlertRuleId</span></span>
<span data-ttu-id="8e13e-121">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="8e13e-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="8e13e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e13e-122">-DefaultProfile</span></span>
<span data-ttu-id="8e13e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e13e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e13e-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="8e13e-124">-Description</span></span>
<span data-ttu-id="8e13e-125">Filtrar todos os alertas com a ID do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="8e13e-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="8e13e-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="8e13e-126">-ImpactedScope</span></span>
<span data-ttu-id="8e13e-127">Filtrar em escopo afetado</span><span class="sxs-lookup"><span data-stu-id="8e13e-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="8e13e-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="8e13e-128">-MonitorService</span></span>
<span data-ttu-id="8e13e-129">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="8e13e-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="8e13e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e13e-130">-Name</span></span>
<span data-ttu-id="8e13e-131">Nome da regra da ação.</span><span class="sxs-lookup"><span data-stu-id="8e13e-131">Name of action rule.</span></span>

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

### <span data-ttu-id="8e13e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e13e-132">-ResourceGroupName</span></span>
<span data-ttu-id="8e13e-133">Nome do grupo de recursos no qual a regra de ação reside.</span><span class="sxs-lookup"><span data-stu-id="8e13e-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="8e13e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e13e-134">-ResourceId</span></span>
<span data-ttu-id="8e13e-135">Obter regra de ação por ID nivelamento.</span><span class="sxs-lookup"><span data-stu-id="8e13e-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="8e13e-136">-Severidade</span><span class="sxs-lookup"><span data-stu-id="8e13e-136">-Severity</span></span>
<span data-ttu-id="8e13e-137">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="8e13e-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="8e13e-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e13e-138">-TargetResourceGroup</span></span>
<span data-ttu-id="8e13e-139">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="8e13e-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="8e13e-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8e13e-140">-TargetResourceId</span></span>
<span data-ttu-id="8e13e-141">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="8e13e-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="8e13e-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="8e13e-142">-TargetResourceType</span></span>
<span data-ttu-id="8e13e-143">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="8e13e-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="8e13e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e13e-144">CommonParameters</span></span>
<span data-ttu-id="8e13e-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e13e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e13e-146">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e13e-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e13e-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e13e-147">INPUTS</span></span>

### <span data-ttu-id="8e13e-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8e13e-148">None</span></span>

## <span data-ttu-id="8e13e-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e13e-149">OUTPUTS</span></span>

### <span data-ttu-id="8e13e-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="8e13e-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="8e13e-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e13e-151">NOTES</span></span>

## <span data-ttu-id="8e13e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e13e-152">RELATED LINKS</span></span>
