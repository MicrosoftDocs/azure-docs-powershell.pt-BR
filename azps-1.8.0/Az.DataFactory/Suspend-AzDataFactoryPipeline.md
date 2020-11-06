---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/suspend-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Suspend-AzDataFactoryPipeline.md
ms.openlocfilehash: 2f3d48044b06292b18b1254adf1e2bc6d0698d4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601108"
---
# <span data-ttu-id="38fef-101">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-101">Suspend-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="38fef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38fef-102">SYNOPSIS</span></span>
<span data-ttu-id="38fef-103">Suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="38fef-103">Suspends a pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="38fef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38fef-104">SYNTAX</span></span>

### <span data-ttu-id="38fef-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="38fef-105">ByFactoryName (Default)</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38fef-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="38fef-106">ByFactoryObject</span></span>
```
Suspend-AzDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38fef-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38fef-107">DESCRIPTION</span></span>
<span data-ttu-id="38fef-108">O cmdlet **Suspend-AzDataFactoryPipeline** suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="38fef-108">The **Suspend-AzDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="38fef-109">Você pode retomar o pipeline usando o cmdlet Resume-AzDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="38fef-109">You can resume the pipeline by using the Resume-AzDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="38fef-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38fef-110">EXAMPLES</span></span>

### <span data-ttu-id="38fef-111">Exemplo 1: suspender um pipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="38fef-112">Esse comando suspende o pipeline chamado DPWikiSample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="38fef-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="38fef-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="38fef-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="38fef-114">OS</span><span class="sxs-lookup"><span data-stu-id="38fef-114">PARAMETERS</span></span>

### <span data-ttu-id="38fef-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="38fef-115">-DataFactory</span></span>
<span data-ttu-id="38fef-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="38fef-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="38fef-117">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38fef-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="38fef-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="38fef-118">-DataFactoryName</span></span>
<span data-ttu-id="38fef-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="38fef-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="38fef-120">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38fef-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="38fef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38fef-121">-DefaultProfile</span></span>
<span data-ttu-id="38fef-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="38fef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38fef-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="38fef-123">-Name</span></span>
<span data-ttu-id="38fef-124">Especifica o nome do pipeline para suspender.</span><span class="sxs-lookup"><span data-stu-id="38fef-124">Specifies the name of the pipeline to suspend.</span></span>

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

### <span data-ttu-id="38fef-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38fef-125">-ResourceGroupName</span></span>
<span data-ttu-id="38fef-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="38fef-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="38fef-127">Esse cmdlet suspende um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="38fef-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="38fef-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38fef-128">-Confirm</span></span>
<span data-ttu-id="38fef-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38fef-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38fef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38fef-130">-WhatIf</span></span>
<span data-ttu-id="38fef-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38fef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38fef-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38fef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38fef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38fef-133">CommonParameters</span></span>
<span data-ttu-id="38fef-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38fef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38fef-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38fef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38fef-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38fef-136">INPUTS</span></span>

### <span data-ttu-id="38fef-137">System. String</span><span class="sxs-lookup"><span data-stu-id="38fef-137">System.String</span></span>

### <span data-ttu-id="38fef-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="38fef-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="38fef-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38fef-139">OUTPUTS</span></span>

### <span data-ttu-id="38fef-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38fef-140">System.Boolean</span></span>

## <span data-ttu-id="38fef-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38fef-141">NOTES</span></span>
* <span data-ttu-id="38fef-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="38fef-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="38fef-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38fef-143">RELATED LINKS</span></span>

[<span data-ttu-id="38fef-144">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-144">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="38fef-145">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-145">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="38fef-146">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-146">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="38fef-147">Currículo-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="38fef-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="38fef-148">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="38fef-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


