---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603233"
---
# <span data-ttu-id="7237c-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="7237c-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="7237c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7237c-102">SYNOPSIS</span></span>
<span data-ttu-id="7237c-103">Invoca uma ação em um recurso.</span><span class="sxs-lookup"><span data-stu-id="7237c-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7237c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7237c-104">SYNTAX</span></span>

### <span data-ttu-id="7237c-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="7237c-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7237c-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="7237c-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7237c-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="7237c-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7237c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7237c-108">DESCRIPTION</span></span>
<span data-ttu-id="7237c-109">O cmdlet **Invoke-AzureRmResourceAction** invoca uma ação em um recurso do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="7237c-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="7237c-110">Para obter uma lista de ações com suporte, use a ferramenta Azure Resource Explorer.</span><span class="sxs-lookup"><span data-stu-id="7237c-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="7237c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7237c-111">EXAMPLES</span></span>

## <span data-ttu-id="7237c-112">OS</span><span class="sxs-lookup"><span data-stu-id="7237c-112">PARAMETERS</span></span>

### <span data-ttu-id="7237c-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="7237c-113">-Action</span></span>
<span data-ttu-id="7237c-114">Especifica o nome da ação a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="7237c-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7237c-115">-ApiVersion</span></span>
<span data-ttu-id="7237c-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="7237c-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7237c-117">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="7237c-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7237c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7237c-118">-DefaultProfile</span></span>
<span data-ttu-id="7237c-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7237c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7237c-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="7237c-120">-ExtensionResourceName</span></span>
<span data-ttu-id="7237c-121">Especifica o nome de um recurso de extensão para o recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="7237c-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7237c-122">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="7237c-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="7237c-123">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="7237c-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="7237c-124">-ExtensionResourceType</span></span>
<span data-ttu-id="7237c-125">Especifica o tipo do recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="7237c-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="7237c-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="7237c-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7237c-127">-Force</span></span>
<span data-ttu-id="7237c-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7237c-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7237c-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7237c-129">-InformationAction</span></span>
<span data-ttu-id="7237c-130">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7237c-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7237c-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7237c-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7237c-132">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7237c-132">Continue</span></span>
- <span data-ttu-id="7237c-133">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7237c-133">Ignore</span></span>
- <span data-ttu-id="7237c-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="7237c-134">Inquire</span></span>
- <span data-ttu-id="7237c-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7237c-135">SilentlyContinue</span></span>
- <span data-ttu-id="7237c-136">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7237c-136">Stop</span></span>
- <span data-ttu-id="7237c-137">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7237c-137">Suspend</span></span>

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

### <span data-ttu-id="7237c-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7237c-138">-InformationVariable</span></span>
<span data-ttu-id="7237c-139">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7237c-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7237c-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="7237c-140">-ODataQuery</span></span>
<span data-ttu-id="7237c-141">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="7237c-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="7237c-142">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="7237c-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="7237c-143">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7237c-143">-Parameters</span></span>
<span data-ttu-id="7237c-144">Especifica os parâmetros, como uma tabela de hash, para a ação invocada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7237c-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="7237c-145">-Pre</span></span>
<span data-ttu-id="7237c-146">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="7237c-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7237c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7237c-147">-ResourceGroupName</span></span>
<span data-ttu-id="7237c-148">Especifica o nome de um grupo de recursos no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="7237c-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7237c-149">-ResourceId</span></span>
<span data-ttu-id="7237c-150">Especifica a ID de recurso totalmente qualificado do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="7237c-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7237c-151">A ID inclui a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="7237c-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="7237c-152">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="7237c-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7237c-153">-ResourceName</span></span>
<span data-ttu-id="7237c-154">Especifica o nome do recurso do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="7237c-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="7237c-155">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="7237c-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7237c-156">-ResourceType</span></span>
<span data-ttu-id="7237c-157">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="7237c-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="7237c-158">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7237c-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="7237c-159">-TenantLevel</span></span>
<span data-ttu-id="7237c-160">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="7237c-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7237c-161">-Confirm</span></span>
<span data-ttu-id="7237c-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7237c-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7237c-163">-WhatIf</span></span>
<span data-ttu-id="7237c-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7237c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7237c-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7237c-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7237c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7237c-166">CommonParameters</span></span>
<span data-ttu-id="7237c-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7237c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7237c-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7237c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7237c-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7237c-169">INPUTS</span></span>

### <span data-ttu-id="7237c-170">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7237c-170">None</span></span>
<span data-ttu-id="7237c-171">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7237c-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7237c-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7237c-172">OUTPUTS</span></span>

### <span data-ttu-id="7237c-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7237c-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7237c-174">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7237c-174">NOTES</span></span>

## <span data-ttu-id="7237c-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7237c-175">RELATED LINKS</span></span>
