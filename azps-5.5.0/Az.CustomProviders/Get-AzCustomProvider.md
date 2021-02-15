---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112007"
---
# <span data-ttu-id="364ac-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="364ac-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="364ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="364ac-102">SYNOPSIS</span></span>
<span data-ttu-id="364ac-103">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="364ac-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="364ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="364ac-104">SYNTAX</span></span>

### <span data-ttu-id="364ac-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="364ac-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="364ac-106">Obter</span><span class="sxs-lookup"><span data-stu-id="364ac-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="364ac-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="364ac-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="364ac-108">Lista</span><span class="sxs-lookup"><span data-stu-id="364ac-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="364ac-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="364ac-109">DESCRIPTION</span></span>
<span data-ttu-id="364ac-110">Obtém o manifesto do provedor de recursos personalizado.</span><span class="sxs-lookup"><span data-stu-id="364ac-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="364ac-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="364ac-111">EXAMPLES</span></span>

### <span data-ttu-id="364ac-112">Exemplo 1: Listar todos os Provedores Personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="364ac-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="364ac-113">Lista todos os provedores personalizados em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="364ac-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="364ac-114">Exemplo 2: Obter um único provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="364ac-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="364ac-115">Obtém detalhes de um único provedor personalizado.</span><span class="sxs-lookup"><span data-stu-id="364ac-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="364ac-116">Use Format-List para mostrar detalhes do objeto na tela.</span><span class="sxs-lookup"><span data-stu-id="364ac-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="364ac-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="364ac-117">PARAMETERS</span></span>

### <span data-ttu-id="364ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364ac-118">-DefaultProfile</span></span>
<span data-ttu-id="364ac-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="364ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="364ac-120">-InputObject</span></span>
<span data-ttu-id="364ac-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="364ac-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="364ac-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="364ac-122">-Name</span></span>
<span data-ttu-id="364ac-123">O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="364ac-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="364ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="364ac-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="364ac-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="364ac-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="364ac-126">-SubscriptionId</span></span>
<span data-ttu-id="364ac-127">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="364ac-127">The Azure subscription ID.</span></span>
<span data-ttu-id="364ac-128">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="364ac-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="364ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364ac-129">CommonParameters</span></span>
<span data-ttu-id="364ac-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364ac-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="364ac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364ac-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="364ac-132">INPUTS</span></span>

### <span data-ttu-id="364ac-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="364ac-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="364ac-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="364ac-134">OUTPUTS</span></span>

### <span data-ttu-id="364ac-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="364ac-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="364ac-136">Notas</span><span class="sxs-lookup"><span data-stu-id="364ac-136">NOTES</span></span>

<span data-ttu-id="364ac-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="364ac-137">ALIASES</span></span>

<span data-ttu-id="364ac-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="364ac-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="364ac-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="364ac-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="364ac-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="364ac-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="364ac-141">INPUTOBJECT: <ICustomProvidersIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="364ac-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="364ac-142">`[AssociationName <String>]`: o nome da associação.</span><span class="sxs-lookup"><span data-stu-id="364ac-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="364ac-143">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="364ac-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="364ac-144">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="364ac-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="364ac-145">`[ResourceProviderName <String>]`: o nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="364ac-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="364ac-146">`[Scope <String>]`: o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="364ac-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="364ac-147">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="364ac-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="364ac-148">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="364ac-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="364ac-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="364ac-149">RELATED LINKS</span></span>

