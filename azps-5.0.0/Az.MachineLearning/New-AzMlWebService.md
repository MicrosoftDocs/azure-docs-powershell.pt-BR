---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlWebService.md
ms.openlocfilehash: 5988aed4ca0560daedc1470198e0b02975f18196
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124871"
---
# <span data-ttu-id="9614c-101">New-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="9614c-101">New-AzMlWebService</span></span>

## <span data-ttu-id="9614c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9614c-102">SYNOPSIS</span></span>
<span data-ttu-id="9614c-103">Cria um novo serviço Web.</span><span class="sxs-lookup"><span data-stu-id="9614c-103">Creates a new web service.</span></span>

## <span data-ttu-id="9614c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9614c-104">SYNTAX</span></span>

### <span data-ttu-id="9614c-105">CreateFromFile</span><span class="sxs-lookup"><span data-stu-id="9614c-105">CreateFromFile</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String> -DefinitionFile <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9614c-106">CreateFromInstance</span><span class="sxs-lookup"><span data-stu-id="9614c-106">CreateFromInstance</span></span>
```
New-AzMlWebService -ResourceGroupName <String> -Location <String> -Name <String>
 -NewWebServiceDefinition <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9614c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9614c-107">DESCRIPTION</span></span>
<span data-ttu-id="9614c-108">Cria um serviço Web do Azure Machine Learning em um grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="9614c-108">Creates an Azure Machine Learning web service in an existing resource group.</span></span>
<span data-ttu-id="9614c-109">Se um serviço Web com o mesmo nome existir no grupo de recursos, a chamada funcionará como uma operação de atualização e o serviço Web existente será substituído.</span><span class="sxs-lookup"><span data-stu-id="9614c-109">If a web service with the same name exists in the resource group, the call acts as an update operation and the existing web service is overwritten.</span></span>

## <span data-ttu-id="9614c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9614c-110">EXAMPLES</span></span>

### <span data-ttu-id="9614c-111">Exemplo 1: criar um novo serviço a partir de uma definição baseada em arquivos JSON</span><span class="sxs-lookup"><span data-stu-id="9614c-111">Example 1: Create a new service from a Json file based definition</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -DefinitionFile "C:\mlservice.json"
```

<span data-ttu-id="9614c-112">Cria um novo serviço Web do Azure Machine Learning chamado "mywebservicename" no grupo "MyResource Group" e a região do centro sul central do Sul, com base na definição presente no arquivo JSON referenciado.</span><span class="sxs-lookup"><span data-stu-id="9614c-112">Creates a new Azure Machine Learning web service named "mywebservicename" in the "myresourcegroup" group and South Central US region, based on the definition present in the referenced json file.</span></span>

### <span data-ttu-id="9614c-113">Exemplo 2: criar um novo serviço a partir de uma instância do objeto</span><span class="sxs-lookup"><span data-stu-id="9614c-113">Example 2: Create a new service from an object instance</span></span>
```
New-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Location "South Central US" -NewWebServiceDefinition $serviceDefinitionObject
```

<span data-ttu-id="9614c-114">Você pode obter uma instância de objeto de serviço Web para personalizar a publicação como um recurso usando o cmdlet Import-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="9614c-114">You can obtain a web service object instance to customize before publishing as a resource by using the Import-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="9614c-115">OS</span><span class="sxs-lookup"><span data-stu-id="9614c-115">PARAMETERS</span></span>

### <span data-ttu-id="9614c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9614c-116">-DefaultProfile</span></span>
<span data-ttu-id="9614c-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9614c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9614c-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="9614c-118">-DefinitionFile</span></span>
<span data-ttu-id="9614c-119">Especifica o caminho para o arquivo que contém a definição de formato JSON do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="9614c-119">Specifies the path to the file containing the JSON format definition of the web service.</span></span>
<span data-ttu-id="9614c-120">Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning .</span><span class="sxs-lookup"><span data-stu-id="9614c-120">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/tree/master/arm-machinelearning.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9614c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9614c-121">-Force</span></span>
<span data-ttu-id="9614c-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="9614c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9614c-123">-Local</span><span class="sxs-lookup"><span data-stu-id="9614c-123">-Location</span></span>
<span data-ttu-id="9614c-124">A região do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="9614c-124">The region of the web service.</span></span>
<span data-ttu-id="9614c-125">Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".</span><span class="sxs-lookup"><span data-stu-id="9614c-125">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="9614c-126">Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="9614c-126">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="9614c-127">O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9614c-127">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="9614c-128">Os grupos de recursos podem conter serviços Web de regiões diferentes.</span><span class="sxs-lookup"><span data-stu-id="9614c-128">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="9614c-129">Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzResourceProvider com o cmdlet de parâmetro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="9614c-129">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="9614c-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9614c-130">-Name</span></span>
<span data-ttu-id="9614c-131">O nome do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="9614c-131">The name for the web service.</span></span>
<span data-ttu-id="9614c-132">O nome deve ser exclusivo no grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9614c-132">The name must be unique in the resource group.</span></span>

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

### <span data-ttu-id="9614c-133">-NewWebServiceDefinition</span><span class="sxs-lookup"><span data-stu-id="9614c-133">-NewWebServiceDefinition</span></span>
<span data-ttu-id="9614c-134">A definição do novo serviço Web, contendo todas as propriedades que compõem o serviço.</span><span class="sxs-lookup"><span data-stu-id="9614c-134">The definition for the new web service, containing all the properties that make up the service.</span></span>
<span data-ttu-id="9614c-135">Esse parâmetro é obrigatório e representa uma instância da classe Microsoft. Azure. Management. MachineLearning. WebServices. WebService.</span><span class="sxs-lookup"><span data-stu-id="9614c-135">This parameter is required and represents an instance of the Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService class.</span></span>
<span data-ttu-id="9614c-136">Você pode encontrar a especificação mais recente para a definição do serviço Web na especificação do Swagger em https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json .</span><span class="sxs-lookup"><span data-stu-id="9614c-136">You can find the latest specification for the web service definition in the swagger spec under https://github.com/Azure/azure-rest-api-specs/blob/master/arm-machinelearning/2017-01-01/swagger/webservices.json.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: CreateFromInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9614c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9614c-137">-ResourceGroupName</span></span>
<span data-ttu-id="9614c-138">O grupo de recursos no qual colocar o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="9614c-138">The resource group in which to place the web service.</span></span>
<span data-ttu-id="9614c-139">Insira uma região do Azure Data Center, como "Oeste EUA" ou "sudeste asiático".</span><span class="sxs-lookup"><span data-stu-id="9614c-139">Enter an Azure data center region, such as "West US" or "Southeast Asia".</span></span>
<span data-ttu-id="9614c-140">Você pode colocar um serviço Web em qualquer região que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="9614c-140">You can place a web service in any region that supports resources of that type.</span></span>
<span data-ttu-id="9614c-141">O serviço Web não precisa estar na mesma região da assinatura do Azure ou da mesma região do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9614c-141">The web service does not have to be in the same region your Azure subscription or the same region as its resource group.</span></span>
<span data-ttu-id="9614c-142">Os grupos de recursos podem conter serviços Web de regiões diferentes.</span><span class="sxs-lookup"><span data-stu-id="9614c-142">Resource groups can contain web services from different regions.</span></span>
<span data-ttu-id="9614c-143">Para determinar quais regiões dão suporte a cada tipo de recurso, use o Get-AzResourceProvider com o cmdlet de parâmetro ProviderNamespace.</span><span class="sxs-lookup"><span data-stu-id="9614c-143">To determine which regions support each resource type, use the Get-AzResourceProvider with the ProviderNamespace parameter cmdlet.</span></span>

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

### <span data-ttu-id="9614c-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9614c-144">-Confirm</span></span>
<span data-ttu-id="9614c-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9614c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9614c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9614c-146">-WhatIf</span></span>
<span data-ttu-id="9614c-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9614c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9614c-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9614c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9614c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9614c-149">CommonParameters</span></span>
<span data-ttu-id="9614c-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9614c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9614c-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9614c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9614c-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9614c-152">INPUTS</span></span>

### <span data-ttu-id="9614c-153">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="9614c-153">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9614c-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9614c-154">OUTPUTS</span></span>

### <span data-ttu-id="9614c-155">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="9614c-155">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="9614c-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9614c-156">NOTES</span></span>
<span data-ttu-id="9614c-157">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="9614c-157">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="9614c-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9614c-158">RELATED LINKS</span></span>
