---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281200"
---
# <span data-ttu-id="8b98a-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="8b98a-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="8b98a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b98a-102">SYNOPSIS</span></span>
<span data-ttu-id="8b98a-103">Obter uma associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-103">Get an association.</span></span>

## <span data-ttu-id="8b98a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b98a-104">SYNTAX</span></span>

### <span data-ttu-id="8b98a-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b98a-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b98a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8b98a-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b98a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8b98a-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b98a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b98a-108">DESCRIPTION</span></span>
<span data-ttu-id="8b98a-109">Obter uma associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-109">Get an association.</span></span>

## <span data-ttu-id="8b98a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b98a-110">EXAMPLES</span></span>

### <span data-ttu-id="8b98a-111">Exemplo 1: listar associações de provedor personalizado</span><span class="sxs-lookup"><span data-stu-id="8b98a-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="8b98a-112">Listar todas as associações de provedor personalizado para um determinado escopo.</span><span class="sxs-lookup"><span data-stu-id="8b98a-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="8b98a-113">Exemplo 2: obter uma associação</span><span class="sxs-lookup"><span data-stu-id="8b98a-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="8b98a-114">Obter detalhes de uma única Associação CustomProvider</span><span class="sxs-lookup"><span data-stu-id="8b98a-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="8b98a-115">OS</span><span class="sxs-lookup"><span data-stu-id="8b98a-115">PARAMETERS</span></span>

### <span data-ttu-id="8b98a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b98a-116">-DefaultProfile</span></span>
<span data-ttu-id="8b98a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b98a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b98a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b98a-118">-InputObject</span></span>
<span data-ttu-id="8b98a-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8b98a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8b98a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b98a-120">-Name</span></span>
<span data-ttu-id="8b98a-121">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-121">The name of the association.</span></span>

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

### <span data-ttu-id="8b98a-122">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8b98a-122">-Scope</span></span>
<span data-ttu-id="8b98a-123">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-123">The scope of the association.</span></span>

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

### <span data-ttu-id="8b98a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b98a-124">CommonParameters</span></span>
<span data-ttu-id="8b98a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b98a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b98a-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b98a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b98a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b98a-127">INPUTS</span></span>

### <span data-ttu-id="8b98a-128">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="8b98a-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="8b98a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b98a-129">OUTPUTS</span></span>

### <span data-ttu-id="8b98a-130">Microsoft. Azure. PowerShell. cmdlets. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="8b98a-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="8b98a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b98a-131">NOTES</span></span>

<span data-ttu-id="8b98a-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b98a-132">ALIASES</span></span>

<span data-ttu-id="8b98a-133">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8b98a-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b98a-134">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8b98a-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b98a-135">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b98a-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b98a-136">INPUTobject <ICustomProvidersIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8b98a-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b98a-137">`[AssociationName <String>]`: O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="8b98a-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8b98a-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b98a-139">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b98a-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="8b98a-140">`[ResourceProviderName <String>]`: O nome do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b98a-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="8b98a-141">`[Scope <String>]`: O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="8b98a-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="8b98a-142">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b98a-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="8b98a-143">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="8b98a-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="8b98a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b98a-144">RELATED LINKS</span></span>

