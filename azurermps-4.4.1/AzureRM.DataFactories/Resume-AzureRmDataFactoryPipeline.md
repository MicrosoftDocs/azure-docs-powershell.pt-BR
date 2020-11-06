---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F522841A-4246-4028-A754-393D8DADD924
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Resume-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 63bb7337e7473d27838b08763ebe2a7de14514a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427975"
---
# <span data-ttu-id="01f05-101">Resume-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-101">Resume-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="01f05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01f05-102">SYNOPSIS</span></span>
<span data-ttu-id="01f05-103">Retoma um pipeline suspenso na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="01f05-103">Resumes a suspended pipeline in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01f05-104">SYNTAX</span></span>

### <span data-ttu-id="01f05-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="01f05-105">ByFactoryName (Default)</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01f05-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="01f05-106">ByFactoryObject</span></span>
```
Resume-AzureRmDataFactoryPipeline [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f05-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01f05-107">DESCRIPTION</span></span>
<span data-ttu-id="01f05-108">O cmdlet **resume-AzureRmDataFactoryPipeline** retoma um pipeline suspenso no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="01f05-108">The **Resume-AzureRmDataFactoryPipeline** cmdlet resumes a suspended pipeline in Azure Data Factory.</span></span>

## <span data-ttu-id="01f05-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01f05-109">EXAMPLES</span></span>

### <span data-ttu-id="01f05-110">Exemplo 1: retomar um pipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-110">Example 1: Resume a pipeline</span></span>
```
PS C:\>Resume-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to resume pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="01f05-111">Esse comando retoma o pipeline chamado DPWikisample no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="01f05-111">This command resumes the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="01f05-112">Use o cmdlet **Suspend-AzureRmDataFactoryPipeline** para suspender um pipeline.</span><span class="sxs-lookup"><span data-stu-id="01f05-112">Use the **Suspend-AzureRmDataFactoryPipeline** cmdlet to suspend a pipeline.</span></span>
<span data-ttu-id="01f05-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="01f05-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="01f05-114">OS</span><span class="sxs-lookup"><span data-stu-id="01f05-114">PARAMETERS</span></span>

### <span data-ttu-id="01f05-115">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="01f05-115">-DataFactory</span></span>
<span data-ttu-id="01f05-116">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="01f05-116">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="01f05-117">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="01f05-117">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="01f05-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="01f05-118">-DataFactoryName</span></span>
<span data-ttu-id="01f05-119">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="01f05-119">Specifies the name of a data factory.</span></span>
<span data-ttu-id="01f05-120">Esse cmdlet retoma um pipeline que pertence à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="01f05-120">This cmdlet resumes a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="01f05-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="01f05-121">-Name</span></span>
<span data-ttu-id="01f05-122">Especifica o nome do pipeline a ser retomado.</span><span class="sxs-lookup"><span data-stu-id="01f05-122">Specifies the name of the pipeline to resume.</span></span>

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

### <span data-ttu-id="01f05-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f05-123">-ResourceGroupName</span></span>
<span data-ttu-id="01f05-124">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="01f05-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="01f05-125">Esse cmdlet retoma um pipeline que pertence ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="01f05-125">This cmdlet resumes a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="01f05-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01f05-126">-Confirm</span></span>
<span data-ttu-id="01f05-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01f05-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f05-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f05-128">-WhatIf</span></span>
<span data-ttu-id="01f05-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01f05-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f05-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01f05-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f05-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f05-131">-DefaultProfile</span></span>
<span data-ttu-id="01f05-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01f05-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f05-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f05-133">CommonParameters</span></span>
<span data-ttu-id="01f05-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f05-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f05-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f05-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f05-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01f05-136">INPUTS</span></span>

## <span data-ttu-id="01f05-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01f05-137">OUTPUTS</span></span>

### <span data-ttu-id="01f05-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01f05-138">System.Boolean</span></span>

## <span data-ttu-id="01f05-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01f05-139">NOTES</span></span>
* <span data-ttu-id="01f05-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="01f05-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="01f05-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01f05-141">RELATED LINKS</span></span>

[<span data-ttu-id="01f05-142">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-142">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="01f05-143">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-143">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="01f05-144">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-144">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="01f05-145">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="01f05-145">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="01f05-146">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="01f05-146">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


