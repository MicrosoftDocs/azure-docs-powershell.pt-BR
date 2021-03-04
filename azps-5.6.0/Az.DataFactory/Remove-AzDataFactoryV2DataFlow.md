---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 66f5cf02c4f50c699f790ec2790080fa37ab166d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892800"
---
# <span data-ttu-id="7c3de-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="7c3de-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="7c3de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c3de-102">SYNOPSIS</span></span>
<span data-ttu-id="7c3de-103">Remove um fluxo de dados do Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7c3de-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="7c3de-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c3de-104">SYNTAX</span></span>

### <span data-ttu-id="7c3de-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c3de-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c3de-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c3de-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c3de-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c3de-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c3de-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c3de-108">DESCRIPTION</span></span>
<span data-ttu-id="7c3de-109">O Remove-AzDataFactoryV2DataFlow cmdlet remove um fluxo de dados do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7c3de-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="7c3de-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c3de-110">EXAMPLES</span></span>

### <span data-ttu-id="7c3de-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c3de-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="7c3de-112">Este comando remove o fluxo de dados denominado dataflow5 do fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7c3de-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="7c3de-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c3de-113">PARAMETERS</span></span>

### <span data-ttu-id="7c3de-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7c3de-114">-DataFactoryName</span></span>
<span data-ttu-id="7c3de-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7c3de-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c3de-116">-DefaultProfile</span></span>
<span data-ttu-id="7c3de-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c3de-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7c3de-118">-Force</span></span>
<span data-ttu-id="7c3de-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="7c3de-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="7c3de-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c3de-120">-InputObject</span></span>
<span data-ttu-id="7c3de-121">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="7c3de-121">The data flow object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3de-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7c3de-122">-Name</span></span>
<span data-ttu-id="7c3de-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="7c3de-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c3de-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c3de-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c3de-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c3de-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3de-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c3de-126">-ResourceId</span></span>
<span data-ttu-id="7c3de-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c3de-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c3de-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c3de-128">-PassThru</span></span>
<span data-ttu-id="7c3de-129">Se especificado, a gravação será true caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7c3de-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7c3de-130">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="7c3de-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="7c3de-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c3de-131">-Confirm</span></span>
<span data-ttu-id="7c3de-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c3de-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c3de-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c3de-133">-WhatIf</span></span>
<span data-ttu-id="7c3de-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c3de-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c3de-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c3de-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c3de-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c3de-136">CommonParameters</span></span>
<span data-ttu-id="7c3de-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c3de-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c3de-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c3de-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c3de-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c3de-139">INPUTS</span></span>

### <span data-ttu-id="7c3de-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7c3de-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="7c3de-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7c3de-141">System.String</span></span>

## <span data-ttu-id="7c3de-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c3de-142">OUTPUTS</span></span>

### <span data-ttu-id="7c3de-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="7c3de-143">System.Void</span></span>

### <span data-ttu-id="7c3de-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c3de-144">System.Boolean</span></span>

## <span data-ttu-id="7c3de-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c3de-145">NOTES</span></span>
<span data-ttu-id="7c3de-146">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="7c3de-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7c3de-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c3de-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c3de-148">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="7c3de-148">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="7c3de-149">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="7c3de-149">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

