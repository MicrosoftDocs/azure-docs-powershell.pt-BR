---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113868"
---
# <span data-ttu-id="aec66-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="aec66-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="aec66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aec66-102">SYNOPSIS</span></span>
<span data-ttu-id="aec66-103">Vincula um armazenamento de dados ou um serviço de nuvem a uma Fábrica de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="aec66-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="aec66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aec66-104">SYNTAX</span></span>

### <span data-ttu-id="aec66-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="aec66-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aec66-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aec66-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aec66-107">DESCRIPTION</span></span>
<span data-ttu-id="aec66-108">O **cmdlet New-AzDataFactoryLinkedService** vincula um armazenamento de dados ou um serviço de nuvem ao Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="aec66-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="aec66-109">Se você especificar um nome para um serviço vinculado que já existe, esse cmdlet solicitará confirmação antes de substituir o serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="aec66-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="aec66-110">Se você especificar o *parâmetro Forçar,* o cmdlet substituirá o serviço vinculado existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="aec66-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="aec66-111">Execute essas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="aec66-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="aec66-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="aec66-112">Create a data factory.</span></span> 
- <span data-ttu-id="aec66-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="aec66-113">Create linked services.</span></span> 
- <span data-ttu-id="aec66-114">Criar conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="aec66-114">Create datasets.</span></span> 
- <span data-ttu-id="aec66-115">Criar um pipeline.</span><span class="sxs-lookup"><span data-stu-id="aec66-115">Create a pipeline.</span></span>

## <span data-ttu-id="aec66-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="aec66-116">EXAMPLES</span></span>

### <span data-ttu-id="aec66-117">Exemplo 1: Criar um serviço vinculado</span><span class="sxs-lookup"><span data-stu-id="aec66-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="aec66-118">Esse comando cria um serviço vinculado chamado LinkedServiceCuratedWikiData no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="aec66-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="aec66-119">Esse serviço vinculado vincula um armazenamento de blob do Azure especificado no arquivo à fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="aec66-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="aec66-120">O comando passa o resultado para o Format-List cmdlet usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="aec66-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aec66-121">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="aec66-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="aec66-122">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="aec66-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="aec66-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aec66-123">PARAMETERS</span></span>

### <span data-ttu-id="aec66-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="aec66-124">-DataFactory</span></span>
<span data-ttu-id="aec66-125">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="aec66-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="aec66-126">Esse cmdlet cria um serviço vinculado para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aec66-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aec66-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aec66-127">-DataFactoryName</span></span>
<span data-ttu-id="aec66-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="aec66-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aec66-129">Esse cmdlet cria um serviço vinculado para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aec66-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aec66-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec66-130">-DefaultProfile</span></span>
<span data-ttu-id="aec66-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aec66-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aec66-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="aec66-132">-File</span></span>
<span data-ttu-id="aec66-133">Especifica o caminho completo do arquivo JSON (Notação de Objeto JavaScript) que contém a descrição do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="aec66-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="aec66-134">-Forçar</span><span class="sxs-lookup"><span data-stu-id="aec66-134">-Force</span></span>
<span data-ttu-id="aec66-135">Indica que esse cmdlet substitui um serviço vinculado existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="aec66-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="aec66-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="aec66-136">-Name</span></span>
<span data-ttu-id="aec66-137">Especifica o nome do serviço vinculado a ser criado.</span><span class="sxs-lookup"><span data-stu-id="aec66-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="aec66-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aec66-138">-ResourceGroupName</span></span>
<span data-ttu-id="aec66-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="aec66-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aec66-140">Esse cmdlet cria um serviço vinculado para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aec66-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aec66-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="aec66-141">-Confirm</span></span>
<span data-ttu-id="aec66-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec66-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec66-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec66-143">-WhatIf</span></span>
<span data-ttu-id="aec66-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="aec66-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec66-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aec66-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec66-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec66-146">CommonParameters</span></span>
<span data-ttu-id="aec66-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec66-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec66-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec66-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec66-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="aec66-149">INPUTS</span></span>

### <span data-ttu-id="aec66-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="aec66-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="aec66-151">System.String</span><span class="sxs-lookup"><span data-stu-id="aec66-151">System.String</span></span>

## <span data-ttu-id="aec66-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="aec66-152">OUTPUTS</span></span>

### <span data-ttu-id="aec66-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="aec66-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="aec66-154">Notas</span><span class="sxs-lookup"><span data-stu-id="aec66-154">NOTES</span></span>
* <span data-ttu-id="aec66-155">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="aec66-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aec66-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aec66-156">RELATED LINKS</span></span>

[<span data-ttu-id="aec66-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="aec66-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="aec66-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="aec66-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


