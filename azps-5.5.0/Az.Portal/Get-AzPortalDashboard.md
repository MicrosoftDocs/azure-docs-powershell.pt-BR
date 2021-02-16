---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/get-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Get-AzPortalDashboard.md
ms.openlocfilehash: aa11a9828c422069823226b2d5df57efc84f8c7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113378"
---
# <span data-ttu-id="721a6-101">Get-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="721a6-101">Get-AzPortalDashboard</span></span>

## <span data-ttu-id="721a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="721a6-102">SYNOPSIS</span></span>
<span data-ttu-id="721a6-103">Obtém o Painel.</span><span class="sxs-lookup"><span data-stu-id="721a6-103">Gets the Dashboard.</span></span>

## <span data-ttu-id="721a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="721a6-104">SYNTAX</span></span>

### <span data-ttu-id="721a6-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="721a6-105">List1 (Default)</span></span>
```
Get-AzPortalDashboard [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="721a6-106">Obter</span><span class="sxs-lookup"><span data-stu-id="721a6-106">Get</span></span>
```
Get-AzPortalDashboard -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="721a6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="721a6-107">GetViaIdentity</span></span>
```
Get-AzPortalDashboard -InputObject <IPortalIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="721a6-108">Lista</span><span class="sxs-lookup"><span data-stu-id="721a6-108">List</span></span>
```
Get-AzPortalDashboard -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="721a6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="721a6-109">DESCRIPTION</span></span>
<span data-ttu-id="721a6-110">Obtém o Painel.</span><span class="sxs-lookup"><span data-stu-id="721a6-110">Gets the Dashboard.</span></span>

## <span data-ttu-id="721a6-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="721a6-111">EXAMPLES</span></span>

### <span data-ttu-id="721a6-112">Exemplo 1: Listar todos os painéis de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="721a6-112">Example 1: List all dashboards in a subscription</span></span>
```powershell
PS C:> Get-AzPortalDashboard                                                                                                                     
Location Name                                           Type
-------- ----                                           ----
eastasia my-custom-dashboard1                           Microsoft.Portal/dashboards
westus   my-second-custom-dashboard1                    Microsoft.Portal/dashboards

```

<span data-ttu-id="721a6-113">Listar todos os painéis de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="721a6-113">List all dashboards in a subscription</span></span>

### <span data-ttu-id="721a6-114">Exemplo 2: Obter detalhes para um único Painel de Portal</span><span class="sxs-lookup"><span data-stu-id="721a6-114">Example 2: Get details for a single Portal Dashboard</span></span>
```powershell
PS C:\> Get-AzPortalDashboard -ResourceGroupName my-rg -Name mydashboard

Location Name        Type
-------- ----        ----
eastus   mydashboard Microsoft.Portal/dashboards
```

<span data-ttu-id="721a6-115">Obter detalhes de um único painel</span><span class="sxs-lookup"><span data-stu-id="721a6-115">Get details for a single dashboard</span></span>

## <span data-ttu-id="721a6-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="721a6-116">PARAMETERS</span></span>

### <span data-ttu-id="721a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721a6-117">-DefaultProfile</span></span>
<span data-ttu-id="721a6-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="721a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="721a6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="721a6-119">-InputObject</span></span>
<span data-ttu-id="721a6-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="721a6-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="721a6-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="721a6-121">-Name</span></span>
<span data-ttu-id="721a6-122">O nome do painel.</span><span class="sxs-lookup"><span data-stu-id="721a6-122">The name of the dashboard.</span></span>

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

### <span data-ttu-id="721a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="721a6-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="721a6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="721a6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="721a6-125">-SubscriptionId</span></span>
<span data-ttu-id="721a6-126">A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="721a6-126">The Azure subscription ID.</span></span>
<span data-ttu-id="721a6-127">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="721a6-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="721a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721a6-128">CommonParameters</span></span>
<span data-ttu-id="721a6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721a6-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="721a6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721a6-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="721a6-131">INPUTS</span></span>

### <span data-ttu-id="721a6-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span><span class="sxs-lookup"><span data-stu-id="721a6-132">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.IPortalIdentity</span></span>

## <span data-ttu-id="721a6-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="721a6-133">OUTPUTS</span></span>

### <span data-ttu-id="721a6-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="721a6-134">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="721a6-135">Notas</span><span class="sxs-lookup"><span data-stu-id="721a6-135">NOTES</span></span>

<span data-ttu-id="721a6-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="721a6-136">ALIASES</span></span>

<span data-ttu-id="721a6-137">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="721a6-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="721a6-138">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="721a6-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="721a6-139">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="721a6-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="721a6-140">INPUTOBJECT: <IPortalIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="721a6-140">INPUTOBJECT <IPortalIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="721a6-141">`[DashboardName <String>]`: o nome do painel.</span><span class="sxs-lookup"><span data-stu-id="721a6-141">`[DashboardName <String>]`: The name of the dashboard.</span></span>
  - <span data-ttu-id="721a6-142">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="721a6-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="721a6-143">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="721a6-143">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="721a6-144">`[SubscriptionId <String>]`: A ID de assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="721a6-144">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="721a6-145">Esta é uma cadeia de caracteres formatada como GUID (por exemplo, 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="721a6-145">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="721a6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="721a6-146">RELATED LINKS</span></span>

