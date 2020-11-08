---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114282"
---
# <span data-ttu-id="a3023-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a3023-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="a3023-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3023-102">SYNOPSIS</span></span>
<span data-ttu-id="a3023-103">Obtém o painel.</span><span class="sxs-lookup"><span data-stu-id="a3023-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="a3023-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3023-104">SYNTAX</span></span>

### <span data-ttu-id="a3023-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3023-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3023-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a3023-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3023-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3023-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a3023-108">Programação</span><span class="sxs-lookup"><span data-stu-id="a3023-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3023-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3023-109">DESCRIPTION</span></span>
<span data-ttu-id="a3023-110">Obtém o painel.</span><span class="sxs-lookup"><span data-stu-id="a3023-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="a3023-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3023-111">EXAMPLES</span></span>

### <span data-ttu-id="a3023-112">Exemplo 1: listar todos os painéis em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a3023-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="a3023-113">Listar todos os painéis em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="a3023-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="a3023-114">Exemplo 2: obter detalhes para um único painel do portal</span><span class="sxs-lookup"><span data-stu-id="a3023-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="a3023-115">Obter detalhes para um único painel</span><span class="sxs-lookup"><span data-stu-id="a3023-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="a3023-116">OS</span><span class="sxs-lookup"><span data-stu-id="a3023-116">PARAMETERS</span></span>

### <span data-ttu-id="a3023-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3023-117">-DefaultProfile</span></span>
<span data-ttu-id="a3023-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3023-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3023-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3023-119">-InputObject</span></span>
<span data-ttu-id="a3023-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a3023-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3023-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3023-121">-Name</span></span>
<span data-ttu-id="a3023-122">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="a3023-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="a3023-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3023-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3023-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3023-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3023-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3023-125">-SubscriptionId</span></span>
<span data-ttu-id="a3023-126">A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3023-126">The Azure subscription ID.</span></span>
<span data-ttu-id="a3023-127">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a3023-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="a3023-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3023-128">CommonParameters</span></span>
<span data-ttu-id="a3023-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3023-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3023-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3023-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3023-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3023-131">INPUTS</span></span>

### <span data-ttu-id="a3023-132">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="a3023-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="a3023-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3023-133">OUTPUTS</span></span>

### <span data-ttu-id="a3023-134">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="a3023-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a3023-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3023-135">NOTES</span></span>

<span data-ttu-id="a3023-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a3023-136">ALIASES</span></span>

<span data-ttu-id="a3023-137">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a3023-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3023-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a3023-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3023-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3023-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3023-140">INPUTobject <IPortalIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a3023-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3023-141">`[DashboardName <String>]`: O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="a3023-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="a3023-142">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a3023-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3023-143">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3023-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a3023-144">`[SubscriptionId <String>]`: A ID da assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3023-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="a3023-145">Esta é uma cadeia de caracteres formatada por GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="a3023-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="a3023-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3023-146">RELATED LINKS</span></span>

