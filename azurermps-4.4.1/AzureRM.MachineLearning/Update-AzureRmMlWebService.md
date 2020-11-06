---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlWebService.md
ms.openlocfilehash: 75f94e5c93f81fa88dd33c3c0b94cb2b36ca291f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432197"
---
# <span data-ttu-id="f1b72-101">Update-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f1b72-101">Update-AzureRmMlWebService</span></span>

## <span data-ttu-id="f1b72-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1b72-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b72-103">Atualiza as propriedades de um recurso de serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="f1b72-103">Updates properties of an existing web service resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1b72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1b72-104">SYNTAX</span></span>

### <span data-ttu-id="f1b72-105">Atualize propriedades específicas do.</span><span class="sxs-lookup"><span data-stu-id="f1b72-105">Update specific properties of the .</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1b72-106">Crie um novo Azure ML WebService a partir de uma definição de instância WebService.</span><span class="sxs-lookup"><span data-stu-id="f1b72-106">Create a new Azure ML webservice from a WebService instance definition.</span></span>
```
Update-AzureRmMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1b72-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1b72-107">DESCRIPTION</span></span>
<span data-ttu-id="f1b72-108">O cmdlet Update-AzureRmMlWebService permite que você atualize as propriedades não estáticas de um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-108">The Update-AzureRmMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="f1b72-109">O cmdlet funciona como uma operação de correção.</span><span class="sxs-lookup"><span data-stu-id="f1b72-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="f1b72-110">Passe apenas as propriedades que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="f1b72-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="f1b72-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1b72-111">EXAMPLES</span></span>

### <span data-ttu-id="f1b72-112">--------------------------Exemplo 1: argumentos de atualização seletiva--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1b72-112">--------------------------  Example 1: Selective update arguments  --------------------------</span></span>
<span data-ttu-id="f1b72-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="f1b72-113">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="f1b72-114">Aqui, alteramos a descrição, a chave de acesso primária e habilitamos a coleta de diagnósticos para todos os rastreamentos durante o tempo de execução para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-114">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="f1b72-115">--------------------------Exemplo 2: atualizar com base em uma instância de serviço Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1b72-115">--------------------------  Example 2: Update based on a web service instance  --------------------------</span></span>
<span data-ttu-id="f1b72-116">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="f1b72-116">@{paragraph=PS C:\\\>}</span></span>





```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="f1b72-117">Primeiro, o exemplo cria uma definição de serviço Web, que contém somente os campos a serem atualizados e, em seguida, chama o Update-AzureRmMlWebService para aplicá-los usando o parâmetro service updates.</span><span class="sxs-lookup"><span data-stu-id="f1b72-117">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzureRmMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="f1b72-118">OS</span><span class="sxs-lookup"><span data-stu-id="f1b72-118">PARAMETERS</span></span>

### <span data-ttu-id="f1b72-119">-Ativos</span><span class="sxs-lookup"><span data-stu-id="f1b72-119">-Assets</span></span>
<span data-ttu-id="f1b72-120">O conjunto de ativos (por exemplo, módulos, conjuntos de valores) que compõem o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-120">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f1b72-121">-Description</span></span>
<span data-ttu-id="f1b72-122">O novo valor para a descrição do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-122">The new value for the web service's description.</span></span>
<span data-ttu-id="f1b72-123">Isso é visível no esquema de API do Swagger do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1b72-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-124">-Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="f1b72-124">-Diagnostics</span></span>
<span data-ttu-id="f1b72-125">As configurações que controlam a coleção de rastreamentos de diagnóstico para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f1b72-126">-Force</span></span>
<span data-ttu-id="f1b72-127">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f1b72-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f1b72-128">-Entrada</span><span class="sxs-lookup"><span data-stu-id="f1b72-128">-Input</span></span>
<span data-ttu-id="f1b72-129">A definição da (s) entrada (s) do serviço Web, fornecida como uma construção de esquema Swagger.</span><span class="sxs-lookup"><span data-stu-id="f1b72-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="f1b72-130">-IsReadOnly</span></span>
<span data-ttu-id="f1b72-131">Especifica que este serviço Web é muito ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="f1b72-131">Specifies that this web serviceis readonly.</span></span>
<span data-ttu-id="f1b72-132">Uma vez definido, o serviço Web pode ser mais atualizado, incluindo a alteração do valor dessa propriedade e só pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f1b72-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-133">-Teclas</span><span class="sxs-lookup"><span data-stu-id="f1b72-133">-Keys</span></span>
<span data-ttu-id="f1b72-134">Atualiza uma ou ambas as teclas de acesso usadas para autenticar chamadas para as APIs de tempo de execução do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1b72-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1b72-135">-Name</span></span>
<span data-ttu-id="f1b72-136">O nome do recurso de serviço Web a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f1b72-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="f1b72-137">-Saída</span><span class="sxs-lookup"><span data-stu-id="f1b72-137">-Output</span></span>
<span data-ttu-id="f1b72-138">A definição da (s) saída (s) do serviço Web, fornecida como uma construção de esquema Swagger.</span><span class="sxs-lookup"><span data-stu-id="f1b72-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-139">-Package</span><span class="sxs-lookup"><span data-stu-id="f1b72-139">-Package</span></span>
<span data-ttu-id="f1b72-140">A definição do pacote de gráficos que define esse serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-141">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1b72-141">-Parameters</span></span>
<span data-ttu-id="f1b72-142">O conjunto de valores de parâmetros globais definidos para o serviço Web, dado como um nome de parâmetro global- \> conjunto de valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f1b72-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="f1b72-143">Se nenhum valor padrão for especificado, o parâmetro será considerado obrigatório.</span><span class="sxs-lookup"><span data-stu-id="f1b72-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1b72-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="f1b72-145">Atualizações para a configuração do ponto de extremidade em tempo real do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1b72-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1b72-146">-ResourceGroupName</span></span>
<span data-ttu-id="f1b72-147">O grupo de recursos que contém o serviço Web a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f1b72-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="f1b72-148">-Atualizações</span><span class="sxs-lookup"><span data-stu-id="f1b72-148">-ServiceUpdates</span></span>
<span data-ttu-id="f1b72-149">Um conjunto de atualizações a ser aplicado ao serviço Web fornecido como uma instância de definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="f1b72-150">Somente campos não estáticos são modificados.</span><span class="sxs-lookup"><span data-stu-id="f1b72-150">Only non-static fields are modified.</span></span>

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

### <span data-ttu-id="f1b72-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f1b72-151">-StorageAccountKey</span></span>
<span data-ttu-id="f1b72-152">Gira a tecla de acesso da conta de armazenamento associada ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-153">-Título</span><span class="sxs-lookup"><span data-stu-id="f1b72-153">-Title</span></span>
<span data-ttu-id="f1b72-154">O novo valor para o título do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="f1b72-154">The new value for the web service's title.</span></span>
<span data-ttu-id="f1b72-155">Isso é visível no esquema de API do Swagger do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1b72-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: Update specific properties of the .
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1b72-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1b72-156">-Confirm</span></span>
<span data-ttu-id="f1b72-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1b72-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1b72-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1b72-158">-WhatIf</span></span>
<span data-ttu-id="f1b72-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1b72-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1b72-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1b72-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1b72-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b72-161">-DefaultProfile</span></span>
<span data-ttu-id="f1b72-162">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b72-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b72-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b72-163">CommonParameters</span></span>
<span data-ttu-id="f1b72-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1b72-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b72-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1b72-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b72-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1b72-166">INPUTS</span></span>

### <span data-ttu-id="f1b72-167">Serviço</span><span class="sxs-lookup"><span data-stu-id="f1b72-167">WebService</span></span>
<span data-ttu-id="f1b72-168">O parâmetro ' unupdates ' aceita o valor do tipo ' WebService ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f1b72-168">Parameter 'ServiceUpdates' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="f1b72-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1b72-169">OUTPUTS</span></span>

### <span data-ttu-id="f1b72-170">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="f1b72-170">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="f1b72-171">Uma descrição resumida do serviço Web do Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="f1b72-171">A summary description of the Azure Machine Learning web service.</span></span>
<span data-ttu-id="f1b72-172">Semelhante à descrição retornada chamando o cmdlet Get-AzureRmMlWebService em um serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="f1b72-172">Similar to the description returned by calling the Get-AzureRmMlWebService cmdlet on an existing web service.</span></span>
<span data-ttu-id="f1b72-173">Essa descrição não contém propriedades confidenciais, como as credenciais da conta de armazenamento e as teclas de acesso do serviço.</span><span class="sxs-lookup"><span data-stu-id="f1b72-173">This description does not contain sensitive properties such as storage account's credentials and the service's access keys.</span></span>

## <span data-ttu-id="f1b72-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1b72-174">NOTES</span></span>
<span data-ttu-id="f1b72-175">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f1b72-175">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f1b72-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1b72-176">RELATED LINKS</span></span>

