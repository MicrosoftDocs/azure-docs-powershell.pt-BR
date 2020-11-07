---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/resume-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Resume-AzDataFactoryPipeline.md
ms.openlocfilehash: 26b0073cafebbd3e24afae5e8265b4acc9f4b0a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778297"
---
# <span data-ttu-id="4c280-101">Resume-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-101">Resume-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="4c280-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c280-102">SYNOPSIS</span></span>
<span data-ttu-id="4c280-103">Retoma um pipeline suspenso na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4c280-103">Resumes a suspended pipeline in Data Factory.</span></span>

## <span data-ttu-id="4c280-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c280-104">SYNTAX</span></span>

### <span data-ttu-id="4c280-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c280-105">ByFactoryName (Default)</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c280-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4c280-106">ByFactoryObject</span></span>
```
Resume-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c280-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c280-107">DESCRIPTION</span></span>
<span data-ttu-id="4c280-108">O cmdlet **resume-AzDataFactoryPipeline** retoma um pipeline suspenso no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="4c280-108">The **Resume-AzDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="4c280-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c280-109">EXAMPLES</span></span>

### <span data-ttu-id="4c280-110">Exemplo 1: retomar um pipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="4c280-111">Esse comando retoma o pipeline chamado DPWikisample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4c280-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="4c280-112">Use o cmdlet **Suspend-AzDataFactoryPipeline** para suspender um pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c280-112">Use the **Suspend-AzDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="4c280-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="4c280-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="4c280-114">OS</span><span class="sxs-lookup"><span data-stu-id="4c280-114">PARAMETERS</span></span>

### <span data-ttu-id="4c280-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4c280-115">-DataFactory</span></span>
<span data-ttu-id="4c280-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="4c280-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4c280-117">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4c280-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c280-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4c280-118">-DataFactoryName</span></span>
<span data-ttu-id="4c280-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4c280-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4c280-120">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4c280-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c280-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c280-121">-DefaultProfile</span></span>
<span data-ttu-id="4c280-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4c280-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c280-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c280-123">-Name</span></span>
<span data-ttu-id="4c280-124">Especifica o nome do pipeline a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="4c280-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="4c280-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c280-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c280-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c280-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4c280-127">Esse cmdlet retoma um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4c280-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c280-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c280-128">-Confirm</span></span>
<span data-ttu-id="4c280-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c280-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c280-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c280-130">-WhatIf</span></span>
<span data-ttu-id="4c280-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c280-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c280-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c280-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c280-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c280-133">CommonParameters</span></span>
<span data-ttu-id="4c280-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c280-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c280-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c280-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c280-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c280-136">INPUTS</span></span>

### <span data-ttu-id="4c280-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4c280-137">System.String</span></span>

### <span data-ttu-id="4c280-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4c280-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="4c280-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c280-139">OUTPUTS</span></span>

### <span data-ttu-id="4c280-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c280-140">System.Boolean</span></span>

## <span data-ttu-id="4c280-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c280-141">NOTES</span></span>
* <span data-ttu-id="4c280-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="4c280-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4c280-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c280-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c280-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c280-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c280-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="4c280-147">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="4c280-147">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="4c280-148">Suspender-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="4c280-148">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


