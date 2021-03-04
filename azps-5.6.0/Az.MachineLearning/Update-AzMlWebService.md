---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/update-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlWebService.md
ms.openlocfilehash: 510e33655fd2e76383fa89a972c477e65d67f070
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888484"
---
# <span data-ttu-id="4cd26-101">Update-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="4cd26-101">Update-AzMlWebService</span></span>

## <span data-ttu-id="4cd26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cd26-102">SYNOPSIS</span></span>
<span data-ttu-id="4cd26-103">Atualiza as propriedades de um recurso de serviço Web existente.</span><span class="sxs-lookup"><span data-stu-id="4cd26-103">Updates properties of an existing web service resource.</span></span>

## <span data-ttu-id="4cd26-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4cd26-104">SYNTAX</span></span>

### <span data-ttu-id="4cd26-105">UpdateFromParameters</span><span class="sxs-lookup"><span data-stu-id="4cd26-105">UpdateFromParameters</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> [-Title <String>] [-Description <String>]
 [-IsReadOnly] [-Keys <WebServiceKeys>] [-StorageAccountKey <String>] [-Diagnostics <DiagnosticsConfiguration>]
 [-RealtimeConfiguration <RealtimeConfiguration>] [-Assets <Hashtable>]
 [-Input <ServiceInputOutputSpecification>] [-Output <ServiceInputOutputSpecification>]
 [-Parameters <Hashtable>] [-Package <GraphPackage>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cd26-106">UpdateFromObject</span><span class="sxs-lookup"><span data-stu-id="4cd26-106">UpdateFromObject</span></span>
```
Update-AzMlWebService -ResourceGroupName <String> -Name <String> -ServiceUpdates <WebService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cd26-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4cd26-107">DESCRIPTION</span></span>
<span data-ttu-id="4cd26-108">O Update-AzMlWebService cmdlet permite que você atualize as propriedades não estáticas de um serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-108">The Update-AzMlWebService cmdlet allows you to update the non-static properties of a web service.</span></span>
<span data-ttu-id="4cd26-109">O cmdlet funciona como uma operação de patch.</span><span class="sxs-lookup"><span data-stu-id="4cd26-109">The cmdlet works as a patch operation.</span></span>
<span data-ttu-id="4cd26-110">Passe apenas as propriedades que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="4cd26-110">Pass only the properties that you want modified.</span></span>

## <span data-ttu-id="4cd26-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cd26-111">EXAMPLES</span></span>

### <span data-ttu-id="4cd26-112">Exemplo 1: argumentos de atualização seletiva</span><span class="sxs-lookup"><span data-stu-id="4cd26-112">Example 1: Selective update arguments</span></span>
```
Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Description "new update to description" -Keys @{Primary='changed primary key'} -Diagnostics @{Level='All'}
```

<span data-ttu-id="4cd26-113">Aqui, alteramos a descrição, a chave de acesso principal e habilitamos a coleção de diagnósticos para todos os rastreamentos durante o tempo de execução do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-113">Here, we change the description, primary access key and enable the diagnostics collection for all traces during runtime for the web service.</span></span>

### <span data-ttu-id="4cd26-114">Exemplo 2: Atualização com base em uma instância do serviço Web</span><span class="sxs-lookup"><span data-stu-id="4cd26-114">Example 2: Update based on a web service instance</span></span>
```
$updates = @{ Properties = @{ Title="New Title"; RealtimeConfiguration = @{ MaxConcurrentCalls=25 }}}

Update-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -ServiceUpdates $updates
```

<span data-ttu-id="4cd26-115">O exemplo primeiro cria uma definição de serviço Web, que contém apenas os campos a serem atualizados e chama o Update-AzMlWebService para aplicá-los usando o parâmetro ServiceUpdates.</span><span class="sxs-lookup"><span data-stu-id="4cd26-115">The example first creates a web service definition, that only contains the fields to be updated, and then calls the Update-AzMlWebService to apply them using the ServiceUpdates parameter.</span></span>

## <span data-ttu-id="4cd26-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4cd26-116">PARAMETERS</span></span>

### <span data-ttu-id="4cd26-117">-Assets</span><span class="sxs-lookup"><span data-stu-id="4cd26-117">-Assets</span></span>
<span data-ttu-id="4cd26-118">O conjunto de ativos (por exemplo, módulos, conjuntos de dados) que comem o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-118">The set of assets (e.g. modules, datasets) that make up the web service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cd26-119">-DefaultProfile</span></span>
<span data-ttu-id="4cd26-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4cd26-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cd26-121">-Description</span><span class="sxs-lookup"><span data-stu-id="4cd26-121">-Description</span></span>
<span data-ttu-id="4cd26-122">O novo valor para a descrição do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-122">The new value for the web service's description.</span></span>
<span data-ttu-id="4cd26-123">Isso é visível no esquema da API swagger do serviço.</span><span class="sxs-lookup"><span data-stu-id="4cd26-123">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-124">-Diagnostics</span><span class="sxs-lookup"><span data-stu-id="4cd26-124">-Diagnostics</span></span>
<span data-ttu-id="4cd26-125">As configurações que controlam a coleção de rastreamentos de diagnósticos para o serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-125">The settings that control the diagnostics traces collection for the web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.DiagnosticsConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4cd26-126">-Force</span></span>
<span data-ttu-id="4cd26-127">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="4cd26-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4cd26-128">-Input</span><span class="sxs-lookup"><span data-stu-id="4cd26-128">-Input</span></span>
<span data-ttu-id="4cd26-129">A definição para as entradas do serviço Web, fornecidas como uma construção de esquema swagger.</span><span class="sxs-lookup"><span data-stu-id="4cd26-129">The definition for the web service's input(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-130">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="4cd26-130">-IsReadOnly</span></span>
<span data-ttu-id="4cd26-131">Especifica que esse serviço Web é readonly.</span><span class="sxs-lookup"><span data-stu-id="4cd26-131">Specifies that this web service is readonly.</span></span>
<span data-ttu-id="4cd26-132">Depois de definido, o serviço Web pode ser mais atualizado, incluindo a alteração do valor dessa propriedade e só pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="4cd26-132">Once set, the web service can longer be updated, including changing the value of this property, and can only be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-133">-Keys</span><span class="sxs-lookup"><span data-stu-id="4cd26-133">-Keys</span></span>
<span data-ttu-id="4cd26-134">Atualiza uma ou ambas as teclas de acesso usadas para autenticar chamadas para as APIs de tempo de execução do serviço.</span><span class="sxs-lookup"><span data-stu-id="4cd26-134">Updates one or both of the access keys used to authenticate calls to the service's runtime APIs.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-135">-Name</span><span class="sxs-lookup"><span data-stu-id="4cd26-135">-Name</span></span>
<span data-ttu-id="4cd26-136">O nome do recurso de serviço Web a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-136">The name of the web service resource to be updated.</span></span>

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

### <span data-ttu-id="4cd26-137">-Output</span><span class="sxs-lookup"><span data-stu-id="4cd26-137">-Output</span></span>
<span data-ttu-id="4cd26-138">A definição para as saídas do serviço Web, fornecidas como uma construção de esquema swagger.</span><span class="sxs-lookup"><span data-stu-id="4cd26-138">The definition for the web service's output(s), provided as a Swagger schema construct.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.ServiceInputOutputSpecification
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-139">-Package</span><span class="sxs-lookup"><span data-stu-id="4cd26-139">-Package</span></span>
<span data-ttu-id="4cd26-140">A definição do pacote gráfico que define esse serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-140">The definition of the graph package that defines this web service.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.GraphPackage
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4cd26-141">-Parameters</span></span>
<span data-ttu-id="4cd26-142">O conjunto de valores de parâmetros globais definidos para o serviço Web, dado como um nome de parâmetro global - \> coleção de valores padrão.</span><span class="sxs-lookup"><span data-stu-id="4cd26-142">The set of global parameters values defined for the web service, given as a global parameter name -\> default value collection.</span></span>
<span data-ttu-id="4cd26-143">Se nenhum valor padrão for especificado, o parâmetro será considerado obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4cd26-143">If no default value is specified, the parameter is considered to be required.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-144">-RealtimeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cd26-144">-RealtimeConfiguration</span></span>
<span data-ttu-id="4cd26-145">Atualizações para a configuração do ponto de extremidade em tempo real do serviço.</span><span class="sxs-lookup"><span data-stu-id="4cd26-145">Updates for the configuration of the service's realtime endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.RealtimeConfiguration
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cd26-146">-ResourceGroupName</span></span>
<span data-ttu-id="4cd26-147">O grupo de recursos que contém o serviço Web a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-147">The resource group that contains the web service to be updated.</span></span>

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

### <span data-ttu-id="4cd26-148">-ServiceUpdates</span><span class="sxs-lookup"><span data-stu-id="4cd26-148">-ServiceUpdates</span></span>
<span data-ttu-id="4cd26-149">Um conjunto de atualizações a ser aplicada ao serviço Web fornecido como uma instância de definição de serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-149">A set of updates to apply to the web service provided as a web service definition instance.</span></span>
<span data-ttu-id="4cd26-150">Somente campos não estáticos são modificados.</span><span class="sxs-lookup"><span data-stu-id="4cd26-150">Only non-static fields are modified.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: UpdateFromObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4cd26-151">-StorageAccountKey</span></span>
<span data-ttu-id="4cd26-152">Gira a chave de acesso para a conta de armazenamento associada ao serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-152">Rotates the access key for the storage account associated with the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-153">-Title</span><span class="sxs-lookup"><span data-stu-id="4cd26-153">-Title</span></span>
<span data-ttu-id="4cd26-154">O novo valor para o título do serviço Web.</span><span class="sxs-lookup"><span data-stu-id="4cd26-154">The new value for the web service's title.</span></span>
<span data-ttu-id="4cd26-155">Isso é visível no esquema da API swagger do serviço.</span><span class="sxs-lookup"><span data-stu-id="4cd26-155">This is visible in the service's Swagger API schema.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFromParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cd26-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cd26-156">-Confirm</span></span>
<span data-ttu-id="4cd26-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cd26-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cd26-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cd26-158">-WhatIf</span></span>
<span data-ttu-id="4cd26-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cd26-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cd26-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cd26-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cd26-161">CommonParameters</span></span>
<span data-ttu-id="4cd26-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cd26-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cd26-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cd26-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cd26-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4cd26-164">INPUTS</span></span>

### <span data-ttu-id="4cd26-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="4cd26-165">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4cd26-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4cd26-166">OUTPUTS</span></span>

### <span data-ttu-id="4cd26-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="4cd26-167">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4cd26-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="4cd26-168">NOTES</span></span>
<span data-ttu-id="4cd26-169">Palavras-chave: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4cd26-169">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4cd26-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cd26-170">RELATED LINKS</span></span>
