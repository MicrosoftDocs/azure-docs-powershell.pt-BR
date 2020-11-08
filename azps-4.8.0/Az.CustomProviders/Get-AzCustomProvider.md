---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115067"
---
# <span data-ttu-id="c8a54-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="c8a54-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="c8a54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8a54-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a54-103">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8a54-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="c8a54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8a54-104">SYNTAX</span></span>

### <span data-ttu-id="c8a54-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="c8a54-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8a54-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c8a54-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8a54-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c8a54-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c8a54-108">Programação</span><span class="sxs-lookup"><span data-stu-id="c8a54-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a54-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8a54-109">DESCRIPTION</span></span>
<span data-ttu-id="c8a54-110">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8a54-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="c8a54-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8a54-111">EXAMPLES</span></span>

### <span data-ttu-id="c8a54-112">Exemplo 1: listar todos os provedores personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c8a54-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="c8a54-113">Lista todos os provedores personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="c8a54-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="c8a54-114">Exemplo 2: obter um único provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="c8a54-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="c8a54-115">Obtém detalhes de um único provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8a54-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="c8a54-116">Use Format-List para mostrar detalhes do objeto na tela.</span><span class="sxs-lookup"><span data-stu-id="c8a54-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="c8a54-117">OS</span><span class="sxs-lookup"><span data-stu-id="c8a54-117">PARAMETERS</span></span>

### <span data-ttu-id="c8a54-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a54-118">-DefaultProfile</span></span>
<span data-ttu-id="c8a54-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a54-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a54-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a54-120">-InputObject</span></span>
<span data-ttu-id="c8a54-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c8a54-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c8a54-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8a54-122">-Name</span></span>
<span data-ttu-id="c8a54-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a54-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="c8a54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a54-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8a54-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a54-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c8a54-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8a54-126">-SubscriptionId</span></span>
<span data-ttu-id="c8a54-127">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a54-127">The Azure subscription ID.</span></span>
<span data-ttu-id="c8a54-128">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c8a54-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="c8a54-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a54-129">CommonParameters</span></span>
<span data-ttu-id="c8a54-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a54-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a54-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a54-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a54-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8a54-132">INPUTS</span></span>

### <span data-ttu-id="c8a54-133">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="c8a54-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="c8a54-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8a54-134">OUTPUTS</span></span>

### <span data-ttu-id="c8a54-135">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="c8a54-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="c8a54-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8a54-136">NOTES</span></span>

<span data-ttu-id="c8a54-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c8a54-137">ALIASES</span></span>

<span data-ttu-id="c8a54-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c8a54-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c8a54-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c8a54-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c8a54-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c8a54-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c8a54-141">INPUTobject <ICustomProvidersIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c8a54-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c8a54-142">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="c8a54-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="c8a54-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c8a54-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c8a54-144">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a54-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c8a54-145">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a54-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="c8a54-146">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="c8a54-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="c8a54-147">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a54-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="c8a54-148">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="c8a54-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="c8a54-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a54-149">RELATED LINKS</span></span>

