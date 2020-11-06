---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 47cbd81fa7e2e8f3877c2e933254cde4e2cee8ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426379"
---
# <span data-ttu-id="0535b-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0535b-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0535b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0535b-102">SYNOPSIS</span></span>
<span data-ttu-id="0535b-103">Vincula um repositório de dados ou um serviço na nuvem ao data Factory.</span><span class="sxs-lookup"><span data-stu-id="0535b-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0535b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0535b-104">SYNTAX</span></span>

### <span data-ttu-id="0535b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0535b-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0535b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0535b-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0535b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0535b-107">DESCRIPTION</span></span>
<span data-ttu-id="0535b-108">O cmdlet Set-AzureRmDataFactoryV2LinkedService vincula um repositório de dados ou um serviço na nuvem ao Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="0535b-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="0535b-109">Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="0535b-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="0535b-110">Se você especificar o parâmetro Force, o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="0535b-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="0535b-111">Execute estas operações na seguinte ordem:--Crie uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0535b-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="0535b-112">--Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="0535b-112">-- Create linked services.</span></span>
<span data-ttu-id="0535b-113">--Criar conjuntos de valores.</span><span class="sxs-lookup"><span data-stu-id="0535b-113">-- Create datasets.</span></span>
<span data-ttu-id="0535b-114">--Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="0535b-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="0535b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0535b-115">EXAMPLES</span></span>

### <span data-ttu-id="0535b-116">Exemplo 1: criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="0535b-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0535b-117">Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0535b-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="0535b-118">Esse serviço vinculado vincula um repositório de blob do Azure especificado no arquivo ao data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0535b-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="0535b-119">O comando passa o resultado para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0535b-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0535b-120">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="0535b-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0535b-121">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="0535b-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="0535b-122">OS</span><span class="sxs-lookup"><span data-stu-id="0535b-122">PARAMETERS</span></span>

### <span data-ttu-id="0535b-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0535b-123">-DataFactoryName</span></span>
<span data-ttu-id="0535b-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0535b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0535b-125">Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0535b-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0535b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0535b-126">-DefaultProfile</span></span>
<span data-ttu-id="0535b-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0535b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0535b-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0535b-128">-DefinitionFile</span></span>
<span data-ttu-id="0535b-129">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="0535b-129">The JSON file path.</span></span>

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

### <span data-ttu-id="0535b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0535b-130">-Force</span></span>
<span data-ttu-id="0535b-131">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="0535b-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0535b-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="0535b-132">-Name</span></span>
<span data-ttu-id="0535b-133">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0535b-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="0535b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0535b-134">-ResourceGroupName</span></span>
<span data-ttu-id="0535b-135">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0535b-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0535b-136">Esse cmdlet cria um serviço vinculado para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0535b-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0535b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0535b-137">-ResourceId</span></span>
<span data-ttu-id="0535b-138">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="0535b-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0535b-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0535b-139">-Confirm</span></span>
<span data-ttu-id="0535b-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0535b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0535b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0535b-141">-WhatIf</span></span>
<span data-ttu-id="0535b-142">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0535b-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0535b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0535b-143">CommonParameters</span></span>
<span data-ttu-id="0535b-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0535b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0535b-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0535b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0535b-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0535b-146">INPUTS</span></span>

### <span data-ttu-id="0535b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0535b-147">System.String</span></span>

## <span data-ttu-id="0535b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0535b-148">OUTPUTS</span></span>

### <span data-ttu-id="0535b-149">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0535b-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="0535b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0535b-150">NOTES</span></span>
<span data-ttu-id="0535b-151">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="0535b-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0535b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0535b-152">RELATED LINKS</span></span>

[<span data-ttu-id="0535b-153">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0535b-153">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0535b-154">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0535b-154">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
