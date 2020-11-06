---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: 57e4bd86ad3f5205749579e190960ea4f8e70588
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602093"
---
# <span data-ttu-id="0b15f-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-101">New-AzureRmResource</span></span>

## <span data-ttu-id="0b15f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b15f-102">SYNOPSIS</span></span>
<span data-ttu-id="0b15f-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b15f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b15f-104">SYNTAX</span></span>

### <span data-ttu-id="0b15f-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b15f-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b15f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0b15f-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b15f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0b15f-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b15f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b15f-108">DESCRIPTION</span></span>
<span data-ttu-id="0b15f-109">O cmdlet **New-AzureRmResource** cria um recurso do Azure, como um site, um servidor de banco de dados SQL do Azure ou um banco de dados SQL do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b15f-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="0b15f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b15f-110">EXAMPLES</span></span>

### <span data-ttu-id="0b15f-111">Exemplo 1: criar um recurso</span><span class="sxs-lookup"><span data-stu-id="0b15f-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="0b15f-112">Esse comando cria um recurso que é um site do ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b15f-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="0b15f-113">Exemplo 2: criar um recurso usando splatting</span><span class="sxs-lookup"><span data-stu-id="0b15f-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="0b15f-114">Esse comando cria um recurso que é um site do ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b15f-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="0b15f-115">OS</span><span class="sxs-lookup"><span data-stu-id="0b15f-115">PARAMETERS</span></span>

### <span data-ttu-id="0b15f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b15f-116">-ApiVersion</span></span>
<span data-ttu-id="0b15f-117">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0b15f-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="0b15f-118">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0b15f-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0b15f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b15f-119">-AsJob</span></span>
<span data-ttu-id="0b15f-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0b15f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b15f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b15f-121">-DefaultProfile</span></span>
<span data-ttu-id="0b15f-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0b15f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b15f-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0b15f-123">-ExtensionResourceName</span></span>
<span data-ttu-id="0b15f-124">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="0b15f-125">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="0b15f-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="0b15f-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0b15f-126">-ExtensionResourceType</span></span>
<span data-ttu-id="0b15f-127">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="0b15f-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0b15f-128">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0b15f-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0b15f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0b15f-129">-Force</span></span>
<span data-ttu-id="0b15f-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0b15f-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b15f-131">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="0b15f-131">-IsFullObject</span></span>
<span data-ttu-id="0b15f-132">Indica que o objeto que o parâmetro *Properties* especifica é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="0b15f-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="0b15f-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="0b15f-133">-Kind</span></span>
<span data-ttu-id="0b15f-134">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="0b15f-135">-Local</span><span class="sxs-lookup"><span data-stu-id="0b15f-135">-Location</span></span>
<span data-ttu-id="0b15f-136">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="0b15f-137">Especifique o local do Data Center, como central EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="0b15f-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="0b15f-138">Você pode colocar um recurso em qualquer local que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="0b15f-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="0b15f-139">Grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="0b15f-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="0b15f-140">Para determinar quais locais dão suporte a cada tipo de recurso, use o cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="0b15f-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="0b15f-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0b15f-141">-ODataQuery</span></span>
<span data-ttu-id="0b15f-142">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0b15f-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="0b15f-143">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="0b15f-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0b15f-144">-Plano</span><span class="sxs-lookup"><span data-stu-id="0b15f-144">-Plan</span></span>
<span data-ttu-id="0b15f-145">Uma tabela de hash que representa as propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b15f-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="0b15f-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b15f-146">-Pre</span></span>
<span data-ttu-id="0b15f-147">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0b15f-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0b15f-148">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="0b15f-148">-Properties</span></span>
<span data-ttu-id="0b15f-149">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="0b15f-150">Use esse parâmetro para especificar os valores das propriedades que são específicas de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="0b15f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b15f-151">-ResourceGroupName</span></span>
<span data-ttu-id="0b15f-152">Especifica o nome do grupo de recursos em que esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="0b15f-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b15f-153">-ResourceId</span></span>
<span data-ttu-id="0b15f-154">Especifica a ID do recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0b15f-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0b15f-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0b15f-155">-ResourceName</span></span>
<span data-ttu-id="0b15f-156">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-156">Specifies the name of the resource.</span></span> <span data-ttu-id="0b15f-157">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0b15f-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0b15f-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0b15f-158">-ResourceType</span></span>
<span data-ttu-id="0b15f-159">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="0b15f-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="0b15f-160">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0b15f-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0b15f-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b15f-161">-Sku</span></span>
<span data-ttu-id="0b15f-162">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="0b15f-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="0b15f-163">-Marca</span><span class="sxs-lookup"><span data-stu-id="0b15f-163">-Tag</span></span>
<span data-ttu-id="0b15f-164">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0b15f-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b15f-165">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0b15f-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0b15f-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0b15f-166">-TenantLevel</span></span>
<span data-ttu-id="0b15f-167">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="0b15f-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0b15f-168">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b15f-168">-Confirm</span></span>
<span data-ttu-id="0b15f-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b15f-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b15f-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b15f-170">-WhatIf</span></span>
<span data-ttu-id="0b15f-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b15f-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b15f-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b15f-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b15f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b15f-173">CommonParameters</span></span>
<span data-ttu-id="0b15f-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b15f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b15f-175">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b15f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b15f-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b15f-176">INPUTS</span></span>

### <span data-ttu-id="0b15f-177">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0b15f-177">None</span></span>

## <span data-ttu-id="0b15f-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b15f-178">OUTPUTS</span></span>

### <span data-ttu-id="0b15f-179">Microsoft. Azure. Commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="0b15f-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b15f-180">NOTES</span></span>

## <span data-ttu-id="0b15f-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b15f-181">RELATED LINKS</span></span>

[<span data-ttu-id="0b15f-182">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-182">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0b15f-183">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-183">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0b15f-184">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-184">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="0b15f-185">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-185">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="0b15f-186">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0b15f-186">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
