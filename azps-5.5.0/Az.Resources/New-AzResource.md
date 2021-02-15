---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114901"
---
# <span data-ttu-id="1e04f-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e04f-101">New-AzResource</span></span>

## <span data-ttu-id="1e04f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e04f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e04f-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-103">Creates a resource.</span></span>

## <span data-ttu-id="1e04f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e04f-104">SYNTAX</span></span>

### <span data-ttu-id="1e04f-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1e04f-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e04f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="1e04f-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e04f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="1e04f-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e04f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e04f-108">DESCRIPTION</span></span>
<span data-ttu-id="1e04f-109">O cmdlet **New-AzResource** cria um recurso do Azure, como um site, um servidor de banco de dados SQL do Azure ou um banco de dados SQL do Azure, em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e04f-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="1e04f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e04f-110">EXAMPLES</span></span>

### <span data-ttu-id="1e04f-111">Exemplo 1: Criar um recurso</span><span class="sxs-lookup"><span data-stu-id="1e04f-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="1e04f-112">Esse comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1e04f-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="1e04f-113">Exemplo 2: Criar um recurso usando aplatação</span><span class="sxs-lookup"><span data-stu-id="1e04f-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="1e04f-114">Esse comando cria um recurso que é um site no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1e04f-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="1e04f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e04f-115">PARAMETERS</span></span>

### <span data-ttu-id="1e04f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e04f-116">-ApiVersion</span></span>
<span data-ttu-id="1e04f-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1e04f-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="1e04f-118">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="1e04f-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1e04f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e04f-119">-AsJob</span></span>
<span data-ttu-id="1e04f-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1e04f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e04f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e04f-121">-DefaultProfile</span></span>
<span data-ttu-id="1e04f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1e04f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e04f-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="1e04f-123">-ExtensionResourceName</span></span>
<span data-ttu-id="1e04f-124">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="1e04f-125">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="1e04f-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="1e04f-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="1e04f-126">-ExtensionResourceType</span></span>
<span data-ttu-id="1e04f-127">Especifica o tipo de recurso de um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="1e04f-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="1e04f-128">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="1e04f-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="1e04f-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1e04f-129">-Force</span></span>
<span data-ttu-id="1e04f-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e04f-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e04f-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="1e04f-131">-IsFullObject</span></span>
<span data-ttu-id="1e04f-132">Indica que o objeto especificado pelo parâmetro *Propriedades* é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="1e04f-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="1e04f-133">-Tipo</span><span class="sxs-lookup"><span data-stu-id="1e04f-133">-Kind</span></span>
<span data-ttu-id="1e04f-134">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="1e04f-135">-Local</span><span class="sxs-lookup"><span data-stu-id="1e04f-135">-Location</span></span>
<span data-ttu-id="1e04f-136">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="1e04f-137">Especifique a localização do data center, como o Centro dos EUA ou o Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="1e04f-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="1e04f-138">Você pode colocar um recurso em qualquer local que suporte recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="1e04f-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="1e04f-139">Os grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="1e04f-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="1e04f-140">Para determinar quais locais suportam cada tipo de recurso, use Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e04f-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="1e04f-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1e04f-141">-ODataQuery</span></span>
<span data-ttu-id="1e04f-142">Especifica um filtro de estilo OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="1e04f-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="1e04f-143">Esse cmdlet anexa esse valor à solicitação além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="1e04f-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="1e04f-144">-Plano</span><span class="sxs-lookup"><span data-stu-id="1e04f-144">-Plan</span></span>
<span data-ttu-id="1e04f-145">Uma tabela hash que representa propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="1e04f-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="1e04f-146">-Pré-</span><span class="sxs-lookup"><span data-stu-id="1e04f-146">-Pre</span></span>
<span data-ttu-id="1e04f-147">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1e04f-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1e04f-148">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e04f-148">-Properties</span></span>
<span data-ttu-id="1e04f-149">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="1e04f-150">Use este parâmetro para especificar os valores de propriedades específicos de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="1e04f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e04f-151">-ResourceGroupName</span></span>
<span data-ttu-id="1e04f-152">Especifica o nome do grupo de recursos onde esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="1e04f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e04f-153">-ResourceId</span></span>
<span data-ttu-id="1e04f-154">Especifica a ID de recurso totalmente qualificada, incluindo a assinatura, como no exemplo a `/subscriptions/` seguir: ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1e04f-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="1e04f-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1e04f-155">-ResourceName</span></span>
<span data-ttu-id="1e04f-156">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-156">Specifies the name of the resource.</span></span> <span data-ttu-id="1e04f-157">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1e04f-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="1e04f-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1e04f-158">-ResourceType</span></span>
<span data-ttu-id="1e04f-159">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="1e04f-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="1e04f-160">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="1e04f-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="1e04f-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="1e04f-161">-Sku</span></span>
<span data-ttu-id="1e04f-162">Uma tabela hash que representa propriedades de sku.</span><span class="sxs-lookup"><span data-stu-id="1e04f-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="1e04f-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="1e04f-163">-Tag</span></span>
<span data-ttu-id="1e04f-164">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1e04f-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e04f-165">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1e04f-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1e04f-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1e04f-166">-TenantLevel</span></span>
<span data-ttu-id="1e04f-167">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="1e04f-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="1e04f-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1e04f-168">-Confirm</span></span>
<span data-ttu-id="1e04f-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e04f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e04f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e04f-170">-WhatIf</span></span>
<span data-ttu-id="1e04f-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1e04f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e04f-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e04f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e04f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e04f-173">CommonParameters</span></span>
<span data-ttu-id="1e04f-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e04f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e04f-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e04f-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e04f-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e04f-176">INPUTS</span></span>

### <span data-ttu-id="1e04f-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1e04f-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1e04f-178">System.String</span><span class="sxs-lookup"><span data-stu-id="1e04f-178">System.String</span></span>

## <span data-ttu-id="1e04f-179">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e04f-179">OUTPUTS</span></span>

### <span data-ttu-id="1e04f-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="1e04f-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1e04f-181">Notas</span><span class="sxs-lookup"><span data-stu-id="1e04f-181">NOTES</span></span>

## <span data-ttu-id="1e04f-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e04f-182">RELATED LINKS</span></span>

[<span data-ttu-id="1e04f-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e04f-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="1e04f-184">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e04f-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="1e04f-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e04f-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="1e04f-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="1e04f-186">Set-AzResource</span></span>](./Set-AzResource.md)
