---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431636"
---
# <span data-ttu-id="fbed0-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="fbed0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbed0-102">SYNOPSIS</span></span>
<span data-ttu-id="fbed0-103">Pesquisa recursos com base em parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="fbed0-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbed0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbed0-104">SYNTAX</span></span>

### <span data-ttu-id="fbed0-105">GetBySpecifiedScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="fbed0-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fbed0-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fbed0-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fbed0-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="fbed0-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fbed0-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="fbed0-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fbed0-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="fbed0-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fbed0-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbed0-110">DESCRIPTION</span></span>
<span data-ttu-id="fbed0-111">O cmdlet **Find-AzureRmResource** pesquisa recursos com base em parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="fbed0-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="fbed0-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbed0-112">EXAMPLES</span></span>

### <span data-ttu-id="fbed0-113">Exemplo 1: procurar recursos por tipo e nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fbed0-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="fbed0-114">Esse comando pesquisa recursos do tipo Microsoft. Web/sites em grupos de recursos que têm nomes que correspondem à cadeia de caracteres do grupo de fontes.</span><span class="sxs-lookup"><span data-stu-id="fbed0-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="fbed0-115">Exemplo 2: pesquisar recursos por tipo e nome do recurso</span><span class="sxs-lookup"><span data-stu-id="fbed0-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="fbed0-116">Esse comando pesquisa recursos do tipo Microsoft. Web/sites que têm um nome de recurso que corresponda ao teste de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fbed0-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="fbed0-117">OS</span><span class="sxs-lookup"><span data-stu-id="fbed0-117">PARAMETERS</span></span>

### <span data-ttu-id="fbed0-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fbed0-118">-ApiVersion</span></span>
<span data-ttu-id="fbed0-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fbed0-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fbed0-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="fbed0-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fbed0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbed0-121">-DefaultProfile</span></span>
<span data-ttu-id="fbed0-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fbed0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbed0-123">-Expandproperties</span><span class="sxs-lookup"><span data-stu-id="fbed0-123">-ExpandProperties</span></span>
<span data-ttu-id="fbed0-124">Indica que esse cmdlet expande as propriedades do recurso.</span><span class="sxs-lookup"><span data-stu-id="fbed0-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="fbed0-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fbed0-125">-ExtensionResourceType</span></span>
<span data-ttu-id="fbed0-126">Especifica o tipo de recurso de extensão para os recursos para os quais esse cmdlet pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fbed0-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="fbed0-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="fbed0-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-128">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fbed0-128">-InformationAction</span></span>
<span data-ttu-id="fbed0-129">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="fbed0-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fbed0-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fbed0-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbed0-131">Contínuo</span><span class="sxs-lookup"><span data-stu-id="fbed0-131">Continue</span></span>
- <span data-ttu-id="fbed0-132">Ignorar</span><span class="sxs-lookup"><span data-stu-id="fbed0-132">Ignore</span></span>
- <span data-ttu-id="fbed0-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="fbed0-133">Inquire</span></span>
- <span data-ttu-id="fbed0-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fbed0-134">SilentlyContinue</span></span>
- <span data-ttu-id="fbed0-135">Finaliza</span><span class="sxs-lookup"><span data-stu-id="fbed0-135">Stop</span></span>
- <span data-ttu-id="fbed0-136">Suspensão</span><span class="sxs-lookup"><span data-stu-id="fbed0-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fbed0-137">-InformationVariable</span></span>
<span data-ttu-id="fbed0-138">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="fbed0-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fbed0-139">-ODataQuery</span></span>
<span data-ttu-id="fbed0-140">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fbed0-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="fbed0-141">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="fbed0-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="fbed0-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="fbed0-142">-Pre</span></span>
<span data-ttu-id="fbed0-143">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fbed0-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fbed0-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="fbed0-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="fbed0-145">Especifica um nome parcial de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbed0-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="fbed0-146">Este cmdlet corresponde a grupos de recursos dos quais esse valor é uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fbed0-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="fbed0-147">O cmdlet pesquisa recursos nesses grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="fbed0-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="fbed0-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="fbed0-149">O nome do grupo de recursos para uma correspondência completa.</span><span class="sxs-lookup"><span data-stu-id="fbed0-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="fbed0-150">-ResourceNameContains</span></span>
<span data-ttu-id="fbed0-151">Especifica um nome parcial de um recurso.</span><span class="sxs-lookup"><span data-stu-id="fbed0-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="fbed0-152">O cmdlet pesquisa recursos que contêm esse valor como uma subcadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fbed0-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="fbed0-153">-ResourceNameEquals</span></span>
<span data-ttu-id="fbed0-154">O nome do recurso para uma correspondência completa.</span><span class="sxs-lookup"><span data-stu-id="fbed0-154">The resource name for a full match.</span></span> <span data-ttu-id="fbed0-155">por exemplo, se o nome do recurso for testResource, você poderá especificar testResource.</span><span class="sxs-lookup"><span data-stu-id="fbed0-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fbed0-156">-ResourceType</span></span>
<span data-ttu-id="fbed0-157">Especifica o tipo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="fbed0-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="fbed0-158">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fbed0-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="fbed0-159">Este cmdlet procura recursos do tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="fbed0-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-160">-Marca</span><span class="sxs-lookup"><span data-stu-id="fbed0-160">-Tag</span></span>
<span data-ttu-id="fbed0-161">O filtro de marca para a consulta OData.</span><span class="sxs-lookup"><span data-stu-id="fbed0-161">The tag filter for the OData query.</span></span> <span data-ttu-id="fbed0-162">O formato esperado é @ {tagName = $null} ou @ {tagName = ' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="fbed0-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="fbed0-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="fbed0-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fbed0-165">-TenantLevel</span></span>
<span data-ttu-id="fbed0-166">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="fbed0-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-167">-Início</span><span class="sxs-lookup"><span data-stu-id="fbed0-167">-Top</span></span>
<span data-ttu-id="fbed0-168">Especifica o número de recursos a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="fbed0-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbed0-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbed0-169">CommonParameters</span></span>
<span data-ttu-id="fbed0-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbed0-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbed0-171">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbed0-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbed0-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbed0-172">INPUTS</span></span>

### <span data-ttu-id="fbed0-173">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fbed0-173">None</span></span>
<span data-ttu-id="fbed0-174">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="fbed0-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbed0-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbed0-175">OUTPUTS</span></span>

### <span data-ttu-id="fbed0-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fbed0-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fbed0-177">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbed0-177">NOTES</span></span>

## <span data-ttu-id="fbed0-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbed0-178">RELATED LINKS</span></span>

[<span data-ttu-id="fbed0-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fbed0-180">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fbed0-181">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fbed0-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="fbed0-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fbed0-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
