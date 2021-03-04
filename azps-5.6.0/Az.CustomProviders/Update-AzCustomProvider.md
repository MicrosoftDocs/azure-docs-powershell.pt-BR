---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 0f124d818b95928f12cdc71f60c436f5691f8151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891484"
---
# <span data-ttu-id="a7cb7-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="a7cb7-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="a7cb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cb7-103">Atualiza um provedor de recursos personalizados existente.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a7cb7-104">O único valor que pode ser atualizado por meio de PATCH atualmente são as marcas.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a7cb7-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a7cb7-105">SYNTAX</span></span>

### <span data-ttu-id="a7cb7-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a7cb7-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a7cb7-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a7cb7-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a7cb7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a7cb7-108">DESCRIPTION</span></span>
<span data-ttu-id="a7cb7-109">Atualiza um provedor de recursos personalizados existente.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="a7cb7-110">O único valor que pode ser atualizado por meio de PATCH atualmente são as marcas.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="a7cb7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-111">EXAMPLES</span></span>

### <span data-ttu-id="a7cb7-112">Exemplo 1: Adicionar marcas a um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="a7cb7-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="a7cb7-113">Atualize as marcas de um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="a7cb7-114">Exemplo 2: Atualizar provedor personalizado com canalização</span><span class="sxs-lookup"><span data-stu-id="a7cb7-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="a7cb7-115">Atualize um provedor personalizado usando a canalização.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="a7cb7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-116">PARAMETERS</span></span>

### <span data-ttu-id="a7cb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cb7-117">-DefaultProfile</span></span>
<span data-ttu-id="a7cb7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7cb7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7cb7-119">-InputObject</span></span>
<span data-ttu-id="a7cb7-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a7cb7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a7cb7-121">-Name</span></span>
<span data-ttu-id="a7cb7-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="a7cb7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7cb7-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7cb7-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a7cb7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a7cb7-125">-SubscriptionId</span></span>
<span data-ttu-id="a7cb7-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-126">The Azure subscription ID.</span></span>
<span data-ttu-id="a7cb7-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="a7cb7-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a7cb7-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7cb7-128">-Tag</span></span>
<span data-ttu-id="a7cb7-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a7cb7-129">Resource tags</span></span>

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

### <span data-ttu-id="a7cb7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7cb7-130">-Confirm</span></span>
<span data-ttu-id="a7cb7-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7cb7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7cb7-132">-WhatIf</span></span>
<span data-ttu-id="a7cb7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7cb7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7cb7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cb7-135">CommonParameters</span></span>
<span data-ttu-id="a7cb7-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cb7-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7cb7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cb7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-138">INPUTS</span></span>

### <span data-ttu-id="a7cb7-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="a7cb7-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="a7cb7-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-140">OUTPUTS</span></span>

### <span data-ttu-id="a7cb7-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="a7cb7-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="a7cb7-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="a7cb7-142">NOTES</span></span>

<span data-ttu-id="a7cb7-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a7cb7-143">ALIASES</span></span>

<span data-ttu-id="a7cb7-144">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a7cb7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a7cb7-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a7cb7-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a7cb7-147">INPUTOBJECT <ICustomProvidersIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a7cb7-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a7cb7-148">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="a7cb7-149">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a7cb7-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a7cb7-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a7cb7-151">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="a7cb7-152">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="a7cb7-153">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a7cb7-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a7cb7-154">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="a7cb7-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a7cb7-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7cb7-155">RELATED LINKS</span></span>

