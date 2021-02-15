---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: 31039d71f0c26b6fea3e19220b3932d2abd02073
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118737"
---
# <span data-ttu-id="91b8f-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="91b8f-101">Remove-AzResource</span></span>

## <span data-ttu-id="91b8f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="91b8f-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="91b8f-103">Removes a resource.</span></span>

## <span data-ttu-id="91b8f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91b8f-104">SYNTAX</span></span>

### <span data-ttu-id="91b8f-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91b8f-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b8f-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="91b8f-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91b8f-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="91b8f-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b8f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="91b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="91b8f-109">O **cmdlet Remove-AzResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="91b8f-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="91b8f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="91b8f-111">Exemplo 1: Remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="91b8f-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="91b8f-112">Esse comando remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="91b8f-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="91b8f-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="91b8f-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="91b8f-114">O comando especifica o parâmetro *Forçar.*</span><span class="sxs-lookup"><span data-stu-id="91b8f-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="91b8f-115">Portanto, ele não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="91b8f-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="91b8f-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91b8f-116">PARAMETERS</span></span>

### <span data-ttu-id="91b8f-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="91b8f-117">-ApiVersion</span></span>
<span data-ttu-id="91b8f-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="91b8f-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="91b8f-119">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="91b8f-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="91b8f-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91b8f-120">-AsJob</span></span>
<span data-ttu-id="91b8f-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="91b8f-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91b8f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b8f-122">-DefaultProfile</span></span>
<span data-ttu-id="91b8f-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91b8f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91b8f-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="91b8f-124">-ExtensionResourceName</span></span>
<span data-ttu-id="91b8f-125">Especifica o nome de um recurso de extensão do recurso que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="91b8f-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="91b8f-126">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="91b8f-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="91b8f-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="91b8f-127">-ExtensionResourceType</span></span>
<span data-ttu-id="91b8f-128">Especifica o tipo de recurso de um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="91b8f-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="91b8f-129">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="91b8f-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="91b8f-130">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="91b8f-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="91b8f-131">-Forçar</span><span class="sxs-lookup"><span data-stu-id="91b8f-131">-Force</span></span>
<span data-ttu-id="91b8f-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="91b8f-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91b8f-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="91b8f-133">-ODataQuery</span></span>
<span data-ttu-id="91b8f-134">Especifica um filtro de estilo OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="91b8f-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="91b8f-135">Esse cmdlet anexa esse valor à solicitação além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="91b8f-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="91b8f-136">-Pré-</span><span class="sxs-lookup"><span data-stu-id="91b8f-136">-Pre</span></span>
<span data-ttu-id="91b8f-137">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="91b8f-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="91b8f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b8f-138">-ResourceGroupName</span></span>
<span data-ttu-id="91b8f-139">Especifica o nome do grupo de recursos do qual este cmdlet remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="91b8f-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="91b8f-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91b8f-140">-ResourceId</span></span>
<span data-ttu-id="91b8f-141">Especifica a ID de recurso totalmente qualificada do recurso que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="91b8f-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="91b8f-142">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="91b8f-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="91b8f-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="91b8f-143">-ResourceName</span></span>
<span data-ttu-id="91b8f-144">Especifica o nome do recurso que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="91b8f-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="91b8f-145">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="91b8f-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="91b8f-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="91b8f-146">-ResourceType</span></span>
<span data-ttu-id="91b8f-147">Especifica o tipo de recurso que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="91b8f-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="91b8f-148">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="91b8f-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="91b8f-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="91b8f-149">-TenantLevel</span></span>
<span data-ttu-id="91b8f-150">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="91b8f-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="91b8f-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91b8f-151">-Confirm</span></span>
<span data-ttu-id="91b8f-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91b8f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b8f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b8f-153">-WhatIf</span></span>
<span data-ttu-id="91b8f-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91b8f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91b8f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91b8f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b8f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b8f-156">CommonParameters</span></span>
<span data-ttu-id="91b8f-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b8f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b8f-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91b8f-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b8f-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="91b8f-159">INPUTS</span></span>

### <span data-ttu-id="91b8f-160">System.String</span><span class="sxs-lookup"><span data-stu-id="91b8f-160">System.String</span></span>

## <span data-ttu-id="91b8f-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="91b8f-161">OUTPUTS</span></span>

### <span data-ttu-id="91b8f-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91b8f-162">System.Boolean</span></span>

## <span data-ttu-id="91b8f-163">Notas</span><span class="sxs-lookup"><span data-stu-id="91b8f-163">NOTES</span></span>

## <span data-ttu-id="91b8f-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91b8f-164">RELATED LINKS</span></span>

[<span data-ttu-id="91b8f-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="91b8f-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="91b8f-166">Mover-AzResource</span><span class="sxs-lookup"><span data-stu-id="91b8f-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="91b8f-167">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="91b8f-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="91b8f-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="91b8f-168">Set-AzResource</span></span>](./Set-AzResource.md)


