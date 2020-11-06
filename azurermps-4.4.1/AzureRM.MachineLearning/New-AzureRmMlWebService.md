---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlWebService.md
ms.openlocfilehash: 1fe6476836622445337ea0b4741b361504a57302
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441027"
---
# <span data-ttu-id="ccdbd-101">New-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="ccdbd-101">New-AzureRmMlWebService</span></span>

## <span data-ttu-id="ccdbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdbd-103">Cria um novo serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-103">Creates a new web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccdbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccdbd-104">SYNTAX</span></span>

### <span data-ttu-id="ccdbd-105">Crie um novo Azure ML WebService a partir de um arquivo JSON definiton.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-105">Create a new Azure ML webservice from a JSON definiton file.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccdbd-106">Crie um novo Azure ML WebService a partir de uma definição de instância WebService.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
New-AzureRmMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccdbd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccdbd-107">DESCRIPTION</span></span>
<span data-ttu-id="ccdbd-108">Cria um serviço Web do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="ccdbd-109">Se um serviço Web com o mesmo nome existir no grupo de recursos, a chamada funcionará como uma operação de atualização e o serviço Web existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="ccdbd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccdbd-110">EXAMPLES</span></span>

### <span data-ttu-id="ccdbd-111">--------------------------Exemplo 1: criar um novo serviço a partir de uma definição baseada em arquivos JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccdbd-111">--------------------------  Example 1: Create a new service from a Json file based definition  --------------------------</span></span>
<span data-ttu-id="ccdbd-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ccdbd-112">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="ccdbd-113">Cria um novo serviço Web do Azure Machine Learning chamado "mywebservicename" no grupo "MyResource Group" e a região do centro sul central do Sul, com base na definição presente no arquivo JSON referenciado.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-113">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="ccdbd-114">--------------------------Exemplo 2: criar um novo serviço a partir de uma instância de objeto--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccdbd-114">--------------------------  Example 2: Create a new service from an object instance  --------------------------</span></span>
<span data-ttu-id="ccdbd-115">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ccdbd-115">@{paragraph=PS C:\\\>}</span></span>





```
New-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="ccdbd-116">Você pode obter uma instância de objeto de serviço Web para personalizar a publicação como um recurso usando o cmdlet Import-AzureRmMlWebService.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-116">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="ccdbd-117">OS</span><span class="sxs-lookup"><span data-stu-id="ccdbd-117">PARAMETERS</span></span>

### <span data-ttu-id="ccdbd-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ccdbd-118">-DefinitionFile</span></span>
<span data-ttu-id="ccdbd-119">Especifica o caminho para o arquivo que contém a definição de formato JSON do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-119">Specifes the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="ccdbd-120">Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="ccdbd-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: Create a new Azure ML webservice from a JSON definiton file.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdbd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ccdbd-121">-Force</span></span>
<span data-ttu-id="ccdbd-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ccdbd-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ccdbd-123">-Location</span></span>
<span data-ttu-id="ccdbd-124">A região do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-124">The region of the web service.</span></span>
<span data-ttu-id="ccdbd-125">Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".</span><span class="sxs-lookup"><span data-stu-id="ccdbd-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="ccdbd-126">Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="ccdbd-127">O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="ccdbd-128">Os grupos de recursos podem conter serviços Web de regiões diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="ccdbd-129">Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzureRmResourceProvider com o cmdlet de parâmetro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-129">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdbd-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccdbd-130">-Name</span></span>
<span data-ttu-id="ccdbd-131">O nome do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-131">The name for the web service.</span></span>
<span data-ttu-id="ccdbd-132">O nome deve ser exclusivo no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-132">The name must be unique in the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdbd-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="ccdbd-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="ccdbd-134">A definição do novo serviço Web, contendo todas as propriedades que compõem o serviço.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="ccdbd-135">Esse parâmetro é obrigatório e representa uma instância da classe Microsoft. Azure. Management. MachineLearning. WebServices. WebService.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="ccdbd-136">Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="ccdbd-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Create a new Azure ML webservice from a WebService instance definition.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdbd-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdbd-137">-ResourceGroupName</span></span>
<span data-ttu-id="ccdbd-138">O grupo de recursos no qual colocar o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="ccdbd-139">Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".</span><span class="sxs-lookup"><span data-stu-id="ccdbd-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="ccdbd-140">Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="ccdbd-141">O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="ccdbd-142">Os grupos de recursos podem conter serviços Web de regiões diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="ccdbd-143">Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzureRmResourceProvider com o cmdlet de parâmetro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-143">To determine which regions support each resource type, use the Get-AzureRmResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdbd-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ccdbd-144">-Confirm</span></span>
<span data-ttu-id="ccdbd-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdbd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdbd-146">-WhatIf</span></span>
<span data-ttu-id="ccdbd-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdbd-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdbd-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdbd-149">-DefaultProfile</span></span>
<span data-ttu-id="ccdbd-150">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccdbd-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdbd-151">CommonParameters</span></span>
<span data-ttu-id="ccdbd-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdbd-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdbd-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdbd-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccdbd-154">INPUTS</span></span>

### <span data-ttu-id="ccdbd-155">Serviço</span><span class="sxs-lookup"><span data-stu-id="ccdbd-155">WebService</span></span>
<span data-ttu-id="ccdbd-156">O parâmetro ' NewWebServiceDefinition ' aceita o valor do tipo ' WebService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ccdbd-156">Parameter 'NewWebServiceDefinition' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="ccdbd-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccdbd-157">OUTPUTS</span></span>

### <span data-ttu-id="ccdbd-158">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ccdbd-158">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="ccdbd-159">Uma descrição resumida do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-159">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="ccdbd-160">Semelhante à descrição retornada chamando o cmdlet Get-AzureRmMlWebService em um serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-160">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="ccdbd-161">Essa descrição não contém propriedades confidenciais, como as credenciais da conta de armazenamento e as teclas de acesso do serviço.</span><span class="sxs-lookup"><span data-stu-id="ccdbd-161">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="ccdbd-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccdbd-162">NOTES</span></span>
<span data-ttu-id="ccdbd-163">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ccdbd-163">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ccdbd-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccdbd-164">RELATED LINKS</span></span>

