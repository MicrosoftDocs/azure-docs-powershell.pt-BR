---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: a3180cd693ae4c234656ba5d0812900ce8c308b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891398"
---
# <span data-ttu-id="5cd50-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="5cd50-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="5cd50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd50-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd50-103">Cria ou atualiza o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="5cd50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5cd50-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5cd50-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5cd50-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd50-106">Cria ou atualiza o provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="5cd50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5cd50-107">EXAMPLES</span></span>

### <span data-ttu-id="5cd50-108">Exemplo 1: Criar um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="5cd50-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="5cd50-109">Criar um provedor de recursos personalizado</span><span class="sxs-lookup"><span data-stu-id="5cd50-109">Create a custom resource provider</span></span>

### <span data-ttu-id="5cd50-110">Exemplo 2: Criar um provedor personalizado com associações</span><span class="sxs-lookup"><span data-stu-id="5cd50-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="5cd50-111">Crie um provedor personalizado, com uma rota para associações de provedores personalizados.</span><span class="sxs-lookup"><span data-stu-id="5cd50-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="5cd50-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5cd50-112">PARAMETERS</span></span>

### <span data-ttu-id="5cd50-113">-Action</span><span class="sxs-lookup"><span data-stu-id="5cd50-113">-Action</span></span>
<span data-ttu-id="5cd50-114">Uma lista de ações que o provedor de recursos personalizado implementa.</span><span class="sxs-lookup"><span data-stu-id="5cd50-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="5cd50-115">Para construir, consulte a seção NOTES para propriedades ACTION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5cd50-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cd50-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cd50-116">-AsJob</span></span>
<span data-ttu-id="5cd50-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="5cd50-117">Run the command as a job</span></span>

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

### <span data-ttu-id="5cd50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd50-118">-DefaultProfile</span></span>
<span data-ttu-id="5cd50-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd50-120">-Location</span><span class="sxs-lookup"><span data-stu-id="5cd50-120">-Location</span></span>
<span data-ttu-id="5cd50-121">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="5cd50-121">Resource location</span></span>

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

### <span data-ttu-id="5cd50-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5cd50-122">-Name</span></span>
<span data-ttu-id="5cd50-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cd50-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="5cd50-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5cd50-124">-NoWait</span></span>
<span data-ttu-id="5cd50-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="5cd50-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5cd50-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd50-126">-ResourceGroupName</span></span>
<span data-ttu-id="5cd50-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cd50-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5cd50-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="5cd50-128">-ResourceType</span></span>
<span data-ttu-id="5cd50-129">Uma lista de tipos de recursos que o provedor de recursos personalizado implementa.</span><span class="sxs-lookup"><span data-stu-id="5cd50-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="5cd50-130">Para construir, consulte a seção NOTES para propriedades RESOURCETYPE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5cd50-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cd50-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cd50-131">-SubscriptionId</span></span>
<span data-ttu-id="5cd50-132">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd50-132">The Azure subscription ID.</span></span>
<span data-ttu-id="5cd50-133">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="5cd50-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="5cd50-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="5cd50-134">-Tag</span></span>
<span data-ttu-id="5cd50-135">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="5cd50-135">Resource tags</span></span>

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

### <span data-ttu-id="5cd50-136">-Validation</span><span class="sxs-lookup"><span data-stu-id="5cd50-136">-Validation</span></span>
<span data-ttu-id="5cd50-137">Uma lista de validações a ser executado nas solicitações do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="5cd50-138">Para construir, consulte a seção NOTES para propriedades VALIDATION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5cd50-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="5cd50-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cd50-139">-Confirm</span></span>
<span data-ttu-id="5cd50-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd50-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd50-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd50-141">-WhatIf</span></span>
<span data-ttu-id="5cd50-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd50-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd50-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd50-144">CommonParameters</span></span>
<span data-ttu-id="5cd50-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd50-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd50-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cd50-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd50-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd50-147">INPUTS</span></span>

## <span data-ttu-id="5cd50-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5cd50-148">OUTPUTS</span></span>

### <span data-ttu-id="5cd50-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="5cd50-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="5cd50-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="5cd50-150">NOTES</span></span>

<span data-ttu-id="5cd50-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5cd50-151">ALIASES</span></span>

<span data-ttu-id="5cd50-152">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="5cd50-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cd50-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5cd50-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cd50-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5cd50-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cd50-155">ACTION <ICustomRpActionRouteDefinition[]>: uma lista de ações que o provedor de recursos personalizado implementa.</span><span class="sxs-lookup"><span data-stu-id="5cd50-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="5cd50-156">`Endpoint <String>`: O URI do ponto de extremidade de definição de rota para o que o provedor de recursos personalizados fará solicitações de proxy.</span><span class="sxs-lookup"><span data-stu-id="5cd50-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="5cd50-157">Isso pode estar na forma de um URI simples (por exemplo, ' ') ou pode especificar a rota por meio de um caminho https://testendpoint/ (por exemplo, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="5cd50-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="5cd50-158">`Name <String>`: O nome da definição de rota.</span><span class="sxs-lookup"><span data-stu-id="5cd50-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="5cd50-159">Isso se torna o nome da extensão ARM (por exemplo, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="5cd50-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="5cd50-160">`[RoutingType <ActionRouting?>]`: Os tipos de roteamento com suporte para solicitações de ação.</span><span class="sxs-lookup"><span data-stu-id="5cd50-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="5cd50-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: uma lista de tipos de recursos que o provedor de recursos personalizado implementa.</span><span class="sxs-lookup"><span data-stu-id="5cd50-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="5cd50-162">`Endpoint <String>`: O URI do ponto de extremidade de definição de rota para o que o provedor de recursos personalizados fará solicitações de proxy.</span><span class="sxs-lookup"><span data-stu-id="5cd50-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="5cd50-163">Isso pode estar na forma de um URI simples (por exemplo, ' ') ou pode especificar a rota por meio de um caminho https://testendpoint/ (por exemplo, ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="5cd50-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="5cd50-164">`Name <String>`: O nome da definição de rota.</span><span class="sxs-lookup"><span data-stu-id="5cd50-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="5cd50-165">Isso se torna o nome da extensão ARM (por exemplo, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="5cd50-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="5cd50-166">`[RoutingType <ResourceTypeRouting?>]`: Os tipos de roteamento com suporte para solicitações de recursos.</span><span class="sxs-lookup"><span data-stu-id="5cd50-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="5cd50-167">VALIDAÇÃO <ICustomRpValidations[]>: uma lista de validações a ser executado nas solicitações do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="5cd50-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="5cd50-168">`Specification <String>`: Um link para a especificação de validação.</span><span class="sxs-lookup"><span data-stu-id="5cd50-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="5cd50-169">A especificação deve ser hospedada no raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="5cd50-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="5cd50-170">`[ValidationType <ValidationType?>]`: O tipo de validação a ser executado em uma solicitação correspondente.</span><span class="sxs-lookup"><span data-stu-id="5cd50-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="5cd50-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5cd50-171">RELATED LINKS</span></span>

