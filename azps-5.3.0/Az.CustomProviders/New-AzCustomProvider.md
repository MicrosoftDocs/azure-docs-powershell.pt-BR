---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433991"
---
# <span data-ttu-id="3de33-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="3de33-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="3de33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3de33-102">SYNOPSIS</span></span>
<span data-ttu-id="3de33-103">Cria ou atualiza o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de33-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="3de33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3de33-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3de33-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3de33-105">DESCRIPTION</span></span>
<span data-ttu-id="3de33-106">Cria ou atualiza o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de33-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="3de33-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3de33-107">EXAMPLES</span></span>

### <span data-ttu-id="3de33-108">Exemplo 1: criar um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="3de33-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="3de33-109">Criar um provedor de recursos personalizado</span><span class="sxs-lookup"><span data-stu-id="3de33-109">Create a custom resource provider</span></span>

### <span data-ttu-id="3de33-110">Exemplo 2: criar um provedor personalizado com associações</span><span class="sxs-lookup"><span data-stu-id="3de33-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="3de33-111">Crie um provedor personalizado, com uma rota para associações de provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de33-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="3de33-112">OS</span><span class="sxs-lookup"><span data-stu-id="3de33-112">PARAMETERS</span></span>

### <span data-ttu-id="3de33-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="3de33-113">-Action</span></span>
<span data-ttu-id="3de33-114">Uma lista de ações implementadas pelo provedor de recursos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3de33-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="3de33-115">Para construir, consulte a seção observações para propriedades de ação e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3de33-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3de33-116">-AsJob</span></span>
<span data-ttu-id="3de33-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3de33-117">Run the command as a job</span></span>

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

### <span data-ttu-id="3de33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de33-118">-DefaultProfile</span></span>
<span data-ttu-id="3de33-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3de33-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-120">-Local</span><span class="sxs-lookup"><span data-stu-id="3de33-120">-Location</span></span>
<span data-ttu-id="3de33-121">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="3de33-121">Resource location</span></span>

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

### <span data-ttu-id="3de33-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3de33-122">-Name</span></span>
<span data-ttu-id="3de33-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de33-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3de33-124">-NoWait</span></span>
<span data-ttu-id="3de33-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3de33-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3de33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de33-126">-ResourceGroupName</span></span>
<span data-ttu-id="3de33-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3de33-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3de33-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3de33-128">-ResourceType</span></span>
<span data-ttu-id="3de33-129">Uma lista de tipos de recurso implementados pelo provedor de recursos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3de33-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="3de33-130">Para construir, consulte a seção de observações para as propriedades de RESOURCETYPE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3de33-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3de33-131">-SubscriptionId</span></span>
<span data-ttu-id="3de33-132">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="3de33-132">The Azure subscription ID.</span></span>
<span data-ttu-id="3de33-133">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3de33-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="3de33-134">-Tag</span></span>
<span data-ttu-id="3de33-135">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="3de33-135">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-136">-Validação</span><span class="sxs-lookup"><span data-stu-id="3de33-136">-Validation</span></span>
<span data-ttu-id="3de33-137">Uma lista de validações a serem executadas nas solicitações do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de33-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="3de33-138">Para construir, consulte a seção de notas para propriedades de validação e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3de33-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de33-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3de33-139">-Confirm</span></span>
<span data-ttu-id="3de33-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de33-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de33-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de33-141">-WhatIf</span></span>
<span data-ttu-id="3de33-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3de33-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de33-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3de33-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de33-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de33-144">CommonParameters</span></span>
<span data-ttu-id="3de33-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de33-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de33-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3de33-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de33-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3de33-147">INPUTS</span></span>

## <span data-ttu-id="3de33-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3de33-148">OUTPUTS</span></span>

### <span data-ttu-id="3de33-149">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="3de33-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="3de33-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3de33-150">NOTES</span></span>

<span data-ttu-id="3de33-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3de33-151">ALIASES</span></span>

<span data-ttu-id="3de33-152">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3de33-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3de33-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3de33-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3de33-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3de33-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3de33-155">AÇÃO <ICustomRpActionRouteDefinition [] >: uma lista de ações implementadas pelo provedor de recursos personalizados.</span><span class="sxs-lookup"><span data-stu-id="3de33-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="3de33-156">`Endpoint <String>`: O URI de ponto de extremidade de definição de rota ao qual o provedor de recursos personalizado fará a solicitação de proxy.</span><span class="sxs-lookup"><span data-stu-id="3de33-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="3de33-157">Isso pode ser na forma de um URI simples (por exemplo, ' https://testendpoint/ ') ou pode especificar a rota por meio de um caminho (por exemplo, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="3de33-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="3de33-158">`Name <String>`: O nome da definição de roteiro.</span><span class="sxs-lookup"><span data-stu-id="3de33-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="3de33-159">Isso se torna o nome da extensão do braço (por exemplo, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="3de33-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="3de33-160">`[RoutingType <ActionRouting?>]`: Os tipos de roteamento com suporte para solicitações de ação.</span><span class="sxs-lookup"><span data-stu-id="3de33-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="3de33-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: uma lista de tipos de recursos que o provedor de recursos personalizado implementa.</span><span class="sxs-lookup"><span data-stu-id="3de33-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="3de33-162">`Endpoint <String>`: O URI de ponto de extremidade de definição de rota ao qual o provedor de recursos personalizado fará a solicitação de proxy.</span><span class="sxs-lookup"><span data-stu-id="3de33-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="3de33-163">Isso pode ser na forma de um URI simples (por exemplo, ' https://testendpoint/ ') ou pode especificar a rota por meio de um caminho (por exemplo, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="3de33-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="3de33-164">`Name <String>`: O nome da definição de roteiro.</span><span class="sxs-lookup"><span data-stu-id="3de33-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="3de33-165">Isso se torna o nome da extensão do braço (por exemplo, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="3de33-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="3de33-166">`[RoutingType <ResourceTypeRouting?>]`: Os tipos de roteamento com suporte para solicitações de recurso.</span><span class="sxs-lookup"><span data-stu-id="3de33-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="3de33-167">VALIDATION <ICustomRpValidations [] >: uma lista de validações a serem executadas nas solicitações do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="3de33-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="3de33-168">`Specification <String>`: Um link para a especificação de validação.</span><span class="sxs-lookup"><span data-stu-id="3de33-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="3de33-169">A especificação deve ser hospedada no raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="3de33-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="3de33-170">`[ValidationType <ValidationType?>]`: O tipo de validação a ser executada em uma solicitação correspondente.</span><span class="sxs-lookup"><span data-stu-id="3de33-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="3de33-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3de33-171">RELATED LINKS</span></span>

