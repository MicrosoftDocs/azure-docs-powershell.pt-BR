---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599409"
---
# <span data-ttu-id="aa91b-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="aa91b-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="aa91b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa91b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa91b-103">Invoca uma ação em um recurso.</span><span class="sxs-lookup"><span data-stu-id="aa91b-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="aa91b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa91b-104">SYNTAX</span></span>

### <span data-ttu-id="aa91b-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="aa91b-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa91b-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="aa91b-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa91b-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa91b-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa91b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa91b-108">DESCRIPTION</span></span>
<span data-ttu-id="aa91b-109">O cmdlet **Invoke-AzResourceAction** invoca uma ação em um recurso do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="aa91b-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="aa91b-110">Para obter uma lista de ações com suporte, use a ferramenta Azure Resource Explorer.</span><span class="sxs-lookup"><span data-stu-id="aa91b-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="aa91b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa91b-111">EXAMPLES</span></span>

## <span data-ttu-id="aa91b-112">OS</span><span class="sxs-lookup"><span data-stu-id="aa91b-112">PARAMETERS</span></span>

### <span data-ttu-id="aa91b-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="aa91b-113">-Action</span></span>
<span data-ttu-id="aa91b-114">Especifica o nome da ação a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="aa91b-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="aa91b-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="aa91b-115">-ApiVersion</span></span>
<span data-ttu-id="aa91b-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="aa91b-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="aa91b-117">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="aa91b-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="aa91b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa91b-118">-DefaultProfile</span></span>
<span data-ttu-id="aa91b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="aa91b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa91b-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="aa91b-120">-ExtensionResourceName</span></span>
<span data-ttu-id="aa91b-121">Especifica o nome de um recurso de extensão para o recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="aa91b-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="aa91b-122">Por exemplo, para especificar um banco de dados, use o seguinte formato: nome do banco de dados nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="aa91b-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="aa91b-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="aa91b-123">-ExtensionResourceType</span></span>
<span data-ttu-id="aa91b-124">Especifica o tipo do recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="aa91b-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="aa91b-125">Por exemplo: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa91b-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa91b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="aa91b-126">-Force</span></span>
<span data-ttu-id="aa91b-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa91b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa91b-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="aa91b-128">-ODataQuery</span></span>
<span data-ttu-id="aa91b-129">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="aa91b-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="aa91b-130">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="aa91b-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="aa91b-131">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa91b-131">-Parameters</span></span>
<span data-ttu-id="aa91b-132">Especifica os parâmetros, como uma tabela de hash, para a ação invocada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa91b-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="aa91b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="aa91b-133">-Pre</span></span>
<span data-ttu-id="aa91b-134">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="aa91b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="aa91b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa91b-135">-ResourceGroupName</span></span>
<span data-ttu-id="aa91b-136">Especifica o nome de um grupo de recursos no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="aa91b-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="aa91b-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa91b-137">-ResourceId</span></span>
<span data-ttu-id="aa91b-138">Especifica a ID de recurso totalmente qualificado do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="aa91b-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="aa91b-139">A ID inclui a assinatura, como no exemplo a seguir: `/subscriptions/` ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa91b-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa91b-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="aa91b-140">-ResourceName</span></span>
<span data-ttu-id="aa91b-141">Especifica o nome do recurso do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="aa91b-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="aa91b-142">Por exemplo, para especificar um banco de dados, use o seguinte formato: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="aa91b-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="aa91b-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="aa91b-143">-ResourceType</span></span>
<span data-ttu-id="aa91b-144">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="aa91b-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="aa91b-145">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="aa91b-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="aa91b-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="aa91b-146">-TenantLevel</span></span>
<span data-ttu-id="aa91b-147">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="aa91b-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="aa91b-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa91b-148">-Confirm</span></span>
<span data-ttu-id="aa91b-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa91b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa91b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa91b-150">-WhatIf</span></span>
<span data-ttu-id="aa91b-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa91b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa91b-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa91b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa91b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa91b-153">CommonParameters</span></span>
<span data-ttu-id="aa91b-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa91b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa91b-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa91b-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa91b-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa91b-156">INPUTS</span></span>

### <span data-ttu-id="aa91b-157">System. String</span><span class="sxs-lookup"><span data-stu-id="aa91b-157">System.String</span></span>

## <span data-ttu-id="aa91b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa91b-158">OUTPUTS</span></span>

### <span data-ttu-id="aa91b-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="aa91b-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="aa91b-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa91b-160">NOTES</span></span>

## <span data-ttu-id="aa91b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa91b-161">RELATED LINKS</span></span>
