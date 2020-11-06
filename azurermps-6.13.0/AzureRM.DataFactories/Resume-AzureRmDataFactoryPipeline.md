---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/resume-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 298a86c05cc318fbe360cddd2341901070601d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427245"
---
# <span data-ttu-id="d7ffe-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="d7ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="d7ffe-103">Retoma um pipeline suspenso na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7ffe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7ffe-104">SYNTAX</span></span>

### <span data-ttu-id="d7ffe-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7ffe-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7ffe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7ffe-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7ffe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7ffe-107">DESCRIPTION</span></span>
<span data-ttu-id="d7ffe-108">O cmdlet **resume-AzureRmDataFactoryPipeline** retoma um pipeline suspenso no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="d7ffe-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7ffe-109">EXAMPLES</span></span>

### <span data-ttu-id="d7ffe-110">Exemplo 1: retomar um pipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="d7ffe-111">Esse comando retoma o pipeline chamado DPWikisample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d7ffe-112">Use o cmdlet **Suspend-AzureRmDataFactoryPipeline** para suspender um pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="d7ffe-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d7ffe-114">OS</span><span class="sxs-lookup"><span data-stu-id="d7ffe-114">PARAMETERS</span></span>

### <span data-ttu-id="d7ffe-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="d7ffe-115">-DataFactory</span></span>
<span data-ttu-id="d7ffe-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d7ffe-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7ffe-117">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7ffe-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d7ffe-118">-DataFactoryName</span></span>
<span data-ttu-id="d7ffe-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7ffe-120">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7ffe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7ffe-121">-DefaultProfile</span></span>
<span data-ttu-id="d7ffe-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d7ffe-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7ffe-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7ffe-123">-Name</span></span>
<span data-ttu-id="d7ffe-124">Especifica o nome do pipeline a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-124">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="d7ffe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7ffe-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7ffe-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7ffe-127">Esse cmdlet retoma um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-127">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7ffe-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7ffe-128">-Confirm</span></span>
<span data-ttu-id="d7ffe-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7ffe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7ffe-130">-WhatIf</span></span>
<span data-ttu-id="d7ffe-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7ffe-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7ffe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7ffe-133">CommonParameters</span></span>
<span data-ttu-id="d7ffe-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7ffe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7ffe-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7ffe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7ffe-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7ffe-136">INPUTS</span></span>

### <span data-ttu-id="d7ffe-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d7ffe-137">System.String</span></span>

### <span data-ttu-id="d7ffe-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d7ffe-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="d7ffe-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7ffe-139">OUTPUTS</span></span>

### <span data-ttu-id="d7ffe-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d7ffe-140">System.Boolean</span></span>

## <span data-ttu-id="d7ffe-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7ffe-141">NOTES</span></span>
* <span data-ttu-id="d7ffe-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d7ffe-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7ffe-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7ffe-143">RELATED LINKS</span></span>

[<span data-ttu-id="d7ffe-144">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-144">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7ffe-145">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-145">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7ffe-146">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-146">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="d7ffe-147">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d7ffe-147">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="d7ffe-148">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="d7ffe-148">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

