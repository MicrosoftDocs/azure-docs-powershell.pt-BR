---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
ms.openlocfilehash: 29cdde4d48ca782abd680647ed895945062c055d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786372"
---
# <span data-ttu-id="0bb10-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0bb10-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="0bb10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bb10-102">SYNOPSIS</span></span>
<span data-ttu-id="0bb10-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="0bb10-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bb10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bb10-104">SYNTAX</span></span>

### <span data-ttu-id="0bb10-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="0bb10-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bb10-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0bb10-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0bb10-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0bb10-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bb10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0bb10-108">DESCRIPTION</span></span>
<span data-ttu-id="0bb10-109">O cmdlet **Remove-AzureRmResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bb10-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="0bb10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bb10-110">EXAMPLES</span></span>

### <span data-ttu-id="0bb10-111">Exemplo 1: remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="0bb10-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="0bb10-112">Esse comando Remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="0bb10-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="0bb10-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="0bb10-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="0bb10-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="0bb10-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0bb10-115">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="0bb10-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0bb10-116">OS</span><span class="sxs-lookup"><span data-stu-id="0bb10-116">PARAMETERS</span></span>

### <span data-ttu-id="0bb10-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0bb10-117">-ApiVersion</span></span>
<span data-ttu-id="0bb10-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="0bb10-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0bb10-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="0bb10-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0bb10-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bb10-120">-AsJob</span></span>
<span data-ttu-id="0bb10-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0bb10-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bb10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bb10-122">-DefaultProfile</span></span>
<span data-ttu-id="0bb10-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0bb10-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bb10-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0bb10-124">-ExtensionResourceName</span></span>
<span data-ttu-id="0bb10-125">Especifica o nome de um recurso de extensão do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0bb10-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="0bb10-126">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="0bb10-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="0bb10-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0bb10-127">-ExtensionResourceType</span></span>
<span data-ttu-id="0bb10-128">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="0bb10-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0bb10-129">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="0bb10-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="0bb10-130">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0bb10-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0bb10-131">-Force</span><span class="sxs-lookup"><span data-stu-id="0bb10-131">-Force</span></span>
<span data-ttu-id="0bb10-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0bb10-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0bb10-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0bb10-133">-ODataQuery</span></span>
<span data-ttu-id="0bb10-134">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0bb10-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="0bb10-135">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="0bb10-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0bb10-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="0bb10-136">-Pre</span></span>
<span data-ttu-id="0bb10-137">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="0bb10-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0bb10-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bb10-138">-ResourceGroupName</span></span>
<span data-ttu-id="0bb10-139">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="0bb10-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="0bb10-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bb10-140">-ResourceId</span></span>
<span data-ttu-id="0bb10-141">Especifica a ID de recurso totalmente qualificado do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0bb10-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="0bb10-142">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0bb10-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0bb10-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0bb10-143">-ResourceName</span></span>
<span data-ttu-id="0bb10-144">Especifica o nome do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0bb10-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="0bb10-145">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0bb10-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0bb10-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0bb10-146">-ResourceType</span></span>
<span data-ttu-id="0bb10-147">Especifica o tipo do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0bb10-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="0bb10-148">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0bb10-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0bb10-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0bb10-149">-TenantLevel</span></span>
<span data-ttu-id="0bb10-150">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="0bb10-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0bb10-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0bb10-151">-Confirm</span></span>
<span data-ttu-id="0bb10-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bb10-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bb10-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bb10-153">-WhatIf</span></span>
<span data-ttu-id="0bb10-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0bb10-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bb10-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0bb10-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bb10-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bb10-156">CommonParameters</span></span>
<span data-ttu-id="0bb10-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bb10-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bb10-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bb10-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bb10-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0bb10-159">INPUTS</span></span>

### <span data-ttu-id="0bb10-160">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0bb10-160">None</span></span>

## <span data-ttu-id="0bb10-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0bb10-161">OUTPUTS</span></span>

### <span data-ttu-id="0bb10-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bb10-162">System.Boolean</span></span>

## <span data-ttu-id="0bb10-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0bb10-163">NOTES</span></span>

## <span data-ttu-id="0bb10-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bb10-164">RELATED LINKS</span></span>



[<span data-ttu-id="0bb10-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0bb10-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0bb10-166">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0bb10-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="0bb10-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0bb10-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="0bb10-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0bb10-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


