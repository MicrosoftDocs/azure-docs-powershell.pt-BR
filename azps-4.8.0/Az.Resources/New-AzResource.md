---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: eea8d72285e478f9eecb0a34f80cae5787ecec83
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405288"
---
# <span data-ttu-id="37cf6-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="37cf6-101">New-AzResource</span></span>

## <span data-ttu-id="37cf6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="37cf6-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-103">Creates a resource.</span></span>

## <span data-ttu-id="37cf6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37cf6-104">SYNTAX</span></span>

### <span data-ttu-id="37cf6-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37cf6-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cf6-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="37cf6-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cf6-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="37cf6-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37cf6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="37cf6-108">DESCRIPTION</span></span>
<span data-ttu-id="37cf6-109">O cmdlet **New-AzResource** cria um recurso do Azure, como um site, um servidor de banco de dados SQL do Azure ou um banco de dados SQL do Azure, em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37cf6-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="37cf6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37cf6-110">EXAMPLES</span></span>

### <span data-ttu-id="37cf6-111">Exemplo 1: Criar um recurso</span><span class="sxs-lookup"><span data-stu-id="37cf6-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="37cf6-112">Esse comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="37cf6-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="37cf6-113">Exemplo 2: Criar um recurso usando a esplatação</span><span class="sxs-lookup"><span data-stu-id="37cf6-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="37cf6-114">Esse comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="37cf6-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="37cf6-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37cf6-115">PARAMETERS</span></span>

### <span data-ttu-id="37cf6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="37cf6-116">-ApiVersion</span></span>
<span data-ttu-id="37cf6-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="37cf6-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="37cf6-118">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="37cf6-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="37cf6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37cf6-119">-AsJob</span></span>
<span data-ttu-id="37cf6-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="37cf6-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37cf6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cf6-121">-DefaultProfile</span></span>
<span data-ttu-id="37cf6-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="37cf6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37cf6-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="37cf6-123">-ExtensionResourceName</span></span>
<span data-ttu-id="37cf6-124">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="37cf6-125">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="37cf6-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="37cf6-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="37cf6-126">-ExtensionResourceType</span></span>
<span data-ttu-id="37cf6-127">Especifica o tipo de recurso de um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="37cf6-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="37cf6-128">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="37cf6-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="37cf6-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="37cf6-129">-Force</span></span>
<span data-ttu-id="37cf6-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="37cf6-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37cf6-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="37cf6-131">-IsFullObject</span></span>
<span data-ttu-id="37cf6-132">Indica que o objeto especificado pelo parâmetro *Propriedades* é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="37cf6-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="37cf6-133">-Tipo</span><span class="sxs-lookup"><span data-stu-id="37cf6-133">-Kind</span></span>
<span data-ttu-id="37cf6-134">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="37cf6-135">-Local</span><span class="sxs-lookup"><span data-stu-id="37cf6-135">-Location</span></span>
<span data-ttu-id="37cf6-136">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="37cf6-137">Especifique a localização do data center, como o Centro dos EUA ou o Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="37cf6-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="37cf6-138">Você pode colocar um recurso em qualquer local que suporte recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="37cf6-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="37cf6-139">Os grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="37cf6-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="37cf6-140">Para determinar quais locais suportam cada tipo de recurso, use Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37cf6-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="37cf6-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="37cf6-141">-ODataQuery</span></span>
<span data-ttu-id="37cf6-142">Especifica um filtro de estilo OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="37cf6-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="37cf6-143">Esse cmdlet anexa esse valor à solicitação além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="37cf6-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="37cf6-144">-Plano</span><span class="sxs-lookup"><span data-stu-id="37cf6-144">-Plan</span></span>
<span data-ttu-id="37cf6-145">Uma tabela hash que representa propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="37cf6-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="37cf6-146">-Pré-</span><span class="sxs-lookup"><span data-stu-id="37cf6-146">-Pre</span></span>
<span data-ttu-id="37cf6-147">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="37cf6-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="37cf6-148">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="37cf6-148">-Properties</span></span>
<span data-ttu-id="37cf6-149">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="37cf6-150">Use este parâmetro para especificar os valores de propriedades específicos de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="37cf6-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cf6-151">-ResourceGroupName</span></span>
<span data-ttu-id="37cf6-152">Especifica o nome do grupo de recursos onde esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="37cf6-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37cf6-153">-ResourceId</span></span>
<span data-ttu-id="37cf6-154">Especifica a ID de recurso totalmente qualificada, incluindo a assinatura, como no exemplo a `/subscriptions/` seguir: ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="37cf6-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="37cf6-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37cf6-155">-ResourceName</span></span>
<span data-ttu-id="37cf6-156">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-156">Specifies the name of the resource.</span></span> <span data-ttu-id="37cf6-157">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="37cf6-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="37cf6-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="37cf6-158">-ResourceType</span></span>
<span data-ttu-id="37cf6-159">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="37cf6-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="37cf6-160">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="37cf6-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="37cf6-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="37cf6-161">-Sku</span></span>
<span data-ttu-id="37cf6-162">Uma tabela hash que representa propriedades de sku.</span><span class="sxs-lookup"><span data-stu-id="37cf6-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="37cf6-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="37cf6-163">-Tag</span></span>
<span data-ttu-id="37cf6-164">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="37cf6-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="37cf6-165">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="37cf6-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="37cf6-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="37cf6-166">-TenantLevel</span></span>
<span data-ttu-id="37cf6-167">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="37cf6-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="37cf6-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="37cf6-168">-Confirm</span></span>
<span data-ttu-id="37cf6-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37cf6-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cf6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cf6-170">-WhatIf</span></span>
<span data-ttu-id="37cf6-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="37cf6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cf6-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37cf6-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cf6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cf6-173">CommonParameters</span></span>
<span data-ttu-id="37cf6-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cf6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cf6-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37cf6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cf6-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="37cf6-176">INPUTS</span></span>

### <span data-ttu-id="37cf6-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="37cf6-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="37cf6-178">System.String</span><span class="sxs-lookup"><span data-stu-id="37cf6-178">System.String</span></span>

## <span data-ttu-id="37cf6-179">Saídas</span><span class="sxs-lookup"><span data-stu-id="37cf6-179">OUTPUTS</span></span>

### <span data-ttu-id="37cf6-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="37cf6-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="37cf6-181">Notas</span><span class="sxs-lookup"><span data-stu-id="37cf6-181">NOTES</span></span>

## <span data-ttu-id="37cf6-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37cf6-182">RELATED LINKS</span></span>


[<span data-ttu-id="37cf6-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="37cf6-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="37cf6-184">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="37cf6-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="37cf6-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="37cf6-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="37cf6-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="37cf6-186">Set-AzResource</span></span>](./Set-AzResource.md)
