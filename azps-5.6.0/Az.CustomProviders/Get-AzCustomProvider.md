---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 287472f89e7875411e287fa1315d5622a4c48a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891405"
---
# <span data-ttu-id="6b8bd-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="6b8bd-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="6b8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8bd-103">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6b8bd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6b8bd-104">SYNTAX</span></span>

### <span data-ttu-id="6b8bd-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6b8bd-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b8bd-106">Obter</span><span class="sxs-lookup"><span data-stu-id="6b8bd-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b8bd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6b8bd-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6b8bd-108">Listar</span><span class="sxs-lookup"><span data-stu-id="6b8bd-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b8bd-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6b8bd-109">DESCRIPTION</span></span>
<span data-ttu-id="6b8bd-110">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6b8bd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-111">EXAMPLES</span></span>

### <span data-ttu-id="6b8bd-112">Exemplo 1: Listar todos os Provedores Personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="6b8bd-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="6b8bd-113">Lista todos os provedores personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="6b8bd-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="6b8bd-114">Exemplo 2: Obter um único provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="6b8bd-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="6b8bd-115">Obtém detalhes de um único provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="6b8bd-116">Use Format-List para mostrar detalhes do objeto na tela.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="6b8bd-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-117">PARAMETERS</span></span>

### <span data-ttu-id="6b8bd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8bd-118">-DefaultProfile</span></span>
<span data-ttu-id="6b8bd-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b8bd-120">-InputObject</span></span>
<span data-ttu-id="6b8bd-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b8bd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b8bd-122">-Name</span></span>
<span data-ttu-id="6b8bd-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b8bd-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8bd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6b8bd-126">-SubscriptionId</span></span>
<span data-ttu-id="6b8bd-127">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-127">The Azure subscription ID.</span></span>
<span data-ttu-id="6b8bd-128">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="6b8bd-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b8bd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8bd-129">CommonParameters</span></span>
<span data-ttu-id="6b8bd-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8bd-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b8bd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8bd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-132">INPUTS</span></span>

### <span data-ttu-id="6b8bd-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="6b8bd-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="6b8bd-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-134">OUTPUTS</span></span>

### <span data-ttu-id="6b8bd-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="6b8bd-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="6b8bd-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="6b8bd-136">NOTES</span></span>

<span data-ttu-id="6b8bd-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6b8bd-137">ALIASES</span></span>

<span data-ttu-id="6b8bd-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="6b8bd-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b8bd-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b8bd-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b8bd-141">INPUTOBJECT <ICustomProvidersIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="6b8bd-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6b8bd-142">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="6b8bd-143">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="6b8bd-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6b8bd-144">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6b8bd-145">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="6b8bd-146">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="6b8bd-147">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8bd-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6b8bd-148">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="6b8bd-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6b8bd-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b8bd-149">RELATED LINKS</span></span>

