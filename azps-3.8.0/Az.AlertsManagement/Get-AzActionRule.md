---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzActionRule.md
ms.openlocfilehash: e1eb623fcb4b77dda95fe3f849c86e20ad5d1601
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941208"
---
# <span data-ttu-id="d3f52-101">Get-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d3f52-101">Get-AzActionRule</span></span>

## <span data-ttu-id="d3f52-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3f52-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f52-103">Obter informações sobre regras de ação</span><span class="sxs-lookup"><span data-stu-id="d3f52-103">Get Action Rules Information</span></span>

## <span data-ttu-id="d3f52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3f52-104">SYNTAX</span></span>

### <span data-ttu-id="d3f52-105">ListActionRules (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3f52-105">ListActionRules (Default)</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceType <String>]
 [-TargetResourceGroup <String>] [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>]
 [-AlertRuleId <String>] [-Description <String>] [-ActionGroup <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f52-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d3f52-106">ResourceId</span></span>
```
Get-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f52-107">ActionRuleByName</span><span class="sxs-lookup"><span data-stu-id="d3f52-107">ActionRuleByName</span></span>
```
Get-AzActionRule -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3f52-108">ListActionRulesByTargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f52-108">ListActionRulesByTargetResourceId</span></span>
```
Get-AzActionRule [-Name <String>] [-ResourceGroupName <String>] [-TargetResourceId <String>]
 [-MonitorService <String>] [-Severity <String>] [-ImpactedScope <String>] [-AlertRuleId <String>]
 [-Description <String>] [-ActionGroup <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3f52-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3f52-109">DESCRIPTION</span></span>
<span data-ttu-id="d3f52-110">O cmdlet **Get-AzActionRule** recebe regras de ação configuradas.</span><span class="sxs-lookup"><span data-stu-id="d3f52-110">**Get-AzActionRule** cmdlet gets action rules configured.</span></span>

## <span data-ttu-id="d3f52-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3f52-111">EXAMPLES</span></span>

### <span data-ttu-id="d3f52-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d3f52-112">Example 1</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Severity "Sev2" -MonitorService "Platform"
```

<span data-ttu-id="d3f52-113">Listar todas as regras de ação configuradas no teste de grupo de recursos-RG filtrado em gravidade Sev2 e serviço de monitor de plataforma.</span><span class="sxs-lookup"><span data-stu-id="d3f52-113">List all action rules configured in resource group test-rg filtered on Sev2 severity and Platform Monitor Service.</span></span> <span data-ttu-id="d3f52-114">Use Format-List para obter os detalhes de cada regra de ação na lista.</span><span class="sxs-lookup"><span data-stu-id="d3f52-114">Use Format-List to get the details of each action rule in list.</span></span>

### <span data-ttu-id="d3f52-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d3f52-115">Example 2</span></span>
```powershell
PS C:\> Get-AzActionRule -ResourceGroupName "test-rg" -Name "Test-Action-Rule" | Format-List
```

<span data-ttu-id="d3f52-116">Obter a regra de ação com o nome Test-Action-Rule no grupo de recursos Test-RG.</span><span class="sxs-lookup"><span data-stu-id="d3f52-116">Get the action rule with name Test-Action-Rule in test-rg resource group.</span></span>

## <span data-ttu-id="d3f52-117">OS</span><span class="sxs-lookup"><span data-stu-id="d3f52-117">PARAMETERS</span></span>

### <span data-ttu-id="d3f52-118">-Botão de ação</span><span class="sxs-lookup"><span data-stu-id="d3f52-118">-ActionGroup</span></span>
<span data-ttu-id="d3f52-119">Grupo de ação</span><span class="sxs-lookup"><span data-stu-id="d3f52-119">Action group</span></span>

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

### <span data-ttu-id="d3f52-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d3f52-120">-AlertRuleId</span></span>
<span data-ttu-id="d3f52-121">Filtrar por ID de regra de alerta</span><span class="sxs-lookup"><span data-stu-id="d3f52-121">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="d3f52-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f52-122">-DefaultProfile</span></span>
<span data-ttu-id="d3f52-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f52-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f52-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d3f52-124">-Description</span></span>
<span data-ttu-id="d3f52-125">Filtrar todos os alertas com a ID do grupo inteligente</span><span class="sxs-lookup"><span data-stu-id="d3f52-125">Filter all the alerts having the Smart Group Id</span></span>

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

### <span data-ttu-id="d3f52-126">-ImpactedScope</span><span class="sxs-lookup"><span data-stu-id="d3f52-126">-ImpactedScope</span></span>
<span data-ttu-id="d3f52-127">Filtrar em escopo afetado</span><span class="sxs-lookup"><span data-stu-id="d3f52-127">Filter on Impacted scope</span></span>

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

### <span data-ttu-id="d3f52-128">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="d3f52-128">-MonitorService</span></span>
<span data-ttu-id="d3f52-129">Filtrar no serviço moniter</span><span class="sxs-lookup"><span data-stu-id="d3f52-129">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="d3f52-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3f52-130">-Name</span></span>
<span data-ttu-id="d3f52-131">Nome da regra da ação.</span><span class="sxs-lookup"><span data-stu-id="d3f52-131">Name of action rule.</span></span>

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

### <span data-ttu-id="d3f52-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f52-132">-ResourceGroupName</span></span>
<span data-ttu-id="d3f52-133">Nome do grupo de recursos no qual a regra de ação reside.</span><span class="sxs-lookup"><span data-stu-id="d3f52-133">Resource Group Name in which action rule resides.</span></span>

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

### <span data-ttu-id="d3f52-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f52-134">-ResourceId</span></span>
<span data-ttu-id="d3f52-135">Obter regra de ação por ID nivelamento.</span><span class="sxs-lookup"><span data-stu-id="d3f52-135">Get Action rule by resoure id.</span></span>

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

### <span data-ttu-id="d3f52-136">-Severidade</span><span class="sxs-lookup"><span data-stu-id="d3f52-136">-Severity</span></span>
<span data-ttu-id="d3f52-137">Filtrar a gravidade do alerta</span><span class="sxs-lookup"><span data-stu-id="d3f52-137">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="d3f52-138">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d3f52-138">-TargetResourceGroup</span></span>
<span data-ttu-id="d3f52-139">Filtrar no grupo de recursos nome do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="d3f52-139">Filter on Resource group name of the target resource of alert.</span></span>

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

### <span data-ttu-id="d3f52-140">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d3f52-140">-TargetResourceId</span></span>
<span data-ttu-id="d3f52-141">Filtre a ID do recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="d3f52-141">Filter on Resource Id of the target resource of alert.</span></span>

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

### <span data-ttu-id="d3f52-142">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="d3f52-142">-TargetResourceType</span></span>
<span data-ttu-id="d3f52-143">Filtrar tipo de recurso do recurso de destino do alerta.</span><span class="sxs-lookup"><span data-stu-id="d3f52-143">Filter on Resource type of the target resource of alert.</span></span>

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

### <span data-ttu-id="d3f52-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f52-144">CommonParameters</span></span>
<span data-ttu-id="d3f52-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f52-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f52-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3f52-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f52-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3f52-147">INPUTS</span></span>

### <span data-ttu-id="d3f52-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d3f52-148">None</span></span>

## <span data-ttu-id="d3f52-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3f52-149">OUTPUTS</span></span>

### <span data-ttu-id="d3f52-150">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d3f52-150">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d3f52-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3f52-151">NOTES</span></span>

## <span data-ttu-id="d3f52-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3f52-152">RELATED LINKS</span></span>
