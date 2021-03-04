---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 14da2ddfdd94be5cd95d00eeeb742b9e4ac982e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888194"
---
# <span data-ttu-id="6b958-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="6b958-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="6b958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b958-102">SYNOPSIS</span></span>
<span data-ttu-id="6b958-103">Invoca uma ação em um recurso.</span><span class="sxs-lookup"><span data-stu-id="6b958-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="6b958-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b958-104">SYNTAX</span></span>

### <span data-ttu-id="6b958-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b958-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b958-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="6b958-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b958-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="6b958-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b958-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b958-108">DESCRIPTION</span></span>
<span data-ttu-id="6b958-109">O cmdlet **Invoke-AzResourceAction** invoca uma ação em um recurso do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="6b958-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="6b958-110">Para obter uma lista de ações com suporte, use a ferramenta Explorador de Recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b958-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="6b958-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b958-111">EXAMPLES</span></span>

### <span data-ttu-id="6b958-112">Exemplo 1: Invocar iniciando uma VM com ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b958-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="6b958-113">Este comando inicia a Máquina Virtual com {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="6b958-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="6b958-114">Exemplo 2: Invocar o poweroffing de uma VM com ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b958-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="6b958-115">Este comando interrompe a Máquina Virtual com {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="6b958-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="6b958-116">O comando especifica o parâmetro *Force,* portanto, não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6b958-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="6b958-117">Exemplo 3: Invocar o registro de um provedor de recursos com ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b958-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="6b958-118">Esse comando registra um provedor de recursos "Microsoft.Network".</span><span class="sxs-lookup"><span data-stu-id="6b958-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="6b958-119">O comando especifica o parâmetro *Force,* portanto, não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="6b958-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6b958-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b958-120">PARAMETERS</span></span>

### <span data-ttu-id="6b958-121">-Action</span><span class="sxs-lookup"><span data-stu-id="6b958-121">-Action</span></span>
<span data-ttu-id="6b958-122">Especifica o nome da ação a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="6b958-122">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b958-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b958-123">-ApiVersion</span></span>
<span data-ttu-id="6b958-124">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="6b958-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6b958-125">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="6b958-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6b958-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b958-126">-DefaultProfile</span></span>
<span data-ttu-id="6b958-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6b958-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b958-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6b958-128">-ExtensionResourceName</span></span>
<span data-ttu-id="6b958-129">Especifica o nome de um recurso de extensão para o recurso no qual este cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="6b958-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6b958-130">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados de nome `/` do servidor</span><span class="sxs-lookup"><span data-stu-id="6b958-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="6b958-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6b958-131">-ExtensionResourceType</span></span>
<span data-ttu-id="6b958-132">Especifica o tipo do recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="6b958-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="6b958-133">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6b958-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6b958-134">-Force</span><span class="sxs-lookup"><span data-stu-id="6b958-134">-Force</span></span>
<span data-ttu-id="6b958-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b958-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b958-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6b958-136">-ODataQuery</span></span>
<span data-ttu-id="6b958-137">Especifica um filtro de estilo OData (Protocolo de Dados Abertos).</span><span class="sxs-lookup"><span data-stu-id="6b958-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="6b958-138">Este cmdlet anexa esse valor à solicitação, além de quaisquer outros filtros.</span><span class="sxs-lookup"><span data-stu-id="6b958-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6b958-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="6b958-139">-Parameters</span></span>
<span data-ttu-id="6b958-140">Especifica parâmetros, como uma tabela de hash, para a ação que esse cmdlet invoca.</span><span class="sxs-lookup"><span data-stu-id="6b958-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b958-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b958-141">-Pre</span></span>
<span data-ttu-id="6b958-142">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6b958-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6b958-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b958-143">-ResourceGroupName</span></span>
<span data-ttu-id="6b958-144">Especifica o nome de um grupo de recursos no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="6b958-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="6b958-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b958-145">-ResourceId</span></span>
<span data-ttu-id="6b958-146">Especifica a ID de recurso totalmente qualificada do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="6b958-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6b958-147">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6b958-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6b958-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b958-148">-ResourceName</span></span>
<span data-ttu-id="6b958-149">Especifica o nome do recurso do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="6b958-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="6b958-150">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6b958-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="6b958-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6b958-151">-ResourceType</span></span>
<span data-ttu-id="6b958-152">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="6b958-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="6b958-153">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="6b958-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="6b958-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6b958-154">-TenantLevel</span></span>
<span data-ttu-id="6b958-155">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="6b958-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="6b958-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b958-156">-Confirm</span></span>
<span data-ttu-id="6b958-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b958-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b958-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b958-158">-WhatIf</span></span>
<span data-ttu-id="6b958-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6b958-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b958-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6b958-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b958-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b958-161">CommonParameters</span></span>
<span data-ttu-id="6b958-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b958-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b958-163">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b958-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b958-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b958-164">INPUTS</span></span>

### <span data-ttu-id="6b958-165">System.String</span><span class="sxs-lookup"><span data-stu-id="6b958-165">System.String</span></span>

## <span data-ttu-id="6b958-166">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b958-166">OUTPUTS</span></span>

### <span data-ttu-id="6b958-167">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="6b958-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6b958-168">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b958-168">NOTES</span></span>

## <span data-ttu-id="6b958-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b958-169">RELATED LINKS</span></span>
