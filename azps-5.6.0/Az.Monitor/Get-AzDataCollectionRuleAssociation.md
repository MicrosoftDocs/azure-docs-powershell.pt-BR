---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1a63d28664eb8ade22c87cfad3a21db0764cbceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888895"
---
# <span data-ttu-id="34fde-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="34fde-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="34fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34fde-102">SYNOPSIS</span></span>
<span data-ttu-id="34fde-103">Obtém associações de regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="34fde-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="34fde-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="34fde-104">SYNTAX</span></span>

### <span data-ttu-id="34fde-105">ByAssociatedResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="34fde-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="34fde-106">ByName</span><span class="sxs-lookup"><span data-stu-id="34fde-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="34fde-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="34fde-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="34fde-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="34fde-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="34fde-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="34fde-109">DESCRIPTION</span></span>
<span data-ttu-id="34fde-110">O cmdlet **Get-AzDataCollectionRuleAssociation** obtém uma ou mais associações de regras de coleta de dados (DCRA).</span><span class="sxs-lookup"><span data-stu-id="34fde-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="34fde-111">Para aplicar um DCR a uma máquina virtual, crie uma associação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34fde-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="34fde-112">Uma máquina virtual pode ter uma associação a vários DCRs, e um DCR pode ter várias máquinas virtuais associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="34fde-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="34fde-113">Isso permite que você defina um conjunto de DCRs, cada um correspondendo a um determinado requisito, e aplicá-los apenas às máquinas virtuais em que elas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="34fde-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="34fde-114">Aqui está o [artigo "Configurar coleta de dados para o agente do Monitor do Azure"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando o artigo DCRA.</span><span class="sxs-lookup"><span data-stu-id="34fde-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="34fde-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34fde-115">EXAMPLES</span></span>

### <span data-ttu-id="34fde-116">Exemplo 1: Obter associações de regras de coleta de dados por ID de recurso de destino (máquina virtual associada)</span><span class="sxs-lookup"><span data-stu-id="34fde-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="34fde-117">Este comando lista todas as regras de coleta de dados para a ID de recurso de destino (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="34fde-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="34fde-118">Exemplo 2: Obter associações de regras de coleta de dados por regra (DCR)</span><span class="sxs-lookup"><span data-stu-id="34fde-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="34fde-119">Este comando lista associações de regras de coleta de dados para o determinado grupo de recursos e regra (DCR).</span><span class="sxs-lookup"><span data-stu-id="34fde-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="34fde-120">Exemplo 3: Obter associações de regras de coleta de dados por objeto de entrada (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="34fde-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="34fde-121">Este comando lista associações de regras de coleta de dados para o objeto de entrada determinado.</span><span class="sxs-lookup"><span data-stu-id="34fde-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="34fde-122">Exemplo 4: obter uma associação de regra de coleta de dados por ID de recurso de destino (máquina virtual associada) e nome da associação</span><span class="sxs-lookup"><span data-stu-id="34fde-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="34fde-123">Este comando lista uma associação de regra de coleta de dados (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="34fde-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="34fde-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="34fde-124">PARAMETERS</span></span>

### <span data-ttu-id="34fde-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34fde-125">-DefaultProfile</span></span>
<span data-ttu-id="34fde-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="34fde-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34fde-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="34fde-127">-TargetResourceId</span></span>
<span data-ttu-id="34fde-128">A ID de recurso associada</span><span class="sxs-lookup"><span data-stu-id="34fde-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34fde-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34fde-129">-ResourceGroupName</span></span>
<span data-ttu-id="34fde-130">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="34fde-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34fde-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="34fde-131">-RuleName</span></span>
<span data-ttu-id="34fde-132">O nome da regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="34fde-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34fde-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34fde-133">-InputObject</span></span>
<span data-ttu-id="34fde-134">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="34fde-134">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="34fde-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="34fde-135">-AssociationName</span></span>
<span data-ttu-id="34fde-136">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="34fde-136">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34fde-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fde-137">CommonParameters</span></span>
<span data-ttu-id="34fde-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34fde-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fde-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34fde-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fde-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34fde-140">INPUTS</span></span>

### <span data-ttu-id="34fde-141">System.String</span><span class="sxs-lookup"><span data-stu-id="34fde-141">System.String</span></span>
### <span data-ttu-id="34fde-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="34fde-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="34fde-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="34fde-143">OUTPUTS</span></span>

### <span data-ttu-id="34fde-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="34fde-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="34fde-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="34fde-145">NOTES</span></span>

## <span data-ttu-id="34fde-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34fde-146">RELATED LINKS</span></span>

<span data-ttu-id="34fde-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="34fde-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
