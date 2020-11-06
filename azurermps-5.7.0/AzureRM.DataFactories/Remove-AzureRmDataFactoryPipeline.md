---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427587"
---
# <span data-ttu-id="5bbd9-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="5bbd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbd9-103">Remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bbd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bbd9-104">SYNTAX</span></span>

### <span data-ttu-id="5bbd9-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5bbd9-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5bbd9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5bbd9-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bbd9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bbd9-107">DESCRIPTION</span></span>
<span data-ttu-id="5bbd9-108">O cmdlet **Remove-AzureRmDataFactoryPipeline** remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="5bbd9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bbd9-109">EXAMPLES</span></span>

### <span data-ttu-id="5bbd9-110">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="5bbd9-111">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="5bbd9-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="5bbd9-113">OS</span><span class="sxs-lookup"><span data-stu-id="5bbd9-113">PARAMETERS</span></span>

### <span data-ttu-id="5bbd9-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="5bbd9-114">-DataFactory</span></span>
<span data-ttu-id="5bbd9-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="5bbd9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5bbd9-116">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5bbd9-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5bbd9-117">-DataFactoryName</span></span>
<span data-ttu-id="5bbd9-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5bbd9-119">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5bbd9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbd9-120">-DefaultProfile</span></span>
<span data-ttu-id="5bbd9-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5bbd9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bbd9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5bbd9-122">-Force</span></span>
<span data-ttu-id="5bbd9-123">Indica que esse cmdlet Remove um pipeline sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbd9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bbd9-124">-Name</span></span>
<span data-ttu-id="5bbd9-125">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="5bbd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="5bbd9-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5bbd9-128">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5bbd9-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5bbd9-129">-Confirm</span></span>
<span data-ttu-id="5bbd9-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bbd9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bbd9-131">-WhatIf</span></span>
<span data-ttu-id="5bbd9-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bbd9-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bbd9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbd9-134">CommonParameters</span></span>
<span data-ttu-id="5bbd9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbd9-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbd9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbd9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bbd9-137">INPUTS</span></span>

### <span data-ttu-id="5bbd9-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5bbd9-138">None</span></span>
<span data-ttu-id="5bbd9-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5bbd9-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bbd9-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bbd9-140">OUTPUTS</span></span>

### <span data-ttu-id="5bbd9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bbd9-141">System.Boolean</span></span>

## <span data-ttu-id="5bbd9-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bbd9-142">NOTES</span></span>
* <span data-ttu-id="5bbd9-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="5bbd9-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5bbd9-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bbd9-144">RELATED LINKS</span></span>

[<span data-ttu-id="5bbd9-145">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5bbd9-146">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5bbd9-147">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="5bbd9-148">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="5bbd9-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="5bbd9-149">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="5bbd9-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


