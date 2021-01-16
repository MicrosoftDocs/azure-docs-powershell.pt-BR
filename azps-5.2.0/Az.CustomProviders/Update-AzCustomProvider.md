---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261373"
---
# <span data-ttu-id="e4412-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="e4412-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="e4412-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4412-102">SYNOPSIS</span></span>
<span data-ttu-id="e4412-103">Atualiza um provedor de recursos personalizado existente.</span><span class="sxs-lookup"><span data-stu-id="e4412-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="e4412-104">Atualmente, o único valor que pode ser atualizado via PATCH é a marca.</span><span class="sxs-lookup"><span data-stu-id="e4412-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="e4412-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4412-105">SYNTAX</span></span>

### <span data-ttu-id="e4412-106">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4412-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4412-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4412-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4412-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4412-108">DESCRIPTION</span></span>
<span data-ttu-id="e4412-109">Atualiza um provedor de recursos personalizado existente.</span><span class="sxs-lookup"><span data-stu-id="e4412-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="e4412-110">Atualmente, o único valor que pode ser atualizado via PATCH é a marca.</span><span class="sxs-lookup"><span data-stu-id="e4412-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="e4412-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4412-111">EXAMPLES</span></span>

### <span data-ttu-id="e4412-112">Exemplo 1: adicionar marcas a um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="e4412-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="e4412-113">Atualize as marcas de um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="e4412-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="e4412-114">Exemplo 2: atualizar provedor personalizado com tubulação</span><span class="sxs-lookup"><span data-stu-id="e4412-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="e4412-115">Atualize um provedor personalizado usando o encanamento.</span><span class="sxs-lookup"><span data-stu-id="e4412-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="e4412-116">OS</span><span class="sxs-lookup"><span data-stu-id="e4412-116">PARAMETERS</span></span>

### <span data-ttu-id="e4412-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4412-117">-DefaultProfile</span></span>
<span data-ttu-id="e4412-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4412-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4412-119">-InputObject</span></span>
<span data-ttu-id="e4412-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e4412-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4412-121">-Name</span></span>
<span data-ttu-id="e4412-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4412-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4412-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4412-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4412-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4412-125">-SubscriptionId</span></span>
<span data-ttu-id="e4412-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4412-126">The Azure subscription ID.</span></span>
<span data-ttu-id="e4412-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="e4412-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="e4412-128">-Tag</span></span>
<span data-ttu-id="e4412-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="e4412-129">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4412-130">-Confirm</span></span>
<span data-ttu-id="e4412-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4412-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4412-132">-WhatIf</span></span>
<span data-ttu-id="e4412-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4412-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4412-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4412-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4412-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4412-135">CommonParameters</span></span>
<span data-ttu-id="e4412-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4412-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4412-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4412-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4412-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4412-138">INPUTS</span></span>

### <span data-ttu-id="e4412-139">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="e4412-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="e4412-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4412-140">OUTPUTS</span></span>

### <span data-ttu-id="e4412-141">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="e4412-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="e4412-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4412-142">NOTES</span></span>

<span data-ttu-id="e4412-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e4412-143">ALIASES</span></span>

<span data-ttu-id="e4412-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e4412-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4412-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e4412-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4412-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4412-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4412-147">INPUTobject <ICustomProvidersIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="e4412-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4412-148">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="e4412-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="e4412-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e4412-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4412-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4412-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="e4412-151">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="e4412-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="e4412-152">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="e4412-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="e4412-153">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4412-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="e4412-154">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="e4412-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="e4412-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4412-155">RELATED LINKS</span></span>

