---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: d6fd12e96a98d0771a984aa5234013dbe4a548af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116257"
---
# <span data-ttu-id="e8429-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e8429-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="e8429-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8429-102">SYNOPSIS</span></span>
<span data-ttu-id="e8429-103">Vincula um armazenamento de dados ou um serviço de nuvem ao Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e8429-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="e8429-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8429-104">SYNTAX</span></span>

### <span data-ttu-id="e8429-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="e8429-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8429-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8429-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8429-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8429-107">DESCRIPTION</span></span>
<span data-ttu-id="e8429-108">O Set-AzDataFactoryV2LinkedService cmdlet vincula um armazenamento de dados ou um serviço de nuvem ao Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e8429-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="e8429-109">Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="e8429-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="e8429-110">Se você especificar o parâmetro Forçar, o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="e8429-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="e8429-111">Execute essas operações na seguinte ordem: - Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e8429-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e8429-112">- Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="e8429-112">-- Create linked services.</span></span>
<span data-ttu-id="e8429-113">-- Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="e8429-113">-- Create datasets.</span></span>
<span data-ttu-id="e8429-114">- Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8429-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="e8429-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e8429-115">EXAMPLES</span></span>

### <span data-ttu-id="e8429-116">Exemplo 1: Criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="e8429-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="e8429-117">Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e8429-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="e8429-118">Esse serviço vinculado vincula um armazenamento de blob do Azure especificado no arquivo à fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e8429-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="e8429-119">O comando passa o resultado para o Format-List cmdlet usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8429-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e8429-120">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="e8429-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e8429-121">Para obter mais informações, digite Get-Help Formatar Lista.</span><span class="sxs-lookup"><span data-stu-id="e8429-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="e8429-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8429-122">PARAMETERS</span></span>

### <span data-ttu-id="e8429-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e8429-123">-DataFactoryName</span></span>
<span data-ttu-id="e8429-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e8429-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e8429-125">Esse cmdlet cria um serviço vinculado para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e8429-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8429-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8429-126">-DefaultProfile</span></span>
<span data-ttu-id="e8429-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8429-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e8429-128">-DefinitionFile</span></span>
<span data-ttu-id="e8429-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="e8429-129">The JSON file path.</span></span>

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

### <span data-ttu-id="e8429-130">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e8429-130">-Force</span></span>
<span data-ttu-id="e8429-131">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="e8429-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e8429-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8429-132">-Name</span></span>
<span data-ttu-id="e8429-133">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="e8429-133">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8429-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8429-134">-ResourceGroupName</span></span>
<span data-ttu-id="e8429-135">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e8429-136">Esse cmdlet cria um serviço vinculado para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e8429-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8429-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8429-137">-ResourceId</span></span>
<span data-ttu-id="e8429-138">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e8429-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e8429-139">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e8429-139">-Confirm</span></span>
<span data-ttu-id="e8429-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8429-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8429-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8429-141">-WhatIf</span></span>
<span data-ttu-id="e8429-142">Mostra o que acontece se o cmdlet é executado, mas não executa o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8429-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e8429-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8429-143">CommonParameters</span></span>
<span data-ttu-id="e8429-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8429-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8429-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8429-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8429-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="e8429-146">INPUTS</span></span>

### <span data-ttu-id="e8429-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e8429-147">System.String</span></span>

## <span data-ttu-id="e8429-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="e8429-148">OUTPUTS</span></span>

### <span data-ttu-id="e8429-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="e8429-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="e8429-150">Notas</span><span class="sxs-lookup"><span data-stu-id="e8429-150">NOTES</span></span>
<span data-ttu-id="e8429-151">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="e8429-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8429-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8429-152">RELATED LINKS</span></span>

[<span data-ttu-id="e8429-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e8429-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="e8429-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e8429-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
