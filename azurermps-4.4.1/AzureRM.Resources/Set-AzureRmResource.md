---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610176"
---
# <span data-ttu-id="a52ad-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="a52ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a52ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a52ad-103">Modifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a52ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a52ad-104">SYNTAX</span></span>

### <span data-ttu-id="a52ad-105">A ID do recurso. (padrão)</span><span class="sxs-lookup"><span data-stu-id="a52ad-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a52ad-106">Recurso que reside no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="a52ad-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a52ad-107">Recurso que reside no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="a52ad-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a52ad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a52ad-108">DESCRIPTION</span></span>
<span data-ttu-id="a52ad-109">O cmdlet **set-AzureRmResource** modifica um recurso existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="a52ad-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="a52ad-110">Especifique um recurso a ser modificado por nome e tipo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="a52ad-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="a52ad-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a52ad-111">EXAMPLES</span></span>

### <span data-ttu-id="a52ad-112">Exemplo 1: modificar um recurso</span><span class="sxs-lookup"><span data-stu-id="a52ad-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="a52ad-113">O primeiro comando obtém o recurso denominado ContosoSite usando o cmdlet Get-AzureRmResource e, em seguida, armazena-o na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="a52ad-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="a52ad-114">O segundo comando modifica uma propriedade de $Resource.</span><span class="sxs-lookup"><span data-stu-id="a52ad-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="a52ad-115">O comando final atualiza o recurso para corresponder ao $Resource.</span><span class="sxs-lookup"><span data-stu-id="a52ad-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="a52ad-116">OS</span><span class="sxs-lookup"><span data-stu-id="a52ad-116">PARAMETERS</span></span>

### <span data-ttu-id="a52ad-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a52ad-117">-ApiVersion</span></span>
<span data-ttu-id="a52ad-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a52ad-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a52ad-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a52ad-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a52ad-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a52ad-120">-ExtensionResourceName</span></span>
<span data-ttu-id="a52ad-121">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="a52ad-122">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a52ad-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="a52ad-123">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="a52ad-123">server name`/`database name</span></span>

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

### <span data-ttu-id="a52ad-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a52ad-124">-ExtensionResourceType</span></span>
<span data-ttu-id="a52ad-125">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="a52ad-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a52ad-126">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a52ad-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="a52ad-127">-Force</span><span class="sxs-lookup"><span data-stu-id="a52ad-127">-Force</span></span>
<span data-ttu-id="a52ad-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a52ad-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a52ad-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="a52ad-129">-Kind</span></span>
<span data-ttu-id="a52ad-130">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a52ad-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a52ad-131">-ODataQuery</span></span>
<span data-ttu-id="a52ad-132">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a52ad-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="a52ad-133">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="a52ad-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a52ad-134">-Plano</span><span class="sxs-lookup"><span data-stu-id="a52ad-134">-Plan</span></span>
<span data-ttu-id="a52ad-135">Especifica as propriedades do plano de recursos, como uma tabela de hash, para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="a52ad-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="a52ad-136">-Pre</span></span>
<span data-ttu-id="a52ad-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a52ad-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a52ad-138">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="a52ad-138">-Properties</span></span>
<span data-ttu-id="a52ad-139">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="a52ad-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52ad-140">-ResourceGroupName</span></span>
<span data-ttu-id="a52ad-141">Especifica o nome do grupo de recursos em que esse cmdlet modifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="a52ad-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a52ad-142">-ResourceId</span></span>
<span data-ttu-id="a52ad-143">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a52ad-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="a52ad-144">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a52ad-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a52ad-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a52ad-145">-ResourceName</span></span>
<span data-ttu-id="a52ad-146">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="a52ad-147">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="a52ad-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="a52ad-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a52ad-148">-ResourceType</span></span>
<span data-ttu-id="a52ad-149">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="a52ad-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="a52ad-150">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a52ad-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="a52ad-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="a52ad-151">-Sku</span></span>
<span data-ttu-id="a52ad-152">Especifica o objeto SKU do recurso como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a52ad-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="a52ad-153">-Marca</span><span class="sxs-lookup"><span data-stu-id="a52ad-153">-Tag</span></span>
<span data-ttu-id="a52ad-154">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a52ad-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a52ad-155">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="a52ad-155">For example:</span></span>

<span data-ttu-id="a52ad-156">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a52ad-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a52ad-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a52ad-157">-TenantLevel</span></span>
<span data-ttu-id="a52ad-158">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="a52ad-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a52ad-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="a52ad-159">-UsePatchSemantics</span></span>
<span data-ttu-id="a52ad-160">Indica que esse cmdlet usa um PATCH HTTP para atualizar o objeto, em vez de um HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="a52ad-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="a52ad-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a52ad-161">-Confirm</span></span>
<span data-ttu-id="a52ad-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52ad-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52ad-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52ad-163">-WhatIf</span></span>
<span data-ttu-id="a52ad-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a52ad-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52ad-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a52ad-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52ad-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52ad-166">-DefaultProfile</span></span>
<span data-ttu-id="a52ad-167">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a52ad-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a52ad-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52ad-168">CommonParameters</span></span>
<span data-ttu-id="a52ad-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52ad-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52ad-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52ad-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52ad-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a52ad-171">INPUTS</span></span>

## <span data-ttu-id="a52ad-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a52ad-172">OUTPUTS</span></span>

### <span data-ttu-id="a52ad-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a52ad-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a52ad-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a52ad-174">NOTES</span></span>

## <span data-ttu-id="a52ad-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a52ad-175">RELATED LINKS</span></span>

[<span data-ttu-id="a52ad-176">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="a52ad-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="a52ad-178">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="a52ad-179">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a52ad-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a52ad-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
