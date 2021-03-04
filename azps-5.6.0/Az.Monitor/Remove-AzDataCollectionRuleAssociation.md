---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889924"
---
# <span data-ttu-id="6f3a1-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="6f3a1-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="6f3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="6f3a1-103">Excluir uma associação de regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="6f3a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6f3a1-104">SYNTAX</span></span>

### <span data-ttu-id="6f3a1-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6f3a1-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="6f3a1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f3a1-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="6f3a1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3a1-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="6f3a1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6f3a1-108">DESCRIPTION</span></span>
<span data-ttu-id="6f3a1-109">O cmdlet **Remove-AzDataCollectionRuleAssociation** exclui uma associação de regras de coleta de dados (DCRA).</span><span class="sxs-lookup"><span data-stu-id="6f3a1-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="6f3a1-110">Para aplicar um DCR a uma máquina virtual, crie uma associação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="6f3a1-111">Uma máquina virtual pode ter uma associação a vários DCRs, e um DCR pode ter várias máquinas virtuais associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="6f3a1-112">Isso permite que você defina um conjunto de DCRs, cada um correspondendo a um determinado requisito, e aplicá-los apenas às máquinas virtuais em que elas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="6f3a1-113">Aqui está o [artigo "Configurar coleta de dados para o agente do Monitor do Azure"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando o artigo DCRA.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="6f3a1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-114">EXAMPLES</span></span>

### <span data-ttu-id="6f3a1-115">Exemplo 1: Excluir associação de regra de coleta de dados com parâmetros de ID de recurso de destino e nome (máquina virtual associada)</span><span class="sxs-lookup"><span data-stu-id="6f3a1-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="6f3a1-116">Exemplo 2: Excluir regra de coleta de dados com o objeto Input</span><span class="sxs-lookup"><span data-stu-id="6f3a1-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="6f3a1-117">Exemplo 3: Excluir regra de coleta de dados com a propriedade de ID de recurso de associação</span><span class="sxs-lookup"><span data-stu-id="6f3a1-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="6f3a1-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-118">PARAMETERS</span></span>

### <span data-ttu-id="6f3a1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f3a1-119">-DefaultProfile</span></span>
<span data-ttu-id="6f3a1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6f3a1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f3a1-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6f3a1-121">-TargetResourceId</span></span>
<span data-ttu-id="6f3a1-122">A ID de recurso associada.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="6f3a1-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="6f3a1-123">-AssociationName</span></span>
<span data-ttu-id="6f3a1-124">O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3a1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f3a1-125">-InputObject</span></span>
<span data-ttu-id="6f3a1-126">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="6f3a1-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="6f3a1-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="6f3a1-127">-AssociationId</span></span>
<span data-ttu-id="6f3a1-128">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-128">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f3a1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f3a1-129">-Confirm</span></span>
<span data-ttu-id="6f3a1-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f3a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f3a1-131">-WhatIf</span></span>
<span data-ttu-id="6f3a1-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f3a1-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f3a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f3a1-134">CommonParameters</span></span>
<span data-ttu-id="6f3a1-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f3a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f3a1-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f3a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f3a1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-137">INPUTS</span></span>

### <span data-ttu-id="6f3a1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6f3a1-138">System.String</span></span>
###<span data-ttu-id="6f3a1-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="6f3a1-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="6f3a1-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-140">OUTPUTS</span></span>

### <span data-ttu-id="6f3a1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6f3a1-141">System.Boolean</span></span>

## <span data-ttu-id="6f3a1-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="6f3a1-142">NOTES</span></span>

## <span data-ttu-id="6f3a1-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f3a1-143">RELATED LINKS</span></span>

<span data-ttu-id="6f3a1-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="6f3a1-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
