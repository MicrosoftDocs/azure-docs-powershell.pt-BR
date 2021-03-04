---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 5b11273e61689c515cc7ed72f013514fcd309dcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887792"
---
# <span data-ttu-id="443f4-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="443f4-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="443f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="443f4-102">SYNOPSIS</span></span>
<span data-ttu-id="443f4-103">Vincula um armazenamento de dados ou um serviço de nuvem a uma Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="443f4-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="443f4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="443f4-104">SYNTAX</span></span>

### <span data-ttu-id="443f4-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="443f4-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="443f4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="443f4-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="443f4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="443f4-107">DESCRIPTION</span></span>
<span data-ttu-id="443f4-108">O cmdlet **New-AzDataFactoryLinkedService** vincula um armazenamento de dados ou um serviço de nuvem à Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="443f4-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="443f4-109">Se você especificar um nome para um serviço vinculado que já existe, este cmdlet solicitará a confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="443f4-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="443f4-110">Se você especificar o *parâmetro Force,* o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="443f4-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="443f4-111">Execute essas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="443f4-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="443f4-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="443f4-112">Create a data factory.</span></span> 
- <span data-ttu-id="443f4-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="443f4-113">Create linked services.</span></span> 
- <span data-ttu-id="443f4-114">Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="443f4-114">Create datasets.</span></span> 
- <span data-ttu-id="443f4-115">Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="443f4-115">Create a pipeline.</span></span>

## <span data-ttu-id="443f4-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="443f4-116">EXAMPLES</span></span>

### <span data-ttu-id="443f4-117">Exemplo 1: Criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="443f4-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="443f4-118">Este comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="443f4-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="443f4-119">Esse serviço vinculado vincula um armazenamento de blob do Azure especificado no arquivo para o fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="443f4-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="443f4-120">O comando passa o resultado para o cmdlet Format-List usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="443f4-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="443f4-121">Esse Windows PowerShell cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="443f4-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="443f4-122">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="443f4-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="443f4-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="443f4-123">PARAMETERS</span></span>

### <span data-ttu-id="443f4-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="443f4-124">-DataFactory</span></span>
<span data-ttu-id="443f4-125">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="443f4-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="443f4-126">Este cmdlet cria um serviço vinculado para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="443f4-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="443f4-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="443f4-127">-DataFactoryName</span></span>
<span data-ttu-id="443f4-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="443f4-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="443f4-129">Este cmdlet cria um serviço vinculado para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="443f4-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="443f4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443f4-130">-DefaultProfile</span></span>
<span data-ttu-id="443f4-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="443f4-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="443f4-132">-File</span><span class="sxs-lookup"><span data-stu-id="443f4-132">-File</span></span>
<span data-ttu-id="443f4-133">Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="443f4-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="443f4-134">-Force</span><span class="sxs-lookup"><span data-stu-id="443f4-134">-Force</span></span>
<span data-ttu-id="443f4-135">Indica que esse cmdlet substitui um serviço vinculado existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="443f4-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="443f4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="443f4-136">-Name</span></span>
<span data-ttu-id="443f4-137">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="443f4-137">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443f4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443f4-138">-ResourceGroupName</span></span>
<span data-ttu-id="443f4-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="443f4-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="443f4-140">Este cmdlet cria um serviço vinculado para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="443f4-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="443f4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="443f4-141">-Confirm</span></span>
<span data-ttu-id="443f4-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="443f4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="443f4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="443f4-143">-WhatIf</span></span>
<span data-ttu-id="443f4-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="443f4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="443f4-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="443f4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="443f4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443f4-146">CommonParameters</span></span>
<span data-ttu-id="443f4-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="443f4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443f4-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="443f4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443f4-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="443f4-149">INPUTS</span></span>

### <span data-ttu-id="443f4-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="443f4-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="443f4-151">System.String</span><span class="sxs-lookup"><span data-stu-id="443f4-151">System.String</span></span>

## <span data-ttu-id="443f4-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="443f4-152">OUTPUTS</span></span>

### <span data-ttu-id="443f4-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="443f4-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="443f4-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="443f4-154">NOTES</span></span>
* <span data-ttu-id="443f4-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="443f4-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="443f4-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="443f4-156">RELATED LINKS</span></span>

[<span data-ttu-id="443f4-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="443f4-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="443f4-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="443f4-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


