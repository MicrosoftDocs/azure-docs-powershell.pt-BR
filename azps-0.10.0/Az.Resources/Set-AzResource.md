---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: d6b8b2edbae697ca9b0427ca7e213de966e35bb6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93786613"
---
# <span data-ttu-id="4d4f5-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-101">Set-AzResource</span></span>

## <span data-ttu-id="4d4f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d4f5-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4f5-103">Modifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-103">Modifies a resource.</span></span>

## <span data-ttu-id="4d4f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d4f5-104">SYNTAX</span></span>

### <span data-ttu-id="4d4f5-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="4d4f5-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d4f5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4d4f5-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d4f5-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="4d4f5-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d4f5-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="4d4f5-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d4f5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d4f5-109">DESCRIPTION</span></span>
<span data-ttu-id="4d4f5-110">O cmdlet **set-AzResource** modifica um recurso existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="4d4f5-111">Especifique um recurso a ser modificado por nome e tipo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="4d4f5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d4f5-112">EXAMPLES</span></span>

### <span data-ttu-id="4d4f5-113">Exemplo 1: modificar um recurso</span><span class="sxs-lookup"><span data-stu-id="4d4f5-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="4d4f5-114">O primeiro comando obtém o recurso denominado ContosoSite usando o cmdlet Get-AzResource e, em seguida, armazena-o na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="4d4f5-115">O segundo comando modifica uma propriedade de $Resource.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="4d4f5-116">O comando final atualiza o recurso para corresponder ao $Resource.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="4d4f5-117">Exemplo 2: modificar todos os recursos em um determinado grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4d4f5-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="4d4f5-118">O primeiro comando obtém os recursos no grupo de recursos testrg e, em seguida, os armazena na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="4d4f5-119">O segundo comando itera em cada um desses recursos no grupo de recursos e adiciona uma nova marca a ele.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="4d4f5-120">O comando final atualiza cada um desses recursos.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="4d4f5-121">OS</span><span class="sxs-lookup"><span data-stu-id="4d4f5-121">PARAMETERS</span></span>

### <span data-ttu-id="4d4f5-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d4f5-122">-ApiVersion</span></span>
<span data-ttu-id="4d4f5-123">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4d4f5-124">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4d4f5-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d4f5-125">-AsJob</span></span>
<span data-ttu-id="4d4f5-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4d4f5-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d4f5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4f5-127">-DefaultProfile</span></span>
<span data-ttu-id="4d4f5-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4d4f5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d4f5-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="4d4f5-129">-ExtensionResourceName</span></span>
<span data-ttu-id="4d4f5-130">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="4d4f5-131">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="4d4f5-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="4d4f5-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="4d4f5-132">-ExtensionResourceType</span></span>
<span data-ttu-id="4d4f5-133">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="4d4f5-134">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4d4f5-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4d4f5-135">-Force</span><span class="sxs-lookup"><span data-stu-id="4d4f5-135">-Force</span></span>
<span data-ttu-id="4d4f5-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d4f5-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d4f5-137">-InputObject</span></span>
<span data-ttu-id="4d4f5-138">A representação do objeto do recurso a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="4d4f5-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="4d4f5-139">-Kind</span></span>
<span data-ttu-id="4d4f5-140">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="4d4f5-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="4d4f5-141">-ODataQuery</span></span>
<span data-ttu-id="4d4f5-142">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="4d4f5-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="4d4f5-143">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="4d4f5-144">-Plano</span><span class="sxs-lookup"><span data-stu-id="4d4f5-144">-Plan</span></span>
<span data-ttu-id="4d4f5-145">Especifica as propriedades do plano de recursos, como uma tabela de hash, para o recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="4d4f5-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d4f5-146">-Pre</span></span>
<span data-ttu-id="4d4f5-147">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4d4f5-148">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="4d4f5-148">-Properties</span></span>
<span data-ttu-id="4d4f5-149">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="4d4f5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4f5-150">-ResourceGroupName</span></span>
<span data-ttu-id="4d4f5-151">Especifica o nome do grupo de recursos em que esse cmdlet modifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="4d4f5-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d4f5-152">-ResourceId</span></span>
<span data-ttu-id="4d4f5-153">Especifica a ID do recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4d4f5-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4d4f5-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4d4f5-154">-ResourceName</span></span>
<span data-ttu-id="4d4f5-155">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="4d4f5-156">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="4d4f5-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="4d4f5-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4d4f5-157">-ResourceType</span></span>
<span data-ttu-id="4d4f5-158">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="4d4f5-159">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="4d4f5-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="4d4f5-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="4d4f5-160">-Sku</span></span>
<span data-ttu-id="4d4f5-161">Especifica o objeto SKU do recurso como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="4d4f5-162">-Marca</span><span class="sxs-lookup"><span data-stu-id="4d4f5-162">-Tag</span></span>
<span data-ttu-id="4d4f5-163">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4d4f5-164">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4d4f5-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4d4f5-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="4d4f5-165">-TenantLevel</span></span>
<span data-ttu-id="4d4f5-166">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="4d4f5-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="4d4f5-167">-UsePatchSemantics</span></span>
<span data-ttu-id="4d4f5-168">Indica que esse cmdlet usa um PATCH HTTP para atualizar o objeto, em vez de um HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="4d4f5-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d4f5-169">-Confirm</span></span>
<span data-ttu-id="4d4f5-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d4f5-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d4f5-171">-WhatIf</span></span>
<span data-ttu-id="4d4f5-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d4f5-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d4f5-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4f5-174">CommonParameters</span></span>
<span data-ttu-id="4d4f5-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d4f5-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4f5-176">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d4f5-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4f5-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d4f5-177">INPUTS</span></span>

### <span data-ttu-id="4d4f5-178">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4d4f5-178">None</span></span>

## <span data-ttu-id="4d4f5-179">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d4f5-179">OUTPUTS</span></span>

### <span data-ttu-id="4d4f5-180">Microsoft. Azure. Commands. ResourceManager. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-180">Microsoft.Azure.Commands.ResourceManager.Models.PSResource</span></span>

## <span data-ttu-id="4d4f5-181">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d4f5-181">NOTES</span></span>

## <span data-ttu-id="4d4f5-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d4f5-182">RELATED LINKS</span></span>

[<span data-ttu-id="4d4f5-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="4d4f5-184">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="4d4f5-185">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-185">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4d4f5-186">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="4d4f5-186">Remove-AzResource</span></span>](./Remove-AzResource.md)
