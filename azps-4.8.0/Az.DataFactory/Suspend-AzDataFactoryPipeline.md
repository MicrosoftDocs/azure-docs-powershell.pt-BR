---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: f2538ecf8d4f6f962be85196ca49b8a0958f69e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113671"
---
# <span data-ttu-id="d5a77-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="d5a77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5a77-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a77-103">Suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d5a77-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="d5a77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5a77-104">SYNTAX</span></span>

### <span data-ttu-id="d5a77-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5a77-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a77-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d5a77-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a77-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5a77-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a77-108">O cmdlet **Suspend-AzDataFactoryPipeline** suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d5a77-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="d5a77-109">Você pode retomar o pipeline usando o cmdlet Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="d5a77-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="d5a77-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5a77-110">EXAMPLES</span></span>

### <span data-ttu-id="d5a77-111">Exemplo 1: suspender um pipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d5a77-112">Esse comando suspende o pipeline chamado DPWikiSample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d5a77-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d5a77-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="d5a77-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d5a77-114">OS</span><span class="sxs-lookup"><span data-stu-id="d5a77-114">PARAMETERS</span></span>

### <span data-ttu-id="d5a77-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="d5a77-115">-DataFactory</span></span>
<span data-ttu-id="d5a77-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d5a77-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d5a77-117">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d5a77-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5a77-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d5a77-118">-DataFactoryName</span></span>
<span data-ttu-id="d5a77-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d5a77-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d5a77-120">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d5a77-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5a77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a77-121">-DefaultProfile</span></span>
<span data-ttu-id="d5a77-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d5a77-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a77-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5a77-123">-Name</span></span>
<span data-ttu-id="d5a77-124">Especifica o nome do pipeline para suspender.</span><span class="sxs-lookup"><span data-stu-id="d5a77-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="d5a77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a77-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5a77-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a77-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d5a77-127">Esse cmdlet suspende um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d5a77-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d5a77-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5a77-128">-Confirm</span></span>
<span data-ttu-id="d5a77-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5a77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a77-130">-WhatIf</span></span>
<span data-ttu-id="d5a77-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5a77-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a77-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5a77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a77-133">CommonParameters</span></span>
<span data-ttu-id="d5a77-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a77-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a77-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a77-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5a77-136">INPUTS</span></span>

### <span data-ttu-id="d5a77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a77-137">System.String</span></span>

### <span data-ttu-id="d5a77-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d5a77-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d5a77-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5a77-139">OUTPUTS</span></span>

### <span data-ttu-id="d5a77-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5a77-140">System.Boolean</span></span>

## <span data-ttu-id="d5a77-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5a77-141">NOTES</span></span>
* <span data-ttu-id="d5a77-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d5a77-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d5a77-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5a77-143">RELATED LINKS</span></span>

[<span data-ttu-id="d5a77-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="d5a77-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="d5a77-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="d5a77-147">Currículo-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d5a77-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="d5a77-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d5a77-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


