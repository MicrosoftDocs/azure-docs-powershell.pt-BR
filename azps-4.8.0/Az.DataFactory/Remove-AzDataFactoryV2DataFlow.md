---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b441c354214775f3f6aad425513a953fbefe7810
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414876"
---
# <span data-ttu-id="64d9f-101">Remove-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="64d9f-101">Remove-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="64d9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="64d9f-103">Remove um fluxo de dados do Data Factory.</span><span class="sxs-lookup"><span data-stu-id="64d9f-103">Removes a data flow from Data Factory.</span></span>

## <span data-ttu-id="64d9f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64d9f-104">SYNTAX</span></span>

### <span data-ttu-id="64d9f-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="64d9f-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64d9f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="64d9f-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2DataFlow [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d9f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="64d9f-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2DataFlow [-Force] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64d9f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="64d9f-108">DESCRIPTION</span></span>
<span data-ttu-id="64d9f-109">O Remove-AzDataFactoryV2DataFlow cmdlet remove um fluxo de dados do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="64d9f-109">The Remove-AzDataFactoryV2DataFlow cmdlet removes a data flow from Azure Data Factory.</span></span>

## <span data-ttu-id="64d9f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64d9f-110">EXAMPLES</span></span>

### <span data-ttu-id="64d9f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64d9f-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Remove-AzDataFactoryV2DataFlow -ResourceGroupName adf -DataFactoryName WikiADF -DataFlowName "dataflow5"

Confirm
Are you sure you want to remove data flow 'dataflow5' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\WINDOWS\system32>
```

<span data-ttu-id="64d9f-112">Esse comando remove o fluxo de dados chamado dataflow5 da fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="64d9f-112">This command removes the data flow named dataflow5 from the data factory named WikiADF.</span></span>

## <span data-ttu-id="64d9f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64d9f-113">PARAMETERS</span></span>

### <span data-ttu-id="64d9f-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="64d9f-114">-DataFactoryName</span></span>
<span data-ttu-id="64d9f-115">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="64d9f-115">The data factory name.</span></span>

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

### <span data-ttu-id="64d9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d9f-116">-DefaultProfile</span></span>
<span data-ttu-id="64d9f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64d9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64d9f-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="64d9f-118">-Force</span></span>
<span data-ttu-id="64d9f-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="64d9f-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="64d9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64d9f-120">-InputObject</span></span>
<span data-ttu-id="64d9f-121">O objeto de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="64d9f-121">The data flow object.</span></span>

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

### <span data-ttu-id="64d9f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="64d9f-122">-Name</span></span>
<span data-ttu-id="64d9f-123">O nome do fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="64d9f-123">The data flow name.</span></span>

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

### <span data-ttu-id="64d9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64d9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="64d9f-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64d9f-125">The resource group name.</span></span>

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

### <span data-ttu-id="64d9f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64d9f-126">-ResourceId</span></span>
<span data-ttu-id="64d9f-127">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="64d9f-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="64d9f-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64d9f-128">-PassThru</span></span>
<span data-ttu-id="64d9f-129">Se especificado, a gravação será verdadeira caso a operação seja bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="64d9f-129">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="64d9f-130">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="64d9f-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="64d9f-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="64d9f-131">-Confirm</span></span>
<span data-ttu-id="64d9f-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64d9f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64d9f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d9f-133">-WhatIf</span></span>
<span data-ttu-id="64d9f-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="64d9f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64d9f-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64d9f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64d9f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d9f-136">CommonParameters</span></span>
<span data-ttu-id="64d9f-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d9f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d9f-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64d9f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d9f-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="64d9f-139">INPUTS</span></span>

### <span data-ttu-id="64d9f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="64d9f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="64d9f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="64d9f-141">System.String</span></span>

## <span data-ttu-id="64d9f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="64d9f-142">OUTPUTS</span></span>

### <span data-ttu-id="64d9f-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="64d9f-143">System.Void</span></span>

### <span data-ttu-id="64d9f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64d9f-144">System.Boolean</span></span>

## <span data-ttu-id="64d9f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="64d9f-145">NOTES</span></span>
<span data-ttu-id="64d9f-146">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="64d9f-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="64d9f-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64d9f-147">RELATED LINKS</span></span>



