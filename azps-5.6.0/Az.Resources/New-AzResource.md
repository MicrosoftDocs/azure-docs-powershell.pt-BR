---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 457f5db18ba43d1fd598e255d9ca1fb2e62f3f3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889759"
---
# <span data-ttu-id="b34cb-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="b34cb-101">New-AzResource</span></span>

## <span data-ttu-id="b34cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b34cb-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-103">Creates a resource.</span></span>

## <span data-ttu-id="b34cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b34cb-104">SYNTAX</span></span>

### <span data-ttu-id="b34cb-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b34cb-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b34cb-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="b34cb-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b34cb-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="b34cb-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b34cb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b34cb-108">DESCRIPTION</span></span>
<span data-ttu-id="b34cb-109">O cmdlet **New-AzResource** cria um recurso do Azure, como um site, um servidor de banco de dados do Azure SQL ou o banco de dados do Azure SQL, em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b34cb-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="b34cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b34cb-110">EXAMPLES</span></span>

### <span data-ttu-id="b34cb-111">Exemplo 1: Criar um recurso</span><span class="sxs-lookup"><span data-stu-id="b34cb-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="b34cb-112">Este comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b34cb-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="b34cb-113">Exemplo 2: Criar um recurso usando splatting</span><span class="sxs-lookup"><span data-stu-id="b34cb-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="b34cb-114">Este comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="b34cb-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="b34cb-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b34cb-115">PARAMETERS</span></span>

### <span data-ttu-id="b34cb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b34cb-116">-ApiVersion</span></span>
<span data-ttu-id="b34cb-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="b34cb-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="b34cb-118">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="b34cb-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b34cb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34cb-119">-AsJob</span></span>
<span data-ttu-id="b34cb-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b34cb-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b34cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34cb-121">-DefaultProfile</span></span>
<span data-ttu-id="b34cb-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b34cb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b34cb-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="b34cb-123">-ExtensionResourceName</span></span>
<span data-ttu-id="b34cb-124">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="b34cb-125">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="b34cb-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="b34cb-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="b34cb-126">-ExtensionResourceType</span></span>
<span data-ttu-id="b34cb-127">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="b34cb-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="b34cb-128">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b34cb-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b34cb-129">-Force</span><span class="sxs-lookup"><span data-stu-id="b34cb-129">-Force</span></span>
<span data-ttu-id="b34cb-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b34cb-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b34cb-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="b34cb-131">-IsFullObject</span></span>
<span data-ttu-id="b34cb-132">Indica que o objeto especificado pelo *parâmetro Properties* é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="b34cb-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="b34cb-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="b34cb-133">-Kind</span></span>
<span data-ttu-id="b34cb-134">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="b34cb-135">-Location</span><span class="sxs-lookup"><span data-stu-id="b34cb-135">-Location</span></span>
<span data-ttu-id="b34cb-136">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="b34cb-137">Especifique o local do data center, como o Centro dos EUA ou o Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="b34cb-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="b34cb-138">Você pode colocar um recurso em qualquer local que suporte recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="b34cb-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="b34cb-139">Os grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="b34cb-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="b34cb-140">Para determinar quais locais suportam cada tipo de recurso, use Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34cb-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="b34cb-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="b34cb-141">-ODataQuery</span></span>
<span data-ttu-id="b34cb-142">Especifica um filtro de estilo OData (Protocolo de Dados Abertos).</span><span class="sxs-lookup"><span data-stu-id="b34cb-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="b34cb-143">Este cmdlet anexa esse valor à solicitação, além de quaisquer outros filtros.</span><span class="sxs-lookup"><span data-stu-id="b34cb-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="b34cb-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="b34cb-144">-Plan</span></span>
<span data-ttu-id="b34cb-145">Uma tabela de hash que representa propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="b34cb-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34cb-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="b34cb-146">-Pre</span></span>
<span data-ttu-id="b34cb-147">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="b34cb-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b34cb-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="b34cb-148">-Properties</span></span>
<span data-ttu-id="b34cb-149">Especifica propriedades de recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="b34cb-150">Use este parâmetro para especificar os valores das propriedades específicas de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34cb-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34cb-151">-ResourceGroupName</span></span>
<span data-ttu-id="b34cb-152">Especifica o nome do grupo de recursos onde esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="b34cb-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b34cb-153">-ResourceId</span></span>
<span data-ttu-id="b34cb-154">Especifica a ID de recurso totalmente qualificada, incluindo a assinatura, como no exemplo a `/subscriptions/` seguir: ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b34cb-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b34cb-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b34cb-155">-ResourceName</span></span>
<span data-ttu-id="b34cb-156">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-156">Specifies the name of the resource.</span></span> <span data-ttu-id="b34cb-157">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="b34cb-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="b34cb-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b34cb-158">-ResourceType</span></span>
<span data-ttu-id="b34cb-159">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="b34cb-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="b34cb-160">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="b34cb-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="b34cb-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="b34cb-161">-Sku</span></span>
<span data-ttu-id="b34cb-162">Uma tabela de hash que representa propriedades sku.</span><span class="sxs-lookup"><span data-stu-id="b34cb-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="b34cb-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="b34cb-163">-Tag</span></span>
<span data-ttu-id="b34cb-164">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b34cb-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b34cb-165">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="b34cb-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34cb-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b34cb-166">-TenantLevel</span></span>
<span data-ttu-id="b34cb-167">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="b34cb-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="b34cb-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b34cb-168">-Confirm</span></span>
<span data-ttu-id="b34cb-169">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34cb-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b34cb-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b34cb-170">-WhatIf</span></span>
<span data-ttu-id="b34cb-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b34cb-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b34cb-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b34cb-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b34cb-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34cb-173">CommonParameters</span></span>
<span data-ttu-id="b34cb-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34cb-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34cb-175">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b34cb-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34cb-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b34cb-176">INPUTS</span></span>

### <span data-ttu-id="b34cb-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b34cb-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b34cb-178">System.String</span><span class="sxs-lookup"><span data-stu-id="b34cb-178">System.String</span></span>

## <span data-ttu-id="b34cb-179">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b34cb-179">OUTPUTS</span></span>

### <span data-ttu-id="b34cb-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b34cb-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b34cb-181">NOTES</span><span class="sxs-lookup"><span data-stu-id="b34cb-181">NOTES</span></span>

## <span data-ttu-id="b34cb-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b34cb-182">RELATED LINKS</span></span>

[<span data-ttu-id="b34cb-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="b34cb-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="b34cb-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="b34cb-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="b34cb-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="b34cb-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="b34cb-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="b34cb-186">Set-AzResource</span></span>](./Set-AzResource.md)
