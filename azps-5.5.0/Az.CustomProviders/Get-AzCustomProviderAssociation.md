---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115884"
---
# <span data-ttu-id="1152b-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="1152b-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="1152b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1152b-102">SYNOPSIS</span></span>
<span data-ttu-id="1152b-103">Obter uma associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-103">Get an association.</span></span>

## <span data-ttu-id="1152b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1152b-104">SYNTAX</span></span>

### <span data-ttu-id="1152b-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1152b-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1152b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1152b-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1152b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1152b-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1152b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1152b-108">DESCRIPTION</span></span>
<span data-ttu-id="1152b-109">Obter uma associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-109">Get an association.</span></span>

## <span data-ttu-id="1152b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1152b-110">EXAMPLES</span></span>

### <span data-ttu-id="1152b-111">Exemplo 1: Listar associações de provedores personalizados</span><span class="sxs-lookup"><span data-stu-id="1152b-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="1152b-112">Liste todas as associações de provedores personalizados para um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="1152b-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="1152b-113">Exemplo 2: Obter uma associação</span><span class="sxs-lookup"><span data-stu-id="1152b-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="1152b-114">Obter detalhes de uma única associação CustomProvider</span><span class="sxs-lookup"><span data-stu-id="1152b-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="1152b-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1152b-115">PARAMETERS</span></span>

### <span data-ttu-id="1152b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1152b-116">-DefaultProfile</span></span>
<span data-ttu-id="1152b-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1152b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1152b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1152b-118">-InputObject</span></span>
<span data-ttu-id="1152b-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="1152b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1152b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1152b-120">-Name</span></span>
<span data-ttu-id="1152b-121">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1152b-122">-Escopo</span><span class="sxs-lookup"><span data-stu-id="1152b-122">-Scope</span></span>
<span data-ttu-id="1152b-123">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-123">The scope of the association.</span></span>

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

### <span data-ttu-id="1152b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1152b-124">CommonParameters</span></span>
<span data-ttu-id="1152b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1152b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1152b-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1152b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1152b-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="1152b-127">INPUTS</span></span>

### <span data-ttu-id="1152b-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="1152b-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="1152b-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="1152b-129">OUTPUTS</span></span>

### <span data-ttu-id="1152b-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="1152b-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="1152b-131">Notas</span><span class="sxs-lookup"><span data-stu-id="1152b-131">NOTES</span></span>

<span data-ttu-id="1152b-132">Aliases</span><span class="sxs-lookup"><span data-stu-id="1152b-132">ALIASES</span></span>

<span data-ttu-id="1152b-133">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="1152b-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1152b-134">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="1152b-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1152b-135">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1152b-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1152b-136">INPUTOBJECT: <ICustomProvidersIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="1152b-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1152b-137">`[AssociationName <String>]`: o nome da associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="1152b-138">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="1152b-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1152b-139">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1152b-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1152b-140">`[ResourceProviderName <String>]`: o nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="1152b-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="1152b-141">`[Scope <String>]`: o escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="1152b-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="1152b-142">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1152b-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="1152b-143">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="1152b-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="1152b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1152b-144">RELATED LINKS</span></span>

