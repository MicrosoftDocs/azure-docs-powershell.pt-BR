---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 01e4e6b990a35b8573a9ea1d2f2803f6d6fabc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432585"
---
# <span data-ttu-id="9683a-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="9683a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9683a-102">SYNOPSIS</span></span>
<span data-ttu-id="9683a-103">Obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="9683a-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9683a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9683a-104">SYNTAX</span></span>

### <span data-ttu-id="9683a-105">O conjunto de parâmetros lista todos os recursos.</span><span class="sxs-lookup"><span data-stu-id="9683a-105">The list all resources parameter set.</span></span> <span data-ttu-id="9683a-106">Assume</span><span class="sxs-lookup"><span data-stu-id="9683a-106">(Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-107">Obter um único recurso pela ID.</span><span class="sxs-lookup"><span data-stu-id="9683a-107">Get a single resource by its Id.</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-108">Obter um único recurso no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="9683a-108">Get a single resource at the tenant level.</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-109">Lista os recursos com base no escopo especificado no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="9683a-109">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-110">Obter recurso por nome e grupo</span><span class="sxs-lookup"><span data-stu-id="9683a-110">Get resource by name and group</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9683a-111">Obter um recurso por nome e tipo.</span><span class="sxs-lookup"><span data-stu-id="9683a-111">Get a resource by name and type.</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-112">Obter recurso por nome, grupo e tipo</span><span class="sxs-lookup"><span data-stu-id="9683a-112">Get resource by name, group and type</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9683a-113">Obter coleta de recursos</span><span class="sxs-lookup"><span data-stu-id="9683a-113">Get resource collection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9683a-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9683a-114">DESCRIPTION</span></span>
<span data-ttu-id="9683a-115">O cmdlet **Get-AzureRmResource** Obtém os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9683a-115">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="9683a-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9683a-116">EXAMPLES</span></span>

### <span data-ttu-id="9683a-117">Exemplo 1: obter um recurso</span><span class="sxs-lookup"><span data-stu-id="9683a-117">Example 1: Get a resource</span></span>
```
PS C:\>Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoWebsite"
```

<span data-ttu-id="9683a-118">Esse comando obtém um recurso do tipo Microsoft. Web/sites, chamado ContosoWebsite em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9683a-118">This command gets a resource of the type microsoft.web/sites, named ContosoWebsite under ResourceGroup11.</span></span>

## <span data-ttu-id="9683a-119">OS</span><span class="sxs-lookup"><span data-stu-id="9683a-119">PARAMETERS</span></span>

### <span data-ttu-id="9683a-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9683a-120">-ApiVersion</span></span>
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

### <span data-ttu-id="9683a-121">-Expandproperties</span><span class="sxs-lookup"><span data-stu-id="9683a-121">-ExpandProperties</span></span>
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

### <span data-ttu-id="9683a-122">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9683a-122">-ExtensionResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9683a-123">-ExtensionResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource by name, group and type
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-124">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="9683a-124">-IsCollection</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type., Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-125">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9683a-125">-ODataQuery</span></span>
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

### <span data-ttu-id="9683a-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="9683a-126">-Pre</span></span>
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

### <span data-ttu-id="9683a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9683a-127">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Get resource by name and group
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9683a-128">-ResourceId</span></span>
<span data-ttu-id="9683a-129">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9683a-129">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="9683a-130">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9683a-130">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="9683a-131">Esse cmdlet obtém o recurso que tem essa ID.</span><span class="sxs-lookup"><span data-stu-id="9683a-131">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a single resource by its Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9683a-132">-ResourceName</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get resource by name and group, Get a resource by name and type.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9683a-133">-ResourceType</span></span>
```yaml
Type: System.String
Parameter Sets: Get a single resource at the tenant level., Get resource by name, group and type
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resource by name and type.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Get resource collection
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-134">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9683a-134">-TenantLevel</span></span>
<span data-ttu-id="9683a-135">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="9683a-135">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get a single resource at the tenant level., Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-136">-Início</span><span class="sxs-lookup"><span data-stu-id="9683a-136">-Top</span></span>
```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9683a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9683a-137">-DefaultProfile</span></span>
<span data-ttu-id="9683a-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9683a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9683a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9683a-139">CommonParameters</span></span>
<span data-ttu-id="9683a-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9683a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9683a-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9683a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9683a-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9683a-142">INPUTS</span></span>

## <span data-ttu-id="9683a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9683a-143">OUTPUTS</span></span>

### <span data-ttu-id="9683a-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9683a-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9683a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9683a-145">NOTES</span></span>

## <span data-ttu-id="9683a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9683a-146">RELATED LINKS</span></span>

[<span data-ttu-id="9683a-147">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-147">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9683a-148">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-148">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9683a-149">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-149">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9683a-150">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-150">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="9683a-151">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9683a-151">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


