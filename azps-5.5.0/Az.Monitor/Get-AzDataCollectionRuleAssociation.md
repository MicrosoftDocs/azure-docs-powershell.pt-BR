---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111764"
---
# <span data-ttu-id="0658c-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="0658c-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="0658c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0658c-102">SYNOPSIS</span></span>
<span data-ttu-id="0658c-103">Obtém associação de regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="0658c-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="0658c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0658c-104">SYNTAX</span></span>

### <span data-ttu-id="0658c-105">ByAssociatedResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0658c-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="0658c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0658c-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="0658c-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="0658c-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="0658c-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0658c-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="0658c-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0658c-109">DESCRIPTION</span></span>
<span data-ttu-id="0658c-110">O cmdlet **Get-AzDataCollectionRuleAssociation** obtém uma ou mais associações de regras de coleta de dados (DCRA).</span><span class="sxs-lookup"><span data-stu-id="0658c-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="0658c-111">Para aplicar um DCR a uma máquina virtual, crie uma associação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0658c-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="0658c-112">Uma máquina virtual pode ter uma associação a várias DCRs, e um DCR pode ter várias máquinas virtuais associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="0658c-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="0658c-113">Isso permite que você defina um conjunto de DCRs, cada um correspondendo a um requisito específico, e aplicá-los somente às máquinas virtuais em que se aplicam.</span><span class="sxs-lookup"><span data-stu-id="0658c-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="0658c-114">Aqui está [o artigo "Configurar a coleta de dados para o agente do Monitor do Azure"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando o artigo DCRA.</span><span class="sxs-lookup"><span data-stu-id="0658c-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="0658c-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0658c-115">EXAMPLES</span></span>

### <span data-ttu-id="0658c-116">Exemplo 1: Obter associações de regras de coleta de dados por ID de recurso de destino (máquina virtual associada)</span><span class="sxs-lookup"><span data-stu-id="0658c-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
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

<span data-ttu-id="0658c-117">Esse comando lista todas as regras de coleta de dados para a ID de recurso de destino determinada (máquina virtual).</span><span class="sxs-lookup"><span data-stu-id="0658c-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="0658c-118">Exemplo 2: Obter associações de regras de coleta de dados por regra (DCR)</span><span class="sxs-lookup"><span data-stu-id="0658c-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
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

<span data-ttu-id="0658c-119">Esse comando lista as associações de regras de coleta de dados para determinado grupo de recursos e regra (DCR).</span><span class="sxs-lookup"><span data-stu-id="0658c-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="0658c-120">Exemplo 3: Obter associações de regras de coleta de dados por objeto de entrada (PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="0658c-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
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

<span data-ttu-id="0658c-121">Este comando lista as associações de regras de coleta de dados para o objeto de entrada determinado.</span><span class="sxs-lookup"><span data-stu-id="0658c-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="0658c-122">Exemplo 4: Obter uma associação de regra de coleta de dados por ID de recurso de destino (máquina virtual associada) e nome da associação</span><span class="sxs-lookup"><span data-stu-id="0658c-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
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

<span data-ttu-id="0658c-123">Esse comando lista uma associação de regras de coleta de dados (uma lista com um único elemento).</span><span class="sxs-lookup"><span data-stu-id="0658c-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="0658c-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0658c-124">PARAMETERS</span></span>

### <span data-ttu-id="0658c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0658c-125">-DefaultProfile</span></span>
<span data-ttu-id="0658c-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0658c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0658c-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="0658c-127">-TargetResourceId</span></span>
<span data-ttu-id="0658c-128">A ID de recurso associada</span><span class="sxs-lookup"><span data-stu-id="0658c-128">The associated resource ID</span></span>

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

### <span data-ttu-id="0658c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0658c-129">-ResourceGroupName</span></span>
<span data-ttu-id="0658c-130">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0658c-130">The resource group name</span></span>

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

### <span data-ttu-id="0658c-131">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="0658c-131">-RuleName</span></span>
<span data-ttu-id="0658c-132">O nome da regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="0658c-132">The data collection rule name</span></span>

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

### <span data-ttu-id="0658c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0658c-133">-InputObject</span></span>
<span data-ttu-id="0658c-134">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="0658c-134">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="0658c-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="0658c-135">-AssociationName</span></span>
<span data-ttu-id="0658c-136">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="0658c-136">The name of the association.</span></span>

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

### <span data-ttu-id="0658c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0658c-137">CommonParameters</span></span>
<span data-ttu-id="0658c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0658c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0658c-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0658c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0658c-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="0658c-140">INPUTS</span></span>

### <span data-ttu-id="0658c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0658c-141">System.String</span></span>
### <span data-ttu-id="0658c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="0658c-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="0658c-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="0658c-143">OUTPUTS</span></span>

### <span data-ttu-id="0658c-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="0658c-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="0658c-145">Notas</span><span class="sxs-lookup"><span data-stu-id="0658c-145">NOTES</span></span>

## <span data-ttu-id="0658c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0658c-146">RELATED LINKS</span></span>

<span data-ttu-id="0658c-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="0658c-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
