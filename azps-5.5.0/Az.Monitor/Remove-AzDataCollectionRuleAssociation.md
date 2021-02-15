---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117514"
---
# <span data-ttu-id="14535-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="14535-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="14535-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14535-102">SYNOPSIS</span></span>
<span data-ttu-id="14535-103">Excluir uma associação de regras de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="14535-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="14535-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14535-104">SYNTAX</span></span>

### <span data-ttu-id="14535-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="14535-105">ByName (Default)</span></span>
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

### <span data-ttu-id="14535-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="14535-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="14535-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14535-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="14535-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="14535-108">DESCRIPTION</span></span>
<span data-ttu-id="14535-109">O cmdlet **Remove-AzDataCollectionRuleAssociation** exclui uma DCRA (associação de regras de coleta de dados).</span><span class="sxs-lookup"><span data-stu-id="14535-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="14535-110">Para aplicar um DCR a uma máquina virtual, crie uma associação para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="14535-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="14535-111">Uma máquina virtual pode ter uma associação a várias DCRs, e um DCR pode ter várias máquinas virtuais associadas a ela.</span><span class="sxs-lookup"><span data-stu-id="14535-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="14535-112">Isso permite que você defina um conjunto de DCRs, cada um correspondendo a um requisito específico, e aplicá-los somente às máquinas virtuais em que se aplicam.</span><span class="sxs-lookup"><span data-stu-id="14535-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="14535-113">Aqui está [o artigo "Configurar a coleta de dados para o agente do Monitor do Azure"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) usando o artigo DCRA.</span><span class="sxs-lookup"><span data-stu-id="14535-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="14535-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="14535-114">EXAMPLES</span></span>

### <span data-ttu-id="14535-115">Exemplo 1: Excluir a associação da regra de coleta de dados com parâmetros de nome e ID de recurso de destino (máquina virtual associada)</span><span class="sxs-lookup"><span data-stu-id="14535-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="14535-116">Exemplo 2: Excluir regra de coleta de dados com Objeto de Entrada</span><span class="sxs-lookup"><span data-stu-id="14535-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="14535-117">Exemplo 3: Excluir regra de coleta de dados com a propriedade ID do recurso de associação</span><span class="sxs-lookup"><span data-stu-id="14535-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="14535-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14535-118">PARAMETERS</span></span>

### <span data-ttu-id="14535-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14535-119">-DefaultProfile</span></span>
<span data-ttu-id="14535-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="14535-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14535-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="14535-121">-TargetResourceId</span></span>
<span data-ttu-id="14535-122">A ID de recurso associada.</span><span class="sxs-lookup"><span data-stu-id="14535-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="14535-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="14535-123">-AssociationName</span></span>
<span data-ttu-id="14535-124">O nome do recurso de associação.</span><span class="sxs-lookup"><span data-stu-id="14535-124">The name of the association resource.</span></span>

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

### <span data-ttu-id="14535-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14535-125">-InputObject</span></span>
<span data-ttu-id="14535-126">Objeto PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="14535-126">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="14535-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="14535-127">-AssociationId</span></span>
<span data-ttu-id="14535-128">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="14535-128">The resource identifier.</span></span>

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

### <span data-ttu-id="14535-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="14535-129">-Confirm</span></span>
<span data-ttu-id="14535-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14535-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14535-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14535-131">-WhatIf</span></span>
<span data-ttu-id="14535-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="14535-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14535-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14535-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14535-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14535-134">CommonParameters</span></span>
<span data-ttu-id="14535-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14535-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14535-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14535-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14535-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="14535-137">INPUTS</span></span>

### <span data-ttu-id="14535-138">System.String</span><span class="sxs-lookup"><span data-stu-id="14535-138">System.String</span></span>
###<span data-ttu-id="14535-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="14535-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="14535-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="14535-140">OUTPUTS</span></span>

### <span data-ttu-id="14535-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14535-141">System.Boolean</span></span>

## <span data-ttu-id="14535-142">Notas</span><span class="sxs-lookup"><span data-stu-id="14535-142">NOTES</span></span>

## <span data-ttu-id="14535-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14535-143">RELATED LINKS</span></span>

<span data-ttu-id="14535-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="14535-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
