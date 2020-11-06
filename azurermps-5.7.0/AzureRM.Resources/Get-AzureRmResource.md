---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429689"
---
# <span data-ttu-id="a9d64-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="a9d64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9d64-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d64-103">Obtém recursos.</span><span class="sxs-lookup"><span data-stu-id="a9d64-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9d64-104">SYNTAX</span></span>

### <span data-ttu-id="a9d64-105">GetAllResources (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9d64-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d64-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a9d64-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a9d64-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="a9d64-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d64-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="a9d64-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="a9d64-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9d64-112">Getresourcecollection</span><span class="sxs-lookup"><span data-stu-id="a9d64-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9d64-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9d64-113">DESCRIPTION</span></span>
<span data-ttu-id="a9d64-114">O cmdlet **Get-AzureRmResource** Obtém os recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d64-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="a9d64-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9d64-115">EXAMPLES</span></span>

### <span data-ttu-id="a9d64-116">Exemplo 1: obter todos os recursos de um tipo específico</span><span class="sxs-lookup"><span data-stu-id="a9d64-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="a9d64-117">Esse comando obtém um recurso do tipo Microsoft. Web/sites em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a9d64-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="a9d64-118">Exemplo 2: obter um recurso por nome</span><span class="sxs-lookup"><span data-stu-id="a9d64-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="a9d64-119">Esse comando obtém um recurso chamado ContosoWebsite em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a9d64-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="a9d64-120">Exemplo 3: mostrar o status de contas de armazenamento em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a9d64-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="a9d64-121">OS</span><span class="sxs-lookup"><span data-stu-id="a9d64-121">PARAMETERS</span></span>

### <span data-ttu-id="a9d64-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9d64-122">-ApiVersion</span></span>
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

### <span data-ttu-id="a9d64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d64-123">-DefaultProfile</span></span>
<span data-ttu-id="a9d64-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9d64-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9d64-125">-Expandproperties</span><span class="sxs-lookup"><span data-stu-id="a9d64-125">-ExpandProperties</span></span>
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

### <span data-ttu-id="a9d64-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a9d64-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a9d64-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="a9d64-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a9d64-129">-ODataQuery</span></span>
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

### <span data-ttu-id="a9d64-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="a9d64-130">-Pre</span></span>
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

### <span data-ttu-id="a9d64-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d64-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d64-132">-ResourceId</span></span>
<span data-ttu-id="a9d64-133">Especifica a ID de recurso totalmente qualificado, incluindo a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="a9d64-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="a9d64-134">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a9d64-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="a9d64-135">Esse cmdlet obtém o recurso que tem essa ID.</span><span class="sxs-lookup"><span data-stu-id="a9d64-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a9d64-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a9d64-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a9d64-138">-TenantLevel</span></span>
<span data-ttu-id="a9d64-139">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="a9d64-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-140">-Início</span><span class="sxs-lookup"><span data-stu-id="a9d64-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d64-141">CommonParameters</span></span>
<span data-ttu-id="a9d64-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d64-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d64-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d64-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9d64-144">INPUTS</span></span>

### <span data-ttu-id="a9d64-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a9d64-145">None</span></span>
<span data-ttu-id="a9d64-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a9d64-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9d64-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9d64-147">OUTPUTS</span></span>

### <span data-ttu-id="a9d64-148">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a9d64-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a9d64-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9d64-149">NOTES</span></span>

## <span data-ttu-id="a9d64-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9d64-150">RELATED LINKS</span></span>

[<span data-ttu-id="a9d64-151">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="a9d64-152">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="a9d64-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a9d64-154">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="a9d64-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a9d64-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


