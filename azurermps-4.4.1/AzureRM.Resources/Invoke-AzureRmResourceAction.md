---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602197"
---
# <span data-ttu-id="d8862-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="d8862-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="d8862-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8862-102">SYNOPSIS</span></span>
<span data-ttu-id="d8862-103">Invoca uma ação em um recurso.</span><span class="sxs-lookup"><span data-stu-id="d8862-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8862-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8862-104">SYNTAX</span></span>

### <span data-ttu-id="d8862-105">A ID do recurso. (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8862-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8862-106">Recurso que reside no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d8862-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8862-107">Recurso que reside no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="d8862-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8862-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8862-108">DESCRIPTION</span></span>
<span data-ttu-id="d8862-109">O cmdlet **Invoke-AzureRmResourceAction** invoca uma ação em um recurso do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="d8862-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="d8862-110">Para obter uma lista de ações com suporte, use a ferramenta Azure Resource Explorer.</span><span class="sxs-lookup"><span data-stu-id="d8862-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="d8862-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8862-111">EXAMPLES</span></span>

## <span data-ttu-id="d8862-112">OS</span><span class="sxs-lookup"><span data-stu-id="d8862-112">PARAMETERS</span></span>

### <span data-ttu-id="d8862-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="d8862-113">-Action</span></span>
<span data-ttu-id="d8862-114">Especifica o nome da ação a ser invocada.</span><span class="sxs-lookup"><span data-stu-id="d8862-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="d8862-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8862-115">-ApiVersion</span></span>
<span data-ttu-id="d8862-116">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d8862-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d8862-117">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="d8862-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d8862-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d8862-118">-ExtensionResourceName</span></span>
<span data-ttu-id="d8862-119">Especifica o nome de um recurso de extensão para o recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="d8862-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="d8862-120">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="d8862-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="d8862-121">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="d8862-121">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d8862-122">-ExtensionResourceType</span></span>
<span data-ttu-id="d8862-123">Especifica o tipo do recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="d8862-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="d8862-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d8862-124">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d8862-125">-Force</span></span>
<span data-ttu-id="d8862-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8862-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8862-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d8862-127">-InformationAction</span></span>
<span data-ttu-id="d8862-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="d8862-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8862-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d8862-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8862-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="d8862-130">Continue</span></span>
- <span data-ttu-id="d8862-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="d8862-131">Ignore</span></span>
- <span data-ttu-id="d8862-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="d8862-132">Inquire</span></span>
- <span data-ttu-id="d8862-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8862-133">SilentlyContinue</span></span>
- <span data-ttu-id="d8862-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="d8862-134">Stop</span></span>
- <span data-ttu-id="d8862-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="d8862-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8862-136">-InformationVariable</span></span>
<span data-ttu-id="d8862-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="d8862-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d8862-138">-ODataQuery</span></span>
<span data-ttu-id="d8862-139">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="d8862-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="d8862-140">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="d8862-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="d8862-141">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8862-141">-Parameters</span></span>
<span data-ttu-id="d8862-142">Especifica os parâmetros, como uma tabela de hash, para a ação invocada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8862-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="d8862-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="d8862-143">-Pre</span></span>
<span data-ttu-id="d8862-144">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d8862-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8862-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8862-145">-ResourceGroupName</span></span>
<span data-ttu-id="d8862-146">Especifica o nome de um grupo de recursos no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="d8862-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8862-147">-ResourceId</span></span>
<span data-ttu-id="d8862-148">Especifica a ID de recurso totalmente qualificado do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="d8862-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="d8862-149">A ID inclui a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="d8862-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="d8862-150">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d8862-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d8862-151">-ResourceName</span></span>
<span data-ttu-id="d8862-152">Especifica o nome do recurso do recurso no qual esse cmdlet invoca uma ação.</span><span class="sxs-lookup"><span data-stu-id="d8862-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="d8862-153">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="d8862-153">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d8862-154">-ResourceType</span></span>
<span data-ttu-id="d8862-155">Especifica o tipo do recurso.</span><span class="sxs-lookup"><span data-stu-id="d8862-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="d8862-156">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d8862-156">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d8862-157">-TenantLevel</span></span>
<span data-ttu-id="d8862-158">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="d8862-158">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8862-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d8862-159">-Confirm</span></span>
<span data-ttu-id="d8862-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8862-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8862-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8862-161">-WhatIf</span></span>
<span data-ttu-id="d8862-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8862-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8862-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8862-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8862-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8862-164">-DefaultProfile</span></span>
<span data-ttu-id="d8862-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8862-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8862-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8862-166">CommonParameters</span></span>
<span data-ttu-id="d8862-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8862-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8862-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8862-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8862-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8862-169">INPUTS</span></span>

## <span data-ttu-id="d8862-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8862-170">OUTPUTS</span></span>

### <span data-ttu-id="d8862-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d8862-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d8862-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8862-172">NOTES</span></span>

## <span data-ttu-id="d8862-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8862-173">RELATED LINKS</span></span>

