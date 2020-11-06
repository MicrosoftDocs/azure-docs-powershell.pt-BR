---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609942"
---
# <span data-ttu-id="317e4-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="317e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="317e4-102">SYNOPSIS</span></span>
<span data-ttu-id="317e4-103">Modifica um recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="317e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="317e4-104">SYNTAX</span></span>

### <span data-ttu-id="317e4-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="317e4-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="317e4-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="317e4-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="317e4-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="317e4-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="317e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="317e4-108">DESCRIPTION</span></span>
<span data-ttu-id="317e4-109">O cmdlet **set-AzureRmResource** modifica um recurso existente do Azure.</span><span class="sxs-lookup"><span data-stu-id="317e4-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="317e4-110">Especifique um recurso a ser modificado por nome e tipo ou por ID.</span><span class="sxs-lookup"><span data-stu-id="317e4-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="317e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="317e4-111">EXAMPLES</span></span>

### <span data-ttu-id="317e4-112">Exemplo 1: modificar um recurso</span><span class="sxs-lookup"><span data-stu-id="317e4-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="317e4-113">O primeiro comando obtém o recurso denominado ContosoSite usando o cmdlet Get-AzureRmResource e, em seguida, armazena-o na variável $Resource.</span><span class="sxs-lookup"><span data-stu-id="317e4-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="317e4-114">O segundo comando modifica uma propriedade de $Resource.</span><span class="sxs-lookup"><span data-stu-id="317e4-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="317e4-115">O comando final atualiza o recurso para corresponder ao $Resource.</span><span class="sxs-lookup"><span data-stu-id="317e4-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="317e4-116">OS</span><span class="sxs-lookup"><span data-stu-id="317e4-116">PARAMETERS</span></span>

### <span data-ttu-id="317e4-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="317e4-117">-ApiVersion</span></span>
<span data-ttu-id="317e4-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="317e4-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="317e4-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="317e4-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="317e4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="317e4-120">-AsJob</span></span>
<span data-ttu-id="317e4-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="317e4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="317e4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317e4-122">-DefaultProfile</span></span>
<span data-ttu-id="317e4-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="317e4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="317e4-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="317e4-124">-ExtensionResourceName</span></span>
<span data-ttu-id="317e4-125">Especifica o nome de um recurso de extensão para o recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="317e4-126">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="317e4-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="317e4-127">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="317e4-127">server name`/`database name</span></span>

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

### <span data-ttu-id="317e4-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="317e4-128">-ExtensionResourceType</span></span>
<span data-ttu-id="317e4-129">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="317e4-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="317e4-130">Por exemplo, se o recurso de extensão for um banco de dados, especifique o seguinte:</span><span class="sxs-lookup"><span data-stu-id="317e4-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="317e4-131">-Force</span><span class="sxs-lookup"><span data-stu-id="317e4-131">-Force</span></span>
<span data-ttu-id="317e4-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="317e4-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="317e4-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="317e4-133">-Kind</span></span>
<span data-ttu-id="317e4-134">Especifica o tipo de recurso do recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e4-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="317e4-135">-ODataQuery</span></span>
<span data-ttu-id="317e4-136">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="317e4-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="317e4-137">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="317e4-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="317e4-138">-Plano</span><span class="sxs-lookup"><span data-stu-id="317e4-138">-Plan</span></span>
<span data-ttu-id="317e4-139">Especifica as propriedades do plano de recursos, como uma tabela de hash, para o recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e4-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="317e4-140">-Pre</span></span>
<span data-ttu-id="317e4-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="317e4-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="317e4-142">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="317e4-142">-Properties</span></span>
<span data-ttu-id="317e4-143">Especifica as propriedades do recurso para o recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e4-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317e4-144">-ResourceGroupName</span></span>
<span data-ttu-id="317e4-145">Especifica o nome do grupo de recursos em que esse cmdlet modifica o recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="317e4-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="317e4-146">-ResourceId</span></span>
<span data-ttu-id="317e4-147">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="317e4-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="317e4-148">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="317e4-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="317e4-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="317e4-149">-ResourceName</span></span>
<span data-ttu-id="317e4-150">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="317e4-151">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="317e4-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="317e4-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="317e4-152">-ResourceType</span></span>
<span data-ttu-id="317e4-153">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="317e4-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="317e4-154">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="317e4-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="317e4-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="317e4-155">-Sku</span></span>
<span data-ttu-id="317e4-156">Especifica o objeto SKU do recurso como uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="317e4-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="317e4-157">-Marca</span><span class="sxs-lookup"><span data-stu-id="317e4-157">-Tag</span></span>
<span data-ttu-id="317e4-158">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="317e4-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="317e4-159">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="317e4-159">For example:</span></span>

<span data-ttu-id="317e4-160">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="317e4-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317e4-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="317e4-161">-TenantLevel</span></span>
<span data-ttu-id="317e4-162">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="317e4-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="317e4-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="317e4-163">-UsePatchSemantics</span></span>
<span data-ttu-id="317e4-164">Indica que esse cmdlet usa um PATCH HTTP para atualizar o objeto, em vez de um HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="317e4-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="317e4-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="317e4-165">-Confirm</span></span>
<span data-ttu-id="317e4-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="317e4-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="317e4-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="317e4-167">-WhatIf</span></span>
<span data-ttu-id="317e4-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="317e4-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="317e4-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="317e4-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="317e4-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317e4-170">CommonParameters</span></span>
<span data-ttu-id="317e4-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="317e4-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317e4-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317e4-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317e4-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="317e4-173">INPUTS</span></span>

### <span data-ttu-id="317e4-174">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="317e4-174">None</span></span>
<span data-ttu-id="317e4-175">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="317e4-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="317e4-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="317e4-176">OUTPUTS</span></span>

### <span data-ttu-id="317e4-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="317e4-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="317e4-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="317e4-178">NOTES</span></span>

## <span data-ttu-id="317e4-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="317e4-179">RELATED LINKS</span></span>

[<span data-ttu-id="317e4-180">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="317e4-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="317e4-182">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="317e4-183">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="317e4-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="317e4-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
