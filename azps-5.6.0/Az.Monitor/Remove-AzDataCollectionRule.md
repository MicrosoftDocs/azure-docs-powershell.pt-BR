---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888236"
---
# <span data-ttu-id="e7a22-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="e7a22-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="e7a22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7a22-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a22-103">Excluir uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="e7a22-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="e7a22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e7a22-104">SYNTAX</span></span>

### <span data-ttu-id="e7a22-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e7a22-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="e7a22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e7a22-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="e7a22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a22-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="e7a22-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e7a22-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a22-109">O cmdlet **Remove-AzDataCollectionRule** exclui uma regra de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="e7a22-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="e7a22-110">As Regras de Coleta de Dados (DCR) definem os dados que vêm para o Monitor do Azure e especificam para onde esses dados devem ser enviados ou armazenados.</span><span class="sxs-lookup"><span data-stu-id="e7a22-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="e7a22-111">Aqui está o artigo completo [de visão geral do DCR](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span><span class="sxs-lookup"><span data-stu-id="e7a22-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="e7a22-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7a22-112">EXAMPLES</span></span>

### <span data-ttu-id="e7a22-113">Exemplo 1: Excluir regra de coleta de dados com parâmetros de nome e grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e7a22-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="e7a22-114">Exemplo 2: Excluir regra de coleta de dados com nome e grupo de recursos retorna bool</span><span class="sxs-lookup"><span data-stu-id="e7a22-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="e7a22-115">Exemplo 3: Excluir regra de coleta de dados de InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a22-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="e7a22-116">Exemplo 4: Excluir regra de coleta de dados da id de recurso</span><span class="sxs-lookup"><span data-stu-id="e7a22-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="e7a22-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e7a22-117">PARAMETERS</span></span>

### <span data-ttu-id="e7a22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a22-118">-DefaultProfile</span></span>
<span data-ttu-id="e7a22-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e7a22-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7a22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a22-120">-ResourceGroupName</span></span>
<span data-ttu-id="e7a22-121">O nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e7a22-121">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a22-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="e7a22-122">-RuleName</span></span>
<span data-ttu-id="e7a22-123">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="e7a22-123">The resource name.</span></span>

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

### <span data-ttu-id="e7a22-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="e7a22-124">-RuleId</span></span>
<span data-ttu-id="e7a22-125">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="e7a22-125">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a22-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7a22-126">-Confirm</span></span>
<span data-ttu-id="e7a22-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a22-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a22-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a22-128">-WhatIf</span></span>
<span data-ttu-id="e7a22-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7a22-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7a22-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7a22-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a22-131">CommonParameters</span></span>
<span data-ttu-id="e7a22-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a22-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7a22-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a22-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7a22-134">INPUTS</span></span>

### <span data-ttu-id="e7a22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e7a22-135">System.String</span></span>

## <span data-ttu-id="e7a22-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e7a22-136">OUTPUTS</span></span>

### <span data-ttu-id="e7a22-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="e7a22-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="e7a22-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="e7a22-138">NOTES</span></span>

## <span data-ttu-id="e7a22-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7a22-139">RELATED LINKS</span></span>

<span data-ttu-id="e7a22-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="e7a22-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>