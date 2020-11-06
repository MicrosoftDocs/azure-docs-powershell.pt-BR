---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 0cf65c33ca5af99be30f7bfa85ad4ad80ff62735
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431623"
---
# <span data-ttu-id="9bb63-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="9bb63-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bb63-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb63-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="9bb63-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb63-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bb63-104">SYNTAX</span></span>

### <span data-ttu-id="9bb63-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bb63-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bb63-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9bb63-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bb63-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9bb63-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb63-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bb63-108">DESCRIPTION</span></span>
<span data-ttu-id="9bb63-109">O cmdlet **Remove-AzureRmResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb63-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="9bb63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bb63-110">EXAMPLES</span></span>

### <span data-ttu-id="9bb63-111">Exemplo 1: remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="9bb63-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="9bb63-112">Esse comando Remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="9bb63-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="9bb63-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9bb63-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="9bb63-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="9bb63-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9bb63-115">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="9bb63-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9bb63-116">OS</span><span class="sxs-lookup"><span data-stu-id="9bb63-116">PARAMETERS</span></span>

### <span data-ttu-id="9bb63-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9bb63-117">-ApiVersion</span></span>
<span data-ttu-id="9bb63-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9bb63-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9bb63-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="9bb63-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9bb63-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9bb63-120">-AsJob</span></span>
<span data-ttu-id="9bb63-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9bb63-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bb63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb63-122">-DefaultProfile</span></span>
<span data-ttu-id="9bb63-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9bb63-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bb63-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9bb63-124">-ExtensionResourceName</span></span>
<span data-ttu-id="9bb63-125">Especifica o nome de um recurso de extensão do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9bb63-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="9bb63-126">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9bb63-126">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="9bb63-127">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="9bb63-127">server name`/`database name</span></span>

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

### <span data-ttu-id="9bb63-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9bb63-128">-ExtensionResourceType</span></span>
<span data-ttu-id="9bb63-129">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="9bb63-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="9bb63-130">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="9bb63-130">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="9bb63-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9bb63-131">For instance:</span></span> 

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

### <span data-ttu-id="9bb63-132">-Force</span><span class="sxs-lookup"><span data-stu-id="9bb63-132">-Force</span></span>
<span data-ttu-id="9bb63-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9bb63-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bb63-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9bb63-134">-ODataQuery</span></span>
<span data-ttu-id="9bb63-135">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="9bb63-135">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9bb63-136">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="9bb63-136">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="9bb63-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="9bb63-137">-Pre</span></span>
<span data-ttu-id="9bb63-138">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9bb63-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9bb63-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb63-139">-ResourceGroupName</span></span>
<span data-ttu-id="9bb63-140">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="9bb63-140">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="9bb63-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bb63-141">-ResourceId</span></span>
<span data-ttu-id="9bb63-142">Especifica a ID de recurso totalmente qualificado do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9bb63-142">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="9bb63-143">A ID inclui a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9bb63-143">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="9bb63-144">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9bb63-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9bb63-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9bb63-145">-ResourceName</span></span>
<span data-ttu-id="9bb63-146">Especifica o nome do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9bb63-146">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="9bb63-147">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="9bb63-147">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="9bb63-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9bb63-148">-ResourceType</span></span>
<span data-ttu-id="9bb63-149">Especifica o tipo do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9bb63-149">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="9bb63-150">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9bb63-150">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="9bb63-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9bb63-151">-TenantLevel</span></span>
<span data-ttu-id="9bb63-152">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="9bb63-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9bb63-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bb63-153">-Confirm</span></span>
<span data-ttu-id="9bb63-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb63-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb63-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb63-155">-WhatIf</span></span>
<span data-ttu-id="9bb63-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bb63-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb63-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bb63-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb63-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb63-158">CommonParameters</span></span>
<span data-ttu-id="9bb63-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb63-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb63-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb63-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb63-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bb63-161">INPUTS</span></span>

### <span data-ttu-id="9bb63-162">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9bb63-162">None</span></span>
<span data-ttu-id="9bb63-163">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="9bb63-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bb63-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bb63-164">OUTPUTS</span></span>

### <span data-ttu-id="9bb63-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bb63-165">System.Boolean</span></span>

## <span data-ttu-id="9bb63-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bb63-166">NOTES</span></span>

## <span data-ttu-id="9bb63-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bb63-167">RELATED LINKS</span></span>

[<span data-ttu-id="9bb63-168">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-168">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9bb63-169">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-169">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="9bb63-170">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-170">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9bb63-171">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-171">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9bb63-172">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9bb63-172">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


