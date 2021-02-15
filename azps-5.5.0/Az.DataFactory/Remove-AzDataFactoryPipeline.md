---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111966"
---
# <span data-ttu-id="138a9-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="138a9-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="138a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="138a9-102">SYNOPSIS</span></span>
<span data-ttu-id="138a9-103">Remove um pipeline do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="138a9-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="138a9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="138a9-104">SYNTAX</span></span>

### <span data-ttu-id="138a9-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="138a9-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="138a9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="138a9-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="138a9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="138a9-107">DESCRIPTION</span></span>
<span data-ttu-id="138a9-108">O cmdlet **Remove-AzDataFactory Pipelineline** remove um pipeline do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="138a9-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="138a9-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="138a9-109">EXAMPLES</span></span>

### <span data-ttu-id="138a9-110">Exemplo 1: Remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="138a9-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="138a9-111">Este cmdlet remove o pipeline chamado DPWikisample da fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="138a9-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="138a9-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="138a9-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="138a9-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="138a9-113">PARAMETERS</span></span>

### <span data-ttu-id="138a9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="138a9-114">-DataFactory</span></span>
<span data-ttu-id="138a9-115">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="138a9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="138a9-116">Este cmdlet remove um pipeline da fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="138a9-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138a9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="138a9-117">-DataFactoryName</span></span>
<span data-ttu-id="138a9-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="138a9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="138a9-119">Este cmdlet remove um pipeline da fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="138a9-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="138a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="138a9-120">-DefaultProfile</span></span>
<span data-ttu-id="138a9-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="138a9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="138a9-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="138a9-122">-Force</span></span>
<span data-ttu-id="138a9-123">Indica que esse cmdlet remove um pipeline sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="138a9-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="138a9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="138a9-124">-Name</span></span>
<span data-ttu-id="138a9-125">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="138a9-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="138a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="138a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="138a9-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="138a9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="138a9-128">Este cmdlet remove um pipeline do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="138a9-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="138a9-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="138a9-129">-Confirm</span></span>
<span data-ttu-id="138a9-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="138a9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="138a9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="138a9-131">-WhatIf</span></span>
<span data-ttu-id="138a9-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="138a9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="138a9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="138a9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="138a9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="138a9-134">CommonParameters</span></span>
<span data-ttu-id="138a9-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="138a9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="138a9-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="138a9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="138a9-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="138a9-137">INPUTS</span></span>

### <span data-ttu-id="138a9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="138a9-138">System.String</span></span>

### <span data-ttu-id="138a9-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="138a9-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="138a9-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="138a9-140">OUTPUTS</span></span>

### <span data-ttu-id="138a9-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="138a9-141">System.Void</span></span>

## <span data-ttu-id="138a9-142">Notas</span><span class="sxs-lookup"><span data-stu-id="138a9-142">NOTES</span></span>
* <span data-ttu-id="138a9-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="138a9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="138a9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="138a9-144">RELATED LINKS</span></span>

[<span data-ttu-id="138a9-145">Get-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="138a9-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="138a9-146">New-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="138a9-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="138a9-147">Resume-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="138a9-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="138a9-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="138a9-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="138a9-149">Suspend-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="138a9-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


