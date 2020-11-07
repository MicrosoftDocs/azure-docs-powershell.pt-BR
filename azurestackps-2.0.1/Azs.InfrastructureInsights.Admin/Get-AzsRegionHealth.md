---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945288"
---
# <span data-ttu-id="3f9e1-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="3f9e1-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="3f9e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9e1-103">Retorna o status de integridade solicitado de uma região.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="3f9e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f9e1-104">SYNTAX</span></span>

### <span data-ttu-id="3f9e1-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f9e1-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f9e1-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3f9e1-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f9e1-107">Programação</span><span class="sxs-lookup"><span data-stu-id="3f9e1-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3f9e1-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f9e1-108">DESCRIPTION</span></span>
<span data-ttu-id="3f9e1-109">Retorna o status de integridade solicitado de uma região.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="3f9e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f9e1-110">EXAMPLES</span></span>

### <span data-ttu-id="3f9e1-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="3f9e1-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="3f9e1-112">Retorna uma lista de status de integridade da região.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="3f9e1-113">OS</span><span class="sxs-lookup"><span data-stu-id="3f9e1-113">PARAMETERS</span></span>

### <span data-ttu-id="3f9e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9e1-114">-DefaultProfile</span></span>
<span data-ttu-id="3f9e1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f9e1-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3f9e1-116">-Filter</span></span>
<span data-ttu-id="3f9e1-117">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f9e1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f9e1-118">-InputObject</span></span>
<span data-ttu-id="3f9e1-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3f9e1-120">-Local</span><span class="sxs-lookup"><span data-stu-id="3f9e1-120">-Location</span></span>
<span data-ttu-id="3f9e1-121">Nome da região</span><span class="sxs-lookup"><span data-stu-id="3f9e1-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f9e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f9e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f9e1-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f9e1-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f9e1-124">-SubscriptionId</span></span>
<span data-ttu-id="3f9e1-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3f9e1-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3f9e1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9e1-127">CommonParameters</span></span>
<span data-ttu-id="3f9e1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9e1-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f9e1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9e1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f9e1-130">INPUTS</span></span>

### <span data-ttu-id="3f9e1-131">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3f9e1-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="3f9e1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f9e1-132">OUTPUTS</span></span>

### <span data-ttu-id="3f9e1-133">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="3f9e1-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="3f9e1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f9e1-134">NOTES</span></span>

<span data-ttu-id="3f9e1-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3f9e1-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3f9e1-137">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3f9e1-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3f9e1-138">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="3f9e1-139">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3f9e1-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3f9e1-140">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="3f9e1-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="3f9e1-141">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3f9e1-142">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="3f9e1-143">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="3f9e1-144">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="3f9e1-145">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3f9e1-146">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3f9e1-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3f9e1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f9e1-147">RELATED LINKS</span></span>

