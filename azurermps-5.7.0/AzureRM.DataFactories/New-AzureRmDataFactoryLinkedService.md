---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: c89a7950b70bf3b3b13b053e4e007434afdb078d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430510"
---
# <span data-ttu-id="dc94c-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dc94c-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="dc94c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc94c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc94c-103">Vincula um repositório de dados ou um serviço na nuvem a uma fábrica de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc94c-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc94c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc94c-104">SYNTAX</span></span>

### <span data-ttu-id="dc94c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc94c-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc94c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="dc94c-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc94c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc94c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc94c-108">O cmdlet **New-AzureRmDataFactoryLinkedService** vincula um repositório de dados ou um serviço na nuvem ao Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="dc94c-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="dc94c-109">Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="dc94c-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="dc94c-110">Se você especificar o parâmetro *Force* , o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="dc94c-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="dc94c-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="dc94c-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="dc94c-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="dc94c-112">Create a data factory.</span></span> 
- <span data-ttu-id="dc94c-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="dc94c-113">Create linked services.</span></span> 
- <span data-ttu-id="dc94c-114">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="dc94c-114">Create datasets.</span></span> 
- <span data-ttu-id="dc94c-115">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc94c-115">Create a pipeline.</span></span>

## <span data-ttu-id="dc94c-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc94c-116">EXAMPLES</span></span>

### <span data-ttu-id="dc94c-117">Exemplo 1: criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="dc94c-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="dc94c-118">Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dc94c-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="dc94c-119">Esse serviço vinculado vincula um repositório de blob do Azure especificado no arquivo ao data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="dc94c-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="dc94c-120">O comando passa o resultado para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="dc94c-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dc94c-121">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="dc94c-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="dc94c-122">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="dc94c-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="dc94c-123">OS</span><span class="sxs-lookup"><span data-stu-id="dc94c-123">PARAMETERS</span></span>

### <span data-ttu-id="dc94c-124">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="dc94c-124">-DataFactory</span></span>
<span data-ttu-id="dc94c-125">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="dc94c-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="dc94c-126">Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dc94c-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc94c-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dc94c-127">-DataFactoryName</span></span>
<span data-ttu-id="dc94c-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="dc94c-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="dc94c-129">Esse cmdlet cria um serviço vinculado para a fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dc94c-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc94c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc94c-130">-DefaultProfile</span></span>
<span data-ttu-id="dc94c-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dc94c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc94c-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="dc94c-132">-File</span></span>
<span data-ttu-id="dc94c-133">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="dc94c-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc94c-134">-Force</span><span class="sxs-lookup"><span data-stu-id="dc94c-134">-Force</span></span>
<span data-ttu-id="dc94c-135">Indica que esse cmdlet substitui um serviço vinculado existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="dc94c-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="dc94c-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc94c-136">-Name</span></span>
<span data-ttu-id="dc94c-137">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="dc94c-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc94c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc94c-138">-ResourceGroupName</span></span>
<span data-ttu-id="dc94c-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="dc94c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="dc94c-140">Esse cmdlet cria um serviço vinculado para o grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="dc94c-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="dc94c-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc94c-141">-Confirm</span></span>
<span data-ttu-id="dc94c-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc94c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc94c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc94c-143">-WhatIf</span></span>
<span data-ttu-id="dc94c-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc94c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc94c-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc94c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc94c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc94c-146">CommonParameters</span></span>
<span data-ttu-id="dc94c-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc94c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc94c-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc94c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc94c-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc94c-149">INPUTS</span></span>

### <span data-ttu-id="dc94c-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dc94c-150">None</span></span>
<span data-ttu-id="dc94c-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="dc94c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc94c-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc94c-152">OUTPUTS</span></span>

### <span data-ttu-id="dc94c-153">Microsoft. WindowsAzure. Commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="dc94c-153">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="dc94c-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc94c-154">NOTES</span></span>
* <span data-ttu-id="dc94c-155">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="dc94c-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="dc94c-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc94c-156">RELATED LINKS</span></span>

[<span data-ttu-id="dc94c-157">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dc94c-157">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="dc94c-158">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="dc94c-158">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


