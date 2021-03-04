---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5ea766b4c35e23a62a0764320a2f0491ea151586
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892521"
---
# <span data-ttu-id="11b31-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="11b31-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="11b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b31-102">SYNOPSIS</span></span>
<span data-ttu-id="11b31-103">Cria um conjuntos de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="11b31-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="11b31-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="11b31-104">SYNTAX</span></span>

### <span data-ttu-id="11b31-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="11b31-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b31-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="11b31-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b31-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="11b31-107">DESCRIPTION</span></span>
<span data-ttu-id="11b31-108">O Set-AzDataFactoryV2Dataset cmdlet cria um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="11b31-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="11b31-109">Se você especificar um nome para um conjuntos de dados que já existe, este cmdlet solicitará a confirmação antes de substituir o conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="11b31-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="11b31-110">Se você especificar o parâmetro Force, o cmdlet substituirá o conjuntos de dados existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="11b31-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="11b31-111">Execute essas operações na seguinte ordem: -- Criar um fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="11b31-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="11b31-112">-- Crie serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="11b31-112">-- Create linked services.</span></span>
<span data-ttu-id="11b31-113">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="11b31-113">-- Create datasets.</span></span>
<span data-ttu-id="11b31-114">-- Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="11b31-114">-- Create a pipeline.</span></span>
<span data-ttu-id="11b31-115">Se um conjuntos de dados com o mesmo nome já existir no fábrica de dados, esse cmdlet solicitará que você confirme se deve substituir o conjuntos de dados existente com o novo conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="11b31-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="11b31-116">Se você confirmar a substituição do conjuntos de dados existente, a definição do conjuntos de dados também será substituída.</span><span class="sxs-lookup"><span data-stu-id="11b31-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="11b31-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11b31-117">EXAMPLES</span></span>

### <span data-ttu-id="11b31-118">Exemplo 1: Criar um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="11b31-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="11b31-119">Este comando cria um grupo de dados chamado DA_WikipediaClickEvents no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="11b31-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="11b31-120">O comando baseia o conjuntos de dados em informações no arquivo DAWikipediaClickEvents.json.</span><span class="sxs-lookup"><span data-stu-id="11b31-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="11b31-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="11b31-121">PARAMETERS</span></span>

### <span data-ttu-id="11b31-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="11b31-122">-DataFactoryName</span></span>
<span data-ttu-id="11b31-123">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="11b31-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="11b31-124">Este cmdlet cria um conjuntos de dados no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="11b31-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="11b31-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b31-125">-DefaultProfile</span></span>
<span data-ttu-id="11b31-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="11b31-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b31-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="11b31-127">-DefinitionFile</span></span>
<span data-ttu-id="11b31-128">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="11b31-128">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b31-129">-Force</span><span class="sxs-lookup"><span data-stu-id="11b31-129">-Force</span></span>
<span data-ttu-id="11b31-130">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="11b31-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="11b31-131">-Name</span><span class="sxs-lookup"><span data-stu-id="11b31-131">-Name</span></span>
<span data-ttu-id="11b31-132">Especifica o nome do conjuntos de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="11b31-132">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b31-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b31-133">-ResourceGroupName</span></span>
<span data-ttu-id="11b31-134">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="11b31-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="11b31-135">Este cmdlet cria um conjunto de dados no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="11b31-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="11b31-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b31-136">-ResourceId</span></span>
<span data-ttu-id="11b31-137">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="11b31-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="11b31-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11b31-138">-Confirm</span></span>
<span data-ttu-id="11b31-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b31-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b31-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b31-140">-WhatIf</span></span>
<span data-ttu-id="11b31-141">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b31-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="11b31-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b31-142">CommonParameters</span></span>
<span data-ttu-id="11b31-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b31-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b31-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b31-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b31-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11b31-145">INPUTS</span></span>

### <span data-ttu-id="11b31-146">System.String</span><span class="sxs-lookup"><span data-stu-id="11b31-146">System.String</span></span>

## <span data-ttu-id="11b31-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="11b31-147">OUTPUTS</span></span>

### <span data-ttu-id="11b31-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="11b31-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="11b31-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="11b31-149">NOTES</span></span>
<span data-ttu-id="11b31-150">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="11b31-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="11b31-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11b31-151">RELATED LINKS</span></span>

[<span data-ttu-id="11b31-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="11b31-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="11b31-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="11b31-153">Remove-AzDataFactoryV2Dataset</span></span>]()
