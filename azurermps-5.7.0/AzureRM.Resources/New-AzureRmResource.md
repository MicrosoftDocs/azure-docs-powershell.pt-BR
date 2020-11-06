---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428797"
---
# <span data-ttu-id="fe6d3-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-101">New-AzureRmResource</span></span>

## <span data-ttu-id="fe6d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6d3-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe6d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe6d3-104">SYNTAX</span></span>

### <span data-ttu-id="fe6d3-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe6d3-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe6d3-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fe6d3-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe6d3-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fe6d3-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe6d3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe6d3-108">DESCRIPTION</span></span>
<span data-ttu-id="fe6d3-109">O cmdlet **New-AzureRmResource** cria um recurso do Azure, como um site, um servidor de banco de dados SQL do Azure ou um banco de dados SQL do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="fe6d3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe6d3-110">EXAMPLES</span></span>

### <span data-ttu-id="fe6d3-111">Exemplo 1: criar um recurso</span><span class="sxs-lookup"><span data-stu-id="fe6d3-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="fe6d3-112">Esse comando cria um recurso que é um site do ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="fe6d3-113">Exemplo 2: criar um recurso usando splatting</span><span class="sxs-lookup"><span data-stu-id="fe6d3-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="fe6d3-114">Esse comando cria um recurso que é um site do ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="fe6d3-115">OS</span><span class="sxs-lookup"><span data-stu-id="fe6d3-115">PARAMETERS</span></span>

### <span data-ttu-id="fe6d3-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe6d3-116">-ApiVersion</span></span>
<span data-ttu-id="fe6d3-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="fe6d3-118">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe6d3-119">-AsJob</span></span>
<span data-ttu-id="fe6d3-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fe6d3-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6d3-121">-DefaultProfile</span></span>
<span data-ttu-id="fe6d3-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fe6d3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fe6d3-123">-ExtensionResourceName</span></span>
<span data-ttu-id="fe6d3-124">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="fe6d3-125">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="fe6d3-126">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="fe6d3-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fe6d3-127">-ExtensionResourceType</span></span>
<span data-ttu-id="fe6d3-128">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="fe6d3-129">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fe6d3-130">-Force</span></span>
<span data-ttu-id="fe6d3-131">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-132">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="fe6d3-132">-IsFullObject</span></span>
<span data-ttu-id="fe6d3-133">Indica que o objeto que o parâmetro *Properties* especifica é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-134">-Kind</span><span class="sxs-lookup"><span data-stu-id="fe6d3-134">-Kind</span></span>
<span data-ttu-id="fe6d3-135">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-136">-Local</span><span class="sxs-lookup"><span data-stu-id="fe6d3-136">-Location</span></span>
<span data-ttu-id="fe6d3-137">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="fe6d3-138">Especifique o local do Data Center, como central EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="fe6d3-139">Você pode colocar um recurso em qualquer local que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="fe6d3-140">Grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="fe6d3-141">Para determinar quais locais dão suporte a cada tipo de recurso, use o cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fe6d3-142">-ODataQuery</span></span>
<span data-ttu-id="fe6d3-143">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fe6d3-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="fe6d3-144">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-145">-Plano</span><span class="sxs-lookup"><span data-stu-id="fe6d3-145">-Plan</span></span>
<span data-ttu-id="fe6d3-146">Uma tabela de hash que representa as propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe6d3-147">-Pre</span></span>
<span data-ttu-id="fe6d3-148">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-149">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe6d3-149">-Properties</span></span>
<span data-ttu-id="fe6d3-150">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="fe6d3-151">Use esse parâmetro para especificar os valores das propriedades que são específicas de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6d3-152">-ResourceGroupName</span></span>
<span data-ttu-id="fe6d3-153">Especifica o nome do grupo de recursos em que esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe6d3-154">-ResourceId</span></span>
<span data-ttu-id="fe6d3-155">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="fe6d3-156">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fe6d3-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fe6d3-157">-ResourceName</span></span>
<span data-ttu-id="fe6d3-158">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-158">Specifies the name of the resource.</span></span> <span data-ttu-id="fe6d3-159">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fe6d3-160">-ResourceType</span></span>
<span data-ttu-id="fe6d3-161">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="fe6d3-162">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe6d3-163">-Sku</span></span>
<span data-ttu-id="fe6d3-164">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-165">-Marca</span><span class="sxs-lookup"><span data-stu-id="fe6d3-165">-Tag</span></span>
<span data-ttu-id="fe6d3-166">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe6d3-167">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fe6d3-167">For example:</span></span>

<span data-ttu-id="fe6d3-168">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fe6d3-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fe6d3-169">-TenantLevel</span></span>
<span data-ttu-id="fe6d3-170">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-171">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe6d3-171">-Confirm</span></span>
<span data-ttu-id="fe6d3-172">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe6d3-173">-WhatIf</span></span>
<span data-ttu-id="fe6d3-174">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe6d3-175">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6d3-176">CommonParameters</span></span>
<span data-ttu-id="fe6d3-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6d3-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6d3-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6d3-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe6d3-179">INPUTS</span></span>

### <span data-ttu-id="fe6d3-180">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fe6d3-180">None</span></span>
<span data-ttu-id="fe6d3-181">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe6d3-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe6d3-182">OUTPUTS</span></span>

### <span data-ttu-id="fe6d3-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fe6d3-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fe6d3-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe6d3-184">NOTES</span></span>

## <span data-ttu-id="fe6d3-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe6d3-185">RELATED LINKS</span></span>

[<span data-ttu-id="fe6d3-186">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="fe6d3-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fe6d3-188">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fe6d3-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fe6d3-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fe6d3-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
