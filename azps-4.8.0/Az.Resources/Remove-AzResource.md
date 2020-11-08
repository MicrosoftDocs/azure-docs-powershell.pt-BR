---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ecd70916f1ddb6e365fb9f880db9974f6c9ae771
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110946"
---
# <span data-ttu-id="aa188-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-101">Remove-AzResource</span></span>

## <span data-ttu-id="aa188-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa188-102">SYNOPSIS</span></span>
<span data-ttu-id="aa188-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="aa188-103">Removes a resource.</span></span>

## <span data-ttu-id="aa188-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa188-104">SYNTAX</span></span>

### <span data-ttu-id="aa188-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa188-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa188-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="aa188-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa188-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa188-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa188-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa188-108">DESCRIPTION</span></span>
<span data-ttu-id="aa188-109">O cmdlet **Remove-AzResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="aa188-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="aa188-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa188-110">EXAMPLES</span></span>

### <span data-ttu-id="aa188-111">Exemplo 1: remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="aa188-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="aa188-112">Esse comando Remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="aa188-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="aa188-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="aa188-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="aa188-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="aa188-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="aa188-115">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="aa188-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="aa188-116">OS</span><span class="sxs-lookup"><span data-stu-id="aa188-116">PARAMETERS</span></span>

### <span data-ttu-id="aa188-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa188-117">-ApiVersion</span></span>
<span data-ttu-id="aa188-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="aa188-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aa188-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="aa188-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aa188-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa188-120">-AsJob</span></span>
<span data-ttu-id="aa188-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="aa188-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa188-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa188-122">-DefaultProfile</span></span>
<span data-ttu-id="aa188-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="aa188-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa188-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="aa188-124">-ExtensionResourceName</span></span>
<span data-ttu-id="aa188-125">Especifica o nome de um recurso de extensão do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="aa188-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="aa188-126">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="aa188-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="aa188-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="aa188-127">-ExtensionResourceType</span></span>
<span data-ttu-id="aa188-128">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="aa188-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="aa188-129">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="aa188-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="aa188-130">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa188-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa188-131">-Force</span><span class="sxs-lookup"><span data-stu-id="aa188-131">-Force</span></span>
<span data-ttu-id="aa188-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa188-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa188-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="aa188-133">-ODataQuery</span></span>
<span data-ttu-id="aa188-134">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="aa188-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="aa188-135">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="aa188-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="aa188-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa188-136">-Pre</span></span>
<span data-ttu-id="aa188-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="aa188-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aa188-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa188-138">-ResourceGroupName</span></span>
<span data-ttu-id="aa188-139">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="aa188-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="aa188-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa188-140">-ResourceId</span></span>
<span data-ttu-id="aa188-141">Especifica a ID de recurso totalmente qualificado do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="aa188-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="aa188-142">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa188-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa188-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aa188-143">-ResourceName</span></span>
<span data-ttu-id="aa188-144">Especifica o nome do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="aa188-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="aa188-145">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa188-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa188-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aa188-146">-ResourceType</span></span>
<span data-ttu-id="aa188-147">Especifica o tipo do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="aa188-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="aa188-148">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa188-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa188-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa188-149">-TenantLevel</span></span>
<span data-ttu-id="aa188-150">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="aa188-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="aa188-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa188-151">-Confirm</span></span>
<span data-ttu-id="aa188-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa188-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa188-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa188-153">-WhatIf</span></span>
<span data-ttu-id="aa188-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa188-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa188-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa188-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa188-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa188-156">CommonParameters</span></span>
<span data-ttu-id="aa188-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa188-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa188-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa188-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa188-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa188-159">INPUTS</span></span>

### <span data-ttu-id="aa188-160">System. String</span><span class="sxs-lookup"><span data-stu-id="aa188-160">System.String</span></span>

## <span data-ttu-id="aa188-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa188-161">OUTPUTS</span></span>

### <span data-ttu-id="aa188-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa188-162">System.Boolean</span></span>

## <span data-ttu-id="aa188-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa188-163">NOTES</span></span>

## <span data-ttu-id="aa188-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa188-164">RELATED LINKS</span></span>

[<span data-ttu-id="aa188-165">Localizar-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-165">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="aa188-166">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-166">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="aa188-167">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-167">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="aa188-168">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-168">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="aa188-169">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="aa188-169">Set-AzResource</span></span>](./Set-AzResource.md)


