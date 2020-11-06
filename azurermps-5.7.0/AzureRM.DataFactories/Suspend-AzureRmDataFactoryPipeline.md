---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1FF0B0F9-4B2C-46BC-8BED-12BE865E4480
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/suspend-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Suspend-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 98c8d5778e827b251c5d0c9b919bde9f86e2c41e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602155"
---
# <span data-ttu-id="47701-101">Suspend-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="47701-101">Suspend-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="47701-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47701-102">SYNOPSIS</span></span>
<span data-ttu-id="47701-103">Suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="47701-103">Suspends a pipeline in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47701-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47701-104">SYNTAX</span></span>

### <span data-ttu-id="47701-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="47701-105">ByFactoryName (Default)</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47701-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="47701-106">ByFactoryObject</span></span>
```
Suspend-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47701-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47701-107">DESCRIPTION</span></span>
<span data-ttu-id="47701-108">O cmdlet **Suspend-AzureRmDataFactoryPipeline** suspende um pipeline no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="47701-108">The **Suspend-AzureRmDataFactoryPipeline** cmdlet suspends a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="47701-109">Você pode retomar o pipeline usando o cmdlet Resume-AzureRmDataFactoryPipeline.</span><span class="sxs-lookup"><span data-stu-id="47701-109">You can resume the pipeline by using the Resume-AzureRmDataFactoryPipeline cmdlet.</span></span>

## <span data-ttu-id="47701-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47701-110">EXAMPLES</span></span>

### <span data-ttu-id="47701-111">Exemplo 1: suspender um pipeline</span><span class="sxs-lookup"><span data-stu-id="47701-111">Example 1: Suspend a pipeline</span></span>
```
PS C:\>Suspend-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikiSample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to suspend pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="47701-112">Esse comando suspende o pipeline chamado DPWikiSample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="47701-112">This command suspends the pipeline named DPWikiSample in the data factory named WikiADF.</span></span>
<span data-ttu-id="47701-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="47701-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="47701-114">OS</span><span class="sxs-lookup"><span data-stu-id="47701-114">PARAMETERS</span></span>

### <span data-ttu-id="47701-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="47701-115">-DataFactory</span></span>
<span data-ttu-id="47701-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="47701-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="47701-117">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="47701-117">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47701-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="47701-118">-DataFactoryName</span></span>
<span data-ttu-id="47701-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="47701-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="47701-120">Esse cmdlet suspende um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="47701-120">This cmdlet suspends a pipeline that belongs to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47701-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47701-121">-DefaultProfile</span></span>
<span data-ttu-id="47701-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="47701-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47701-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="47701-123">-Name</span></span>
<span data-ttu-id="47701-124">Especifica o nome do pipeline para suspender.</span><span class="sxs-lookup"><span data-stu-id="47701-124">Specifies the name of the pipeline to suspend.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47701-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47701-125">-ResourceGroupName</span></span>
<span data-ttu-id="47701-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="47701-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="47701-127">Esse cmdlet suspende um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="47701-127">This cmdlet suspends a pipeline that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47701-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47701-128">-Confirm</span></span>
<span data-ttu-id="47701-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47701-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47701-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47701-130">-WhatIf</span></span>
<span data-ttu-id="47701-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47701-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47701-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47701-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47701-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47701-133">CommonParameters</span></span>
<span data-ttu-id="47701-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47701-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47701-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47701-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47701-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47701-136">INPUTS</span></span>

### <span data-ttu-id="47701-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="47701-137">None</span></span>
<span data-ttu-id="47701-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="47701-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="47701-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47701-139">OUTPUTS</span></span>

### <span data-ttu-id="47701-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47701-140">System.Boolean</span></span>

## <span data-ttu-id="47701-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47701-141">NOTES</span></span>
* <span data-ttu-id="47701-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="47701-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="47701-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47701-143">RELATED LINKS</span></span>

[<span data-ttu-id="47701-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="47701-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="47701-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="47701-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="47701-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="47701-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="47701-147">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="47701-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="47701-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="47701-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


