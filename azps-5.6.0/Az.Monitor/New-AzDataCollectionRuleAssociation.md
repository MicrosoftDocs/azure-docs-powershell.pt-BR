---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 1086f67bcec4adeef74fe7bf591e61d9d08a90e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889459"
---
# <span data-ttu-id="5a01b-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="5a01b-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="5a01b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a01b-102">SYNOPSIS</span></span>
<span data-ttu-id="5a01b-103">Criar associação de regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="5a01b-103">Create data collection rule association.</span></span>

## <span data-ttu-id="5a01b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5a01b-104">SYNTAX</span></span>

### <span data-ttu-id="5a01b-105">ByDataCollectionRuleId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5a01b-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="5a01b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a01b-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="5a01b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5a01b-107">DESCRIPTION</span></span>
<span data-ttu-id="5a01b-108">O cmdlet **New-AzDataCollectionRuleAssociation** cria uma associação de regras de coleta de dados (DCRA).</span><span class="sxs-lookup"><span data-stu-id="5a01b-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="5a01b-109">Para aplicar um DCR a uma máquina virtual, crie uma associação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5a01b-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="5a01b-110">Uma máquina virtual pode ter uma associação a vários DCRs, e um DCR pode ter várias máquinas virtuais associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="5a01b-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="5a01b-111">Isso permite que você defina um conjunto de DCRs, cada um correspondendo a um determinado requisito, e aplicá-los apenas às máquinas virtuais em que elas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="5a01b-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="5a01b-112">Aqui está o [artigo "Configurar coleta de dados para o agente do Monitor do Azure"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando o artigo DCRA.</span><span class="sxs-lookup"><span data-stu-id="5a01b-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="5a01b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a01b-113">EXAMPLES</span></span>

### <span data-ttu-id="5a01b-114">Exemplo 1: Criar associação de regras de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="5a01b-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="5a01b-115">Este comando cria uma associação de regra de coleta de dados para determinada ID de recurso de destino e regra.</span><span class="sxs-lookup"><span data-stu-id="5a01b-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="5a01b-116">Exemplo 2: Criar associação de regra de coleta de dados a partir de um objeto DCR</span><span class="sxs-lookup"><span data-stu-id="5a01b-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="5a01b-117">Este comando cria uma associação de regra de coleta de dados para determinada ID de recurso de destino e regra.</span><span class="sxs-lookup"><span data-stu-id="5a01b-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="5a01b-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5a01b-118">PARAMETERS</span></span>

### <span data-ttu-id="5a01b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a01b-119">-DefaultProfile</span></span>
<span data-ttu-id="5a01b-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5a01b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a01b-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="5a01b-121">-TargetResourceId</span></span>
<span data-ttu-id="5a01b-122">A ID do recurso a ser associada</span><span class="sxs-lookup"><span data-stu-id="5a01b-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="5a01b-123">-AssociationName</span></span>
<span data-ttu-id="5a01b-124">O nome do recurso</span><span class="sxs-lookup"><span data-stu-id="5a01b-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="5a01b-125">-RuleId</span></span>
<span data-ttu-id="5a01b-126">A ID da regra de coleta de dados</span><span class="sxs-lookup"><span data-stu-id="5a01b-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a01b-127">-InputObject</span></span>
<span data-ttu-id="5a01b-128">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="5a01b-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-129">-Description</span><span class="sxs-lookup"><span data-stu-id="5a01b-129">-Description</span></span>
<span data-ttu-id="5a01b-130">A descrição do recurso</span><span class="sxs-lookup"><span data-stu-id="5a01b-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a01b-131">-Confirm</span></span>
<span data-ttu-id="5a01b-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a01b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a01b-133">-WhatIf</span></span>
<span data-ttu-id="5a01b-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5a01b-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a01b-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5a01b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a01b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a01b-136">CommonParameters</span></span>
<span data-ttu-id="5a01b-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a01b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a01b-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a01b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a01b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a01b-139">INPUTS</span></span>

### <span data-ttu-id="5a01b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5a01b-140">System.String</span></span>

## <span data-ttu-id="5a01b-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5a01b-141">OUTPUTS</span></span>

### <span data-ttu-id="5a01b-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="5a01b-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="5a01b-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="5a01b-143">NOTES</span></span>

## <span data-ttu-id="5a01b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a01b-144">RELATED LINKS</span></span>

<span data-ttu-id="5a01b-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
 [Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="5a01b-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
