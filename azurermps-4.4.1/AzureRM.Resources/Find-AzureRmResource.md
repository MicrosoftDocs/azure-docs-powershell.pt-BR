---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429130"
---
# <span data-ttu-id="8667b-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="8667b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8667b-102">SYNOPSIS</span></span>
<span data-ttu-id="8667b-103">Pesquisa recursos com base em parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="8667b-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8667b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8667b-104">SYNTAX</span></span>

### <span data-ttu-id="8667b-105">Lista os recursos com base no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="8667b-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="8667b-106">Assume</span><span class="sxs-lookup"><span data-stu-id="8667b-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8667b-107">Lista os recursos com base no escopo especificado no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="8667b-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8667b-108">Obter recursos usando uma consulta de várias assinaturas.</span><span class="sxs-lookup"><span data-stu-id="8667b-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8667b-109">Lista os recursos por um objeto de marca especificado como um HashSet.</span><span class="sxs-lookup"><span data-stu-id="8667b-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8667b-110">Lista os recursos por uma marca especificada como um nome individual e parâmetros de valor.</span><span class="sxs-lookup"><span data-stu-id="8667b-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8667b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8667b-111">DESCRIPTION</span></span>
<span data-ttu-id="8667b-112">O cmdlet **Find-AzureRmResource** pesquisa recursos com base em parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="8667b-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="8667b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8667b-113">EXAMPLES</span></span>

### <span data-ttu-id="8667b-114">Exemplo 1: procurar recursos por tipo e nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8667b-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="8667b-115">Esse comando pesquisa recursos do tipo Microsoft. Web/sites em grupos de recursos que têm nomes que correspondem à cadeia de caracteres do grupo de fontes.</span><span class="sxs-lookup"><span data-stu-id="8667b-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="8667b-116">Exemplo 2: pesquisar recursos por tipo e nome do recurso</span><span class="sxs-lookup"><span data-stu-id="8667b-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="8667b-117">Esse comando pesquisa recursos do tipo Microsoft. Web/sites que têm um nome de recurso que corresponda ao teste de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8667b-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="8667b-118">OS</span><span class="sxs-lookup"><span data-stu-id="8667b-118">PARAMETERS</span></span>

### <span data-ttu-id="8667b-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8667b-119">-ApiVersion</span></span>
<span data-ttu-id="8667b-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8667b-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8667b-121">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8667b-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8667b-122">-Expandproperties</span><span class="sxs-lookup"><span data-stu-id="8667b-122">-ExpandProperties</span></span>
<span data-ttu-id="8667b-123">Indica que esse cmdlet expande as propriedades do recurso.</span><span class="sxs-lookup"><span data-stu-id="8667b-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="8667b-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8667b-124">-ExtensionResourceType</span></span>
<span data-ttu-id="8667b-125">Especifica o tipo de recurso de extensão para os recursos para os quais esse cmdlet pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8667b-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="8667b-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8667b-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8667b-127">-InformationAction</span></span>
<span data-ttu-id="8667b-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8667b-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8667b-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8667b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8667b-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8667b-130">Continue</span></span>
- <span data-ttu-id="8667b-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8667b-131">Ignore</span></span>
- <span data-ttu-id="8667b-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="8667b-132">Inquire</span></span>
- <span data-ttu-id="8667b-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8667b-133">SilentlyContinue</span></span>
- <span data-ttu-id="8667b-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8667b-134">Stop</span></span>
- <span data-ttu-id="8667b-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8667b-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8667b-136">-InformationVariable</span></span>
<span data-ttu-id="8667b-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8667b-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8667b-138">-ODataQuery</span></span>
<span data-ttu-id="8667b-139">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8667b-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8667b-140">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="8667b-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8667b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8667b-141">-Pre</span></span>
<span data-ttu-id="8667b-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8667b-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8667b-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="8667b-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="8667b-144">Especifica um nome parcial de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8667b-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="8667b-145">Este cmdlet corresponde a grupos de recursos dos quais esse valor é uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8667b-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="8667b-146">O cmdlet pesquisa recursos nesses grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="8667b-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="8667b-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="8667b-148">O nome do grupo de recursos para uma correspondência completa.</span><span class="sxs-lookup"><span data-stu-id="8667b-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="8667b-149">-ResourceNameContains</span></span>
<span data-ttu-id="8667b-150">Especifica um nome parcial de um recurso.</span><span class="sxs-lookup"><span data-stu-id="8667b-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="8667b-151">O cmdlet pesquisa recursos que contêm esse valor como uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8667b-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="8667b-152">-ResourceNameEquals</span></span>
<span data-ttu-id="8667b-153">O nome do recurso para uma correspondência completa.</span><span class="sxs-lookup"><span data-stu-id="8667b-153">The resource name for a full match.</span></span> <span data-ttu-id="8667b-154">por exemplo, se o nome do recurso for testResource, você poderá especificar testResource.</span><span class="sxs-lookup"><span data-stu-id="8667b-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8667b-155">-ResourceType</span></span>
<span data-ttu-id="8667b-156">Especifica o tipo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="8667b-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="8667b-157">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8667b-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="8667b-158">Este cmdlet procura recursos do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="8667b-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-159">-Marca</span><span class="sxs-lookup"><span data-stu-id="8667b-159">-Tag</span></span>
<span data-ttu-id="8667b-160">O filtro de marca para a consulta OData.</span><span class="sxs-lookup"><span data-stu-id="8667b-160">The tag filter for the OData query.</span></span> <span data-ttu-id="8667b-161">O formato esperado é @ {tagName = $null} ou @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="8667b-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="8667b-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="8667b-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8667b-164">-TenantLevel</span></span>
<span data-ttu-id="8667b-165">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="8667b-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-166">-Início</span><span class="sxs-lookup"><span data-stu-id="8667b-166">-Top</span></span>
<span data-ttu-id="8667b-167">Especifica o número de recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="8667b-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8667b-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8667b-168">-DefaultProfile</span></span>
<span data-ttu-id="8667b-169">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8667b-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8667b-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8667b-170">CommonParameters</span></span>
<span data-ttu-id="8667b-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8667b-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8667b-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8667b-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8667b-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8667b-173">INPUTS</span></span>

## <span data-ttu-id="8667b-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8667b-174">OUTPUTS</span></span>

### <span data-ttu-id="8667b-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="8667b-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8667b-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8667b-176">NOTES</span></span>

## <span data-ttu-id="8667b-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8667b-177">RELATED LINKS</span></span>

[<span data-ttu-id="8667b-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="8667b-179">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="8667b-180">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8667b-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="8667b-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8667b-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
