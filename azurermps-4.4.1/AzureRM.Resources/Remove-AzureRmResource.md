---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432558"
---
# <span data-ttu-id="8483e-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="8483e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8483e-102">SYNOPSIS</span></span>
<span data-ttu-id="8483e-103">Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="8483e-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8483e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8483e-104">SYNTAX</span></span>

### <span data-ttu-id="8483e-105">A ID do recurso. (padrão)</span><span class="sxs-lookup"><span data-stu-id="8483e-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8483e-106">Recurso que reside no nível da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8483e-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8483e-107">Recurso que reside no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="8483e-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8483e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8483e-108">DESCRIPTION</span></span>
<span data-ttu-id="8483e-109">O cmdlet **Remove-AzureRmResource** remove um recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="8483e-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="8483e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8483e-110">EXAMPLES</span></span>

### <span data-ttu-id="8483e-111">Exemplo 1: remover um recurso de site</span><span class="sxs-lookup"><span data-stu-id="8483e-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="8483e-112">Esse comando Remove o recurso de site chamado ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="8483e-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="8483e-113">O exemplo usa um valor de espaço reservado para a ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="8483e-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="8483e-114">O comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8483e-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8483e-115">Portanto, ele não solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="8483e-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8483e-116">OS</span><span class="sxs-lookup"><span data-stu-id="8483e-116">PARAMETERS</span></span>

### <span data-ttu-id="8483e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8483e-117">-ApiVersion</span></span>
<span data-ttu-id="8483e-118">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8483e-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8483e-119">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8483e-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8483e-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="8483e-120">-ExtensionResourceName</span></span>
<span data-ttu-id="8483e-121">Especifica o nome de um recurso de extensão do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8483e-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="8483e-122">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="8483e-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="8483e-123">nome do banco de dados do nome do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="8483e-123">server name`/`database name</span></span>

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

### <span data-ttu-id="8483e-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="8483e-124">-ExtensionResourceType</span></span>
<span data-ttu-id="8483e-125">Especifica o tipo de recurso para um recurso de extensão.</span><span class="sxs-lookup"><span data-stu-id="8483e-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="8483e-126">Especifica o tipo de recurso de extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="8483e-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="8483e-127">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8483e-127">For instance:</span></span> 

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

### <span data-ttu-id="8483e-128">-Force</span><span class="sxs-lookup"><span data-stu-id="8483e-128">-Force</span></span>
<span data-ttu-id="8483e-129">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8483e-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8483e-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8483e-130">-ODataQuery</span></span>
<span data-ttu-id="8483e-131">Especifica um filtro de estilo Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="8483e-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="8483e-132">Esse cmdlet acrescenta esse valor à solicitação, além de outros filtros.</span><span class="sxs-lookup"><span data-stu-id="8483e-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="8483e-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="8483e-133">-Pre</span></span>
<span data-ttu-id="8483e-134">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8483e-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8483e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8483e-135">-ResourceGroupName</span></span>
<span data-ttu-id="8483e-136">Especifica o nome do grupo de recursos a partir do qual esse cmdlet Remove um recurso.</span><span class="sxs-lookup"><span data-stu-id="8483e-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="8483e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8483e-137">-ResourceId</span></span>
<span data-ttu-id="8483e-138">Especifica a ID de recurso totalmente qualificado do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8483e-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="8483e-139">A ID inclui a assinatura, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="8483e-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="8483e-140">`/subscriptions/`ID da assinatura`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="8483e-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="8483e-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8483e-141">-ResourceName</span></span>
<span data-ttu-id="8483e-142">Especifica o nome do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8483e-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="8483e-143">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="8483e-143">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="8483e-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8483e-144">-ResourceType</span></span>
<span data-ttu-id="8483e-145">Especifica o tipo do recurso que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8483e-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="8483e-146">Por exemplo, para um banco de dados, o tipo de recurso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8483e-146">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="8483e-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8483e-147">-TenantLevel</span></span>
<span data-ttu-id="8483e-148">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="8483e-148">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8483e-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8483e-149">-Confirm</span></span>
<span data-ttu-id="8483e-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8483e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8483e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8483e-151">-WhatIf</span></span>
<span data-ttu-id="8483e-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8483e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8483e-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8483e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8483e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8483e-154">-DefaultProfile</span></span>
<span data-ttu-id="8483e-155">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8483e-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8483e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8483e-156">CommonParameters</span></span>
<span data-ttu-id="8483e-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8483e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8483e-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8483e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8483e-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8483e-159">INPUTS</span></span>

## <span data-ttu-id="8483e-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8483e-160">OUTPUTS</span></span>

### <span data-ttu-id="8483e-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8483e-161">System.Boolean</span></span>

## <span data-ttu-id="8483e-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8483e-162">NOTES</span></span>

## <span data-ttu-id="8483e-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8483e-163">RELATED LINKS</span></span>

[<span data-ttu-id="8483e-164">Localizar-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="8483e-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="8483e-166">Mover-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="8483e-167">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="8483e-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="8483e-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


