---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112002"
---
# <span data-ttu-id="90e3a-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="90e3a-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="90e3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="90e3a-103">Atualiza um provedor de recursos personalizado existente.</span><span class="sxs-lookup"><span data-stu-id="90e3a-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="90e3a-104">O único valor que pode ser atualizado por meio de PATCH atualmente são as marcas.</span><span class="sxs-lookup"><span data-stu-id="90e3a-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="90e3a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90e3a-105">SYNTAX</span></span>

### <span data-ttu-id="90e3a-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="90e3a-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90e3a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="90e3a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90e3a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="90e3a-108">DESCRIPTION</span></span>
<span data-ttu-id="90e3a-109">Atualiza um provedor de recursos personalizado existente.</span><span class="sxs-lookup"><span data-stu-id="90e3a-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="90e3a-110">O único valor que pode ser atualizado por meio de PATCH atualmente são as marcas.</span><span class="sxs-lookup"><span data-stu-id="90e3a-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="90e3a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90e3a-111">EXAMPLES</span></span>

### <span data-ttu-id="90e3a-112">Exemplo 1: Adicionar marcas a um provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="90e3a-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="90e3a-113">Atualize as marcas de um provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="90e3a-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="90e3a-114">Exemplo 2: Atualizar provedor personalizado com canos</span><span class="sxs-lookup"><span data-stu-id="90e3a-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="90e3a-115">Atualize um provedor personalizado usando a canalização.</span><span class="sxs-lookup"><span data-stu-id="90e3a-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="90e3a-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90e3a-116">PARAMETERS</span></span>

### <span data-ttu-id="90e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="90e3a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90e3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e3a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90e3a-119">-InputObject</span></span>
<span data-ttu-id="90e3a-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="90e3a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90e3a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="90e3a-121">-Name</span></span>
<span data-ttu-id="90e3a-122">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="90e3a-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="90e3a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e3a-123">-ResourceGroupName</span></span>
<span data-ttu-id="90e3a-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90e3a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="90e3a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90e3a-125">-SubscriptionId</span></span>
<span data-ttu-id="90e3a-126">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="90e3a-126">The Azure subscription ID.</span></span>
<span data-ttu-id="90e3a-127">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="90e3a-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="90e3a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="90e3a-128">-Tag</span></span>
<span data-ttu-id="90e3a-129">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="90e3a-129">Resource tags</span></span>

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

### <span data-ttu-id="90e3a-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="90e3a-130">-Confirm</span></span>
<span data-ttu-id="90e3a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e3a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e3a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e3a-132">-WhatIf</span></span>
<span data-ttu-id="90e3a-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="90e3a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e3a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90e3a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e3a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e3a-135">CommonParameters</span></span>
<span data-ttu-id="90e3a-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e3a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e3a-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90e3a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e3a-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="90e3a-138">INPUTS</span></span>

### <span data-ttu-id="90e3a-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="90e3a-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="90e3a-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="90e3a-140">OUTPUTS</span></span>

### <span data-ttu-id="90e3a-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="90e3a-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="90e3a-142">Notas</span><span class="sxs-lookup"><span data-stu-id="90e3a-142">NOTES</span></span>

<span data-ttu-id="90e3a-143">Aliases</span><span class="sxs-lookup"><span data-stu-id="90e3a-143">ALIASES</span></span>

<span data-ttu-id="90e3a-144">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="90e3a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90e3a-145">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="90e3a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90e3a-146">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90e3a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90e3a-147">INPUTOBJECT: <ICustomProvidersIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="90e3a-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90e3a-148">`[AssociationName <String>]`: o nome da associação.</span><span class="sxs-lookup"><span data-stu-id="90e3a-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="90e3a-149">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="90e3a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90e3a-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90e3a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="90e3a-151">`[ResourceProviderName <String>]`: o nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="90e3a-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="90e3a-152">`[Scope <String>]`: o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="90e3a-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="90e3a-153">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="90e3a-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="90e3a-154">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="90e3a-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="90e3a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90e3a-155">RELATED LINKS</span></span>

