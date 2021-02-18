---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415743"
---
# <span data-ttu-id="c121d-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="c121d-101">Set-AzResource</span></span>

## <span data-ttu-id="c121d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c121d-102">SYNOPSIS</span></span>
<span data-ttu-id="c121d-103">Modifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-103">Modifies a resource.</span></span>

## <span data-ttu-id="c121d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c121d-104">SYNTAX</span></span>

### <span data-ttu-id="c121d-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c121d-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c121d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c121d-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c121d-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c121d-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c121d-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c121d-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c121d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c121d-109">DESCRIPTION</span></span>
<span data-ttu-id="c121d-110">O **cmdlet Set-AzResource** modifica um recurso existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="c121d-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="c121d-111">Especifique um recurso para modificar por nome e tipo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="c121d-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="c121d-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c121d-112">EXAMPLES</span></span>

### <span data-ttu-id="c121d-113">Exemplo 1: Modificar um recurso</span><span class="sxs-lookup"><span data-stu-id="c121d-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="c121d-114">O primeiro comando obtém o recurso contosoSite usando o cmdlet Get-AzResource e, em seguida, o armazena na variável $Resource dados.</span><span class="sxs-lookup"><span data-stu-id="c121d-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="c121d-115">O segundo comando modifica uma propriedade de $Resource.</span><span class="sxs-lookup"><span data-stu-id="c121d-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="c121d-116">O comando final atualiza o recurso para corresponder $Resource.</span><span class="sxs-lookup"><span data-stu-id="c121d-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="c121d-117">Exemplo 2: Modificar todos os recursos em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c121d-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="c121d-118">O primeiro comando obtém os recursos no grupo de recursos testrg e os armazena na variável $Resource dados.</span><span class="sxs-lookup"><span data-stu-id="c121d-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="c121d-119">O segundo comando itera sobre cada um desses recursos no grupo de recursos e adiciona uma nova marca a eles.</span><span class="sxs-lookup"><span data-stu-id="c121d-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="c121d-120">O comando final atualiza cada um desses recursos.</span><span class="sxs-lookup"><span data-stu-id="c121d-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="c121d-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c121d-121">PARAMETERS</span></span>

### <span data-ttu-id="c121d-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c121d-122">-ApiVersion</span></span>
<span data-ttu-id="c121d-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c121d-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c121d-124">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="c121d-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c121d-125">-AsJob</span></span>
<span data-ttu-id="c121d-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c121d-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c121d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c121d-127">-DefaultProfile</span></span>
<span data-ttu-id="c121d-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c121d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c121d-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c121d-129">-ExtensionResourceName</span></span>
<span data-ttu-id="c121d-130">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="c121d-131">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="c121d-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c121d-132">-ExtensionResourceType</span></span>
<span data-ttu-id="c121d-133">Especifica o tipo de recurso de um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="c121d-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c121d-134">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c121d-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-135">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c121d-135">-Force</span></span>
<span data-ttu-id="c121d-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c121d-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c121d-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c121d-137">-InputObject</span></span>
<span data-ttu-id="c121d-138">A representação de objeto do recurso a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c121d-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-139">-Tipo</span><span class="sxs-lookup"><span data-stu-id="c121d-139">-Kind</span></span>
<span data-ttu-id="c121d-140">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c121d-141">-ODataQuery</span></span>
<span data-ttu-id="c121d-142">Especifica um filtro de estilo OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="c121d-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c121d-143">Esse cmdlet anexa esse valor à solicitação além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="c121d-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-144">-Plano</span><span class="sxs-lookup"><span data-stu-id="c121d-144">-Plan</span></span>
<span data-ttu-id="c121d-145">Especifica as propriedades do plano de recursos, como uma tabela hash, para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-146">-Pré-</span><span class="sxs-lookup"><span data-stu-id="c121d-146">-Pre</span></span>
<span data-ttu-id="c121d-147">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c121d-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c121d-148">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="c121d-148">-Properties</span></span>
<span data-ttu-id="c121d-149">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c121d-150">-ResourceGroupName</span></span>
<span data-ttu-id="c121d-151">Especifica o nome do grupo de recursos onde esse cmdlet modifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c121d-152">-ResourceId</span></span>
<span data-ttu-id="c121d-153">Especifica a ID de recurso totalmente qualificada, incluindo a assinatura, como no exemplo a `/subscriptions/` seguir: ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c121d-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c121d-154">-ResourceName</span></span>
<span data-ttu-id="c121d-155">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="c121d-156">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c121d-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c121d-157">-ResourceType</span></span>
<span data-ttu-id="c121d-158">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="c121d-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="c121d-159">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c121d-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="c121d-160">-Sku</span></span>
<span data-ttu-id="c121d-161">Especifica o objeto SKU do recurso como uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c121d-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="c121d-162">-Tag</span></span>
<span data-ttu-id="c121d-163">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="c121d-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c121d-164">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="c121d-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c121d-165">-TenantLevel</span></span>
<span data-ttu-id="c121d-166">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="c121d-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c121d-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="c121d-167">-UsePatchSemantics</span></span>
<span data-ttu-id="c121d-168">Indica que esse cmdlet usa um PATCH HTTP para atualizar o objeto, em vez de um HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="c121d-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="c121d-169">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c121d-169">-Confirm</span></span>
<span data-ttu-id="c121d-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c121d-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c121d-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c121d-171">-WhatIf</span></span>
<span data-ttu-id="c121d-172">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c121d-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c121d-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c121d-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c121d-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c121d-174">CommonParameters</span></span>
<span data-ttu-id="c121d-175">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c121d-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c121d-176">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c121d-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c121d-177">Entradas</span><span class="sxs-lookup"><span data-stu-id="c121d-177">INPUTS</span></span>

### <span data-ttu-id="c121d-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="c121d-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="c121d-179">System.String</span><span class="sxs-lookup"><span data-stu-id="c121d-179">System.String</span></span>

### <span data-ttu-id="c121d-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c121d-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="c121d-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c121d-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c121d-182">Saídas</span><span class="sxs-lookup"><span data-stu-id="c121d-182">OUTPUTS</span></span>

### <span data-ttu-id="c121d-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c121d-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c121d-184">Notas</span><span class="sxs-lookup"><span data-stu-id="c121d-184">NOTES</span></span>

## <span data-ttu-id="c121d-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c121d-185">RELATED LINKS</span></span>


[<span data-ttu-id="c121d-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c121d-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="c121d-187">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="c121d-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="c121d-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="c121d-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c121d-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="c121d-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
