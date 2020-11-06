---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433019"
---
# <span data-ttu-id="67aa9-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-101">New-AzureRmResource</span></span>

## <span data-ttu-id="67aa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="67aa9-103">Cria um recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67aa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67aa9-104">SYNTAX</span></span>

### <span data-ttu-id="67aa9-105">A ID do recurso. (padrão)</span><span class="sxs-lookup"><span data-stu-id="67aa9-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67aa9-106">Recurso que reside no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="67aa9-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67aa9-107">Recurso que reside no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="67aa9-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67aa9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67aa9-108">DESCRIPTION</span></span>
<span data-ttu-id="67aa9-109">O cmdlet **New-AzureRmResource** cria um recurso do Azure, como um site, um servidor de banco de dados SQL do Azure ou um banco de dados SQL do Azure em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="67aa9-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="67aa9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67aa9-110">EXAMPLES</span></span>

### <span data-ttu-id="67aa9-111">Exemplo 1: criar um recurso</span><span class="sxs-lookup"><span data-stu-id="67aa9-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="67aa9-112">Esse comando cria um recurso que é um site do ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="67aa9-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="67aa9-113">OS</span><span class="sxs-lookup"><span data-stu-id="67aa9-113">PARAMETERS</span></span>

### <span data-ttu-id="67aa9-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="67aa9-114">-ApiVersion</span></span>
<span data-ttu-id="67aa9-115">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="67aa9-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="67aa9-116">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="67aa9-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="67aa9-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="67aa9-117">-ExtensionResourceName</span></span>
<span data-ttu-id="67aa9-118">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="67aa9-119">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="67aa9-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="67aa9-120">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="67aa9-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="67aa9-121">-ExtensionResourceType</span></span>
<span data-ttu-id="67aa9-122">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="67aa9-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="67aa9-123">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte tipo:</span><span class="sxs-lookup"><span data-stu-id="67aa9-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="67aa9-124">-Force</span></span>
<span data-ttu-id="67aa9-125">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="67aa9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="67aa9-126">-Isfullobject</span><span class="sxs-lookup"><span data-stu-id="67aa9-126">-IsFullObject</span></span>
<span data-ttu-id="67aa9-127">Indica que o objeto que o parâmetro *Properties* especifica é o objeto completo.</span><span class="sxs-lookup"><span data-stu-id="67aa9-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="67aa9-128">-Kind</span><span class="sxs-lookup"><span data-stu-id="67aa9-128">-Kind</span></span>
<span data-ttu-id="67aa9-129">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="67aa9-130">-Local</span><span class="sxs-lookup"><span data-stu-id="67aa9-130">-Location</span></span>
<span data-ttu-id="67aa9-131">Especifica o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="67aa9-132">Especifique o local do Data Center, como central EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="67aa9-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="67aa9-133">Você pode colocar um recurso em qualquer local que ofereça suporte a recursos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="67aa9-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="67aa9-134">Grupos de recursos podem conter recursos de locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="67aa9-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="67aa9-135">Para determinar quais locais dão suporte a cada tipo de recurso, use o cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="67aa9-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="67aa9-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="67aa9-136">-ODataQuery</span></span>
<span data-ttu-id="67aa9-137">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="67aa9-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="67aa9-138">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="67aa9-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="67aa9-139">-Plano</span><span class="sxs-lookup"><span data-stu-id="67aa9-139">-Plan</span></span>
<span data-ttu-id="67aa9-140">Uma tabela de hash que representa as propriedades do plano de recursos.</span><span class="sxs-lookup"><span data-stu-id="67aa9-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="67aa9-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="67aa9-141">-Pre</span></span>
<span data-ttu-id="67aa9-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="67aa9-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="67aa9-143">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="67aa9-143">-Properties</span></span>
<span data-ttu-id="67aa9-144">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="67aa9-145">Use esse parâmetro para especificar os valores das propriedades que são específicas de um tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="67aa9-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67aa9-146">-ResourceGroupName</span></span>
<span data-ttu-id="67aa9-147">Especifica o nome do grupo de recursos em que esse cmdlet cria o recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67aa9-148">-ResourceId</span></span>
<span data-ttu-id="67aa9-149">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="67aa9-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="67aa9-150">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="67aa9-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="67aa9-151">-ResourceName</span></span>
<span data-ttu-id="67aa9-152">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-152">Specifies the name of the resource.</span></span> <span data-ttu-id="67aa9-153">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="67aa9-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="67aa9-154">-ResourceType</span></span>
<span data-ttu-id="67aa9-155">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="67aa9-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="67aa9-156">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="67aa9-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="67aa9-157">-Sku</span></span>
<span data-ttu-id="67aa9-158">Uma tabela de hash que representa as propriedades de SKU.</span><span class="sxs-lookup"><span data-stu-id="67aa9-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="67aa9-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="67aa9-159">-Tag</span></span>
<span data-ttu-id="67aa9-160">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="67aa9-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="67aa9-161">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="67aa9-161">For example:</span></span>

<span data-ttu-id="67aa9-162">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="67aa9-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="67aa9-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="67aa9-163">-TenantLevel</span></span>
<span data-ttu-id="67aa9-164">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="67aa9-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67aa9-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67aa9-165">-Confirm</span></span>
<span data-ttu-id="67aa9-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67aa9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67aa9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67aa9-167">-WhatIf</span></span>
<span data-ttu-id="67aa9-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67aa9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67aa9-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67aa9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67aa9-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67aa9-170">-DefaultProfile</span></span>
<span data-ttu-id="67aa9-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67aa9-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67aa9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67aa9-172">CommonParameters</span></span>
<span data-ttu-id="67aa9-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67aa9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67aa9-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67aa9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67aa9-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67aa9-175">INPUTS</span></span>

## <span data-ttu-id="67aa9-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67aa9-176">OUTPUTS</span></span>

### <span data-ttu-id="67aa9-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="67aa9-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="67aa9-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67aa9-178">NOTES</span></span>

## <span data-ttu-id="67aa9-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67aa9-179">RELATED LINKS</span></span>

[<span data-ttu-id="67aa9-180">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="67aa9-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="67aa9-182">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="67aa9-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="67aa9-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="67aa9-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
