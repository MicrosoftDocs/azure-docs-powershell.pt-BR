---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610063"
---
# <span data-ttu-id="fc45b-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="fc45b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc45b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc45b-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="fc45b-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc45b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc45b-104">SYNTAX</span></span>

### <span data-ttu-id="fc45b-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="fc45b-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc45b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="fc45b-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc45b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="fc45b-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc45b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc45b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc45b-109">O cmdlet **Remove-AzureRmResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc45b-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="fc45b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc45b-110">EXAMPLES</span></span>

### <span data-ttu-id="fc45b-111">Exemplo 1: remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="fc45b-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="fc45b-112">Esse comando Remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="fc45b-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="fc45b-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fc45b-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="fc45b-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="fc45b-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="fc45b-115">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="fc45b-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="fc45b-116">OS</span><span class="sxs-lookup"><span data-stu-id="fc45b-116">PARAMETERS</span></span>

### <span data-ttu-id="fc45b-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc45b-117">-ApiVersion</span></span>
<span data-ttu-id="fc45b-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="fc45b-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fc45b-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="fc45b-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fc45b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc45b-120">-AsJob</span></span>
<span data-ttu-id="fc45b-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fc45b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc45b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc45b-122">-DefaultProfile</span></span>
<span data-ttu-id="fc45b-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fc45b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc45b-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="fc45b-124">-ExtensionResourceName</span></span>
<span data-ttu-id="fc45b-125">Especifica o nome de um recurso de extensão do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fc45b-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fc45b-126">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="fc45b-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="fc45b-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="fc45b-127">-ExtensionResourceType</span></span>
<span data-ttu-id="fc45b-128">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="fc45b-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="fc45b-129">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="fc45b-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="fc45b-130">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fc45b-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fc45b-131">-Force</span><span class="sxs-lookup"><span data-stu-id="fc45b-131">-Force</span></span>
<span data-ttu-id="fc45b-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fc45b-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fc45b-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="fc45b-133">-ODataQuery</span></span>
<span data-ttu-id="fc45b-134">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="fc45b-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="fc45b-135">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="fc45b-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="fc45b-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc45b-136">-Pre</span></span>
<span data-ttu-id="fc45b-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="fc45b-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fc45b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc45b-138">-ResourceGroupName</span></span>
<span data-ttu-id="fc45b-139">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="fc45b-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="fc45b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc45b-140">-ResourceId</span></span>
<span data-ttu-id="fc45b-141">Especifica a ID de recurso totalmente qualificado do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fc45b-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fc45b-142">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fc45b-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fc45b-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="fc45b-143">-ResourceName</span></span>
<span data-ttu-id="fc45b-144">Especifica o nome do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fc45b-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fc45b-145">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="fc45b-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="fc45b-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="fc45b-146">-ResourceType</span></span>
<span data-ttu-id="fc45b-147">Especifica o tipo do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="fc45b-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="fc45b-148">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="fc45b-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="fc45b-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="fc45b-149">-TenantLevel</span></span>
<span data-ttu-id="fc45b-150">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="fc45b-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="fc45b-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc45b-151">-Confirm</span></span>
<span data-ttu-id="fc45b-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc45b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc45b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc45b-153">-WhatIf</span></span>
<span data-ttu-id="fc45b-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc45b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc45b-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc45b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc45b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc45b-156">CommonParameters</span></span>
<span data-ttu-id="fc45b-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc45b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc45b-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc45b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc45b-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc45b-159">INPUTS</span></span>

### <span data-ttu-id="fc45b-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc45b-160">None</span></span>

## <span data-ttu-id="fc45b-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc45b-161">OUTPUTS</span></span>

### <span data-ttu-id="fc45b-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc45b-162">System.Boolean</span></span>

## <span data-ttu-id="fc45b-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc45b-163">NOTES</span></span>

## <span data-ttu-id="fc45b-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc45b-164">RELATED LINKS</span></span>

[<span data-ttu-id="fc45b-165">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="fc45b-166">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="fc45b-167">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="fc45b-168">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="fc45b-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="fc45b-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


