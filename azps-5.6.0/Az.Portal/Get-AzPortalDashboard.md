---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: fc888161df56e3edbf1a51014c7173542e395ad3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890098"
---
# <span data-ttu-id="a969c-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a969c-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="a969c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a969c-102">SYNOPSIS</span></span>
<span data-ttu-id="a969c-103">Obtém o Painel.</span><span class="sxs-lookup"><span data-stu-id="a969c-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="a969c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a969c-104">SYNTAX</span></span>

### <span data-ttu-id="a969c-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a969c-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a969c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a969c-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a969c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a969c-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a969c-108">Listar</span><span class="sxs-lookup"><span data-stu-id="a969c-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a969c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a969c-109">DESCRIPTION</span></span>
<span data-ttu-id="a969c-110">Obtém o Painel.</span><span class="sxs-lookup"><span data-stu-id="a969c-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="a969c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a969c-111">EXAMPLES</span></span>

### <span data-ttu-id="a969c-112">Exemplo 1: Listar todos os painéis em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a969c-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="a969c-113">Listar todos os painéis em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a969c-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="a969c-114">Exemplo 2: Obter detalhes para um único Painel de Portal</span><span class="sxs-lookup"><span data-stu-id="a969c-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="a969c-115">Obter detalhes para um único painel</span><span class="sxs-lookup"><span data-stu-id="a969c-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="a969c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a969c-116">PARAMETERS</span></span>

### <span data-ttu-id="a969c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a969c-117">-DefaultProfile</span></span>
<span data-ttu-id="a969c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a969c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a969c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a969c-119">-InputObject</span></span>
<span data-ttu-id="a969c-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a969c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a969c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a969c-121">-Name</span></span>
<span data-ttu-id="a969c-122">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="a969c-122">The name of the dashboard.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a969c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a969c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a969c-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a969c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a969c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a969c-125">-SubscriptionId</span></span>
<span data-ttu-id="a969c-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a969c-126">The Azure subscription ID.</span></span>
<span data-ttu-id="a969c-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="a969c-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a969c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a969c-128">CommonParameters</span></span>
<span data-ttu-id="a969c-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a969c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a969c-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a969c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a969c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a969c-131">INPUTS</span></span>

### <span data-ttu-id="a969c-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="a969c-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="a969c-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a969c-133">OUTPUTS</span></span>

### <span data-ttu-id="a969c-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="a969c-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a969c-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="a969c-135">NOTES</span></span>

<span data-ttu-id="a969c-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a969c-136">ALIASES</span></span>

<span data-ttu-id="a969c-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a969c-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a969c-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a969c-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a969c-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a969c-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a969c-140">INPUTOBJECT <IPortalIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a969c-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a969c-141">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="a969c-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="a969c-142">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a969c-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a969c-143">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a969c-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a969c-144">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a969c-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a969c-145">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 000000000-0000-0000-0000-0000000000000000)</span><span class="sxs-lookup"><span data-stu-id="a969c-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a969c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a969c-146">RELATED LINKS</span></span>

