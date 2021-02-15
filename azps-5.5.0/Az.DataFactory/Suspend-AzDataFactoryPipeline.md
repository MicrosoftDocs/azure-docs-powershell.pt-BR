---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118805"
---
# <span data-ttu-id="af357-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="af357-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="af357-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="af357-102">SYNOPSIS</span></span>
<span data-ttu-id="af357-103">Suspende um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="af357-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="af357-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af357-104">SYNTAX</span></span>

### <span data-ttu-id="af357-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="af357-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af357-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="af357-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af357-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="af357-107">DESCRIPTION</span></span>
<span data-ttu-id="af357-108">O cmdlet **Suspend-AzDataFactory Pipelineline** suspende um pipeline no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="af357-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="af357-109">Você pode retomar o pipeline usando o cmdlet Resume-AzDataFactoryPipeline usuário.</span><span class="sxs-lookup"><span data-stu-id="af357-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="af357-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="af357-110">EXAMPLES</span></span>

### <span data-ttu-id="af357-111">Exemplo 1: Suspender um pipeline</span><span class="sxs-lookup"><span data-stu-id="af357-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="af357-112">Este comando suspende o pipeline chamado DPWikiSample na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="af357-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="af357-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="af357-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="af357-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af357-114">PARAMETERS</span></span>

### <span data-ttu-id="af357-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="af357-115">-DataFactory</span></span>
<span data-ttu-id="af357-116">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="af357-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="af357-117">Este cmdlet suspende um pipeline que pertence ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="af357-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="af357-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="af357-118">-DataFactoryName</span></span>
<span data-ttu-id="af357-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="af357-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="af357-120">Este cmdlet suspende um pipeline que pertence ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="af357-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="af357-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af357-121">-DefaultProfile</span></span>
<span data-ttu-id="af357-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="af357-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af357-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="af357-123">-Name</span></span>
<span data-ttu-id="af357-124">Especifica o nome do pipeline a ser suspenso.</span><span class="sxs-lookup"><span data-stu-id="af357-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="af357-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af357-125">-ResourceGroupName</span></span>
<span data-ttu-id="af357-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="af357-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="af357-127">Este cmdlet suspende um pipeline que pertence ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="af357-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="af357-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="af357-128">-Confirm</span></span>
<span data-ttu-id="af357-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af357-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af357-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af357-130">-WhatIf</span></span>
<span data-ttu-id="af357-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="af357-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af357-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af357-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af357-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af357-133">CommonParameters</span></span>
<span data-ttu-id="af357-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af357-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af357-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af357-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af357-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="af357-136">INPUTS</span></span>

### <span data-ttu-id="af357-137">System.String</span><span class="sxs-lookup"><span data-stu-id="af357-137">System.String</span></span>

### <span data-ttu-id="af357-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="af357-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="af357-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="af357-139">OUTPUTS</span></span>

### <span data-ttu-id="af357-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af357-140">System.Boolean</span></span>

## <span data-ttu-id="af357-141">Notas</span><span class="sxs-lookup"><span data-stu-id="af357-141">NOTES</span></span>
* <span data-ttu-id="af357-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="af357-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="af357-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af357-143">RELATED LINKS</span></span>

[<span data-ttu-id="af357-144">Get-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="af357-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="af357-145">New-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="af357-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="af357-146">Remove-AzDataFactoryDataDataLine</span><span class="sxs-lookup"><span data-stu-id="af357-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="af357-147">Resume-AzDataFactoryFactline</span><span class="sxs-lookup"><span data-stu-id="af357-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="af357-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="af357-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


