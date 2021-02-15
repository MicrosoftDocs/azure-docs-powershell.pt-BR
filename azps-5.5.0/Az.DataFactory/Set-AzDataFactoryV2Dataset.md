---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118809"
---
# <span data-ttu-id="4c013-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4c013-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="4c013-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c013-102">SYNOPSIS</span></span>
<span data-ttu-id="4c013-103">Cria um conjuntos de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4c013-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="4c013-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c013-104">SYNTAX</span></span>

### <span data-ttu-id="4c013-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="4c013-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c013-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4c013-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c013-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c013-107">DESCRIPTION</span></span>
<span data-ttu-id="4c013-108">O Set-AzDataFactoryV2Dataset cmdlet cria um conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="4c013-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="4c013-109">Se você especificar um nome para um conjuntos de dados que já existe, esse cmdlet solicitará confirmação antes de substituir o conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c013-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="4c013-110">Se você especificar o parâmetro Forçar, o cmdlet substituirá o conjuntos de dados existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="4c013-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="4c013-111">Execute essas operações na seguinte ordem: - Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4c013-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="4c013-112">- Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="4c013-112">-- Create linked services.</span></span>
<span data-ttu-id="4c013-113">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c013-113">-- Create datasets.</span></span>
<span data-ttu-id="4c013-114">- Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c013-114">-- Create a pipeline.</span></span>
<span data-ttu-id="4c013-115">Se um conjuntos de dados com o mesmo nome já existir no fábrica de dados, esse cmdlet solicitará que você confirme se deve substituir o conjuntos de dados existente com o novo conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="4c013-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="4c013-116">Se você confirmar para substituir o conjuntos de dados existente, a definição de conjuntos de dados também será substituída.</span><span class="sxs-lookup"><span data-stu-id="4c013-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="4c013-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c013-117">EXAMPLES</span></span>

### <span data-ttu-id="4c013-118">Exemplo 1: Criar um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="4c013-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="4c013-119">Esse comando cria um grupo de dados chamado DA_WikipediaClickEvents na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4c013-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="4c013-120">O comando baseia o conjuntos de dados em informações no DAWikipediaClickEvents.jsno arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c013-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="4c013-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c013-121">PARAMETERS</span></span>

### <span data-ttu-id="4c013-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4c013-122">-DataFactoryName</span></span>
<span data-ttu-id="4c013-123">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4c013-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4c013-124">Esse cmdlet cria um conjuntos de dados no fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4c013-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c013-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c013-125">-DefaultProfile</span></span>
<span data-ttu-id="4c013-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4c013-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c013-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="4c013-127">-DefinitionFile</span></span>
<span data-ttu-id="4c013-128">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="4c013-128">The JSON file path.</span></span>

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

### <span data-ttu-id="4c013-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="4c013-129">-Force</span></span>
<span data-ttu-id="4c013-130">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="4c013-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4c013-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c013-131">-Name</span></span>
<span data-ttu-id="4c013-132">Especifica o nome do conjuntos de dados a ser criado.</span><span class="sxs-lookup"><span data-stu-id="4c013-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="4c013-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c013-133">-ResourceGroupName</span></span>
<span data-ttu-id="4c013-134">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c013-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4c013-135">Esse cmdlet cria um conjunto de dados no grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4c013-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4c013-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c013-136">-ResourceId</span></span>
<span data-ttu-id="4c013-137">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c013-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4c013-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4c013-138">-Confirm</span></span>
<span data-ttu-id="4c013-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c013-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c013-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c013-140">-WhatIf</span></span>
<span data-ttu-id="4c013-141">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c013-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4c013-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c013-142">CommonParameters</span></span>
<span data-ttu-id="4c013-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c013-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c013-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c013-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c013-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c013-145">INPUTS</span></span>

### <span data-ttu-id="4c013-146">System.String</span><span class="sxs-lookup"><span data-stu-id="4c013-146">System.String</span></span>

## <span data-ttu-id="4c013-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c013-147">OUTPUTS</span></span>

### <span data-ttu-id="4c013-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="4c013-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="4c013-149">Notas</span><span class="sxs-lookup"><span data-stu-id="4c013-149">NOTES</span></span>
<span data-ttu-id="4c013-150">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="4c013-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4c013-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c013-151">RELATED LINKS</span></span>

[<span data-ttu-id="4c013-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4c013-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="4c013-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="4c013-153">Remove-AzDataFactoryV2Dataset</span></span>]()
