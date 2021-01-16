---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261206"
---
# <span data-ttu-id="c5c56-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5c56-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="c5c56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5c56-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c56-103">Cria um conjunto de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c5c56-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="c5c56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5c56-104">SYNTAX</span></span>

### <span data-ttu-id="c5c56-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c5c56-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5c56-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c56-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5c56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5c56-107">DESCRIPTION</span></span>
<span data-ttu-id="c5c56-108">O cmdlet Set-AzDataFactoryV2Dataset cria um DataSet no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c5c56-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="c5c56-109">Se você especificar um nome para um DataSet que já existe, esse cmdlet solicitará confirmação antes de substituir o DataSet.</span><span class="sxs-lookup"><span data-stu-id="c5c56-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="c5c56-110">Se você especificar o parâmetro Force, o cmdlet substituirá o DataSet existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5c56-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="c5c56-111">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c5c56-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="c5c56-112">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="c5c56-112">-- Create linked services.</span></span>
<span data-ttu-id="c5c56-113">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="c5c56-113">-- Create datasets.</span></span>
<span data-ttu-id="c5c56-114">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="c5c56-114">-- Create a pipeline.</span></span>
<span data-ttu-id="c5c56-115">Se um conjunto de dados com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o conjunto de dados existente pelo novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="c5c56-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="c5c56-116">Se você confirmar para substituir o conjunto de um conjunto de um existente, a definição de DataSet também será substituída.</span><span class="sxs-lookup"><span data-stu-id="c5c56-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="c5c56-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5c56-117">EXAMPLES</span></span>

### <span data-ttu-id="c5c56-118">Exemplo 1: criar um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="c5c56-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="c5c56-119">Esse comando cria um conjunto de dados chamado DA_WikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c5c56-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="c5c56-120">O comando baseia o DataSet nas informações do DAWikipediaClickEvents.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="c5c56-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="c5c56-121">OS</span><span class="sxs-lookup"><span data-stu-id="c5c56-121">PARAMETERS</span></span>

### <span data-ttu-id="c5c56-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c5c56-122">-DataFactoryName</span></span>
<span data-ttu-id="c5c56-123">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c5c56-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c5c56-124">Esse cmdlet cria um conjunto de dados na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c5c56-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5c56-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c56-125">-DefaultProfile</span></span>
<span data-ttu-id="c5c56-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c56-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5c56-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c5c56-127">-DefinitionFile</span></span>
<span data-ttu-id="c5c56-128">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="c5c56-128">The JSON file path.</span></span>

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

### <span data-ttu-id="c5c56-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c5c56-129">-Force</span></span>
<span data-ttu-id="c5c56-130">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="c5c56-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c5c56-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5c56-131">-Name</span></span>
<span data-ttu-id="c5c56-132">Especifica o nome do DataSet a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c5c56-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="c5c56-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c56-133">-ResourceGroupName</span></span>
<span data-ttu-id="c5c56-134">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c56-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c5c56-135">Esse cmdlet cria um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="c5c56-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c5c56-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c56-136">-ResourceId</span></span>
<span data-ttu-id="c5c56-137">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c56-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c5c56-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5c56-138">-Confirm</span></span>
<span data-ttu-id="c5c56-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5c56-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5c56-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5c56-140">-WhatIf</span></span>
<span data-ttu-id="c5c56-141">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5c56-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c5c56-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c56-142">CommonParameters</span></span>
<span data-ttu-id="c5c56-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c56-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c56-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c56-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c56-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5c56-145">INPUTS</span></span>

### <span data-ttu-id="c5c56-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c5c56-146">System.String</span></span>

## <span data-ttu-id="c5c56-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5c56-147">OUTPUTS</span></span>

### <span data-ttu-id="c5c56-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c5c56-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="c5c56-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5c56-149">NOTES</span></span>
<span data-ttu-id="c5c56-150">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c5c56-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c5c56-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5c56-151">RELATED LINKS</span></span>

[<span data-ttu-id="c5c56-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5c56-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="c5c56-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="c5c56-153">Remove-AzDataFactoryV2Dataset</span></span>]()
