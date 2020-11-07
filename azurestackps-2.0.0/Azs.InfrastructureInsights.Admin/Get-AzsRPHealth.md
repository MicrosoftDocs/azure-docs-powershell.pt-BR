---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776005"
---
# <span data-ttu-id="ede38-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="ede38-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="ede38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ede38-102">SYNOPSIS</span></span>
<span data-ttu-id="ede38-103">Retorna o objeto de integridade do serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="ede38-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="ede38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ede38-104">SYNTAX</span></span>

### <span data-ttu-id="ede38-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ede38-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ede38-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ede38-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ede38-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ede38-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ede38-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ede38-108">DESCRIPTION</span></span>
<span data-ttu-id="ede38-109">Retorna o objeto de integridade do serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="ede38-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="ede38-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ede38-110">EXAMPLES</span></span>

### <span data-ttu-id="ede38-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="ede38-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="ede38-112">Retorna uma lista da integridade de cada serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="ede38-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="ede38-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="ede38-114">Retorna a integridade de um serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-114">Returns a service's health.</span></span>

## <span data-ttu-id="ede38-115">OS</span><span class="sxs-lookup"><span data-stu-id="ede38-115">PARAMETERS</span></span>

### <span data-ttu-id="ede38-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede38-116">-DefaultProfile</span></span>
<span data-ttu-id="ede38-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ede38-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede38-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="ede38-118">-Filter</span></span>
<span data-ttu-id="ede38-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="ede38-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="ede38-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ede38-120">-InputObject</span></span>
<span data-ttu-id="ede38-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ede38-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ede38-122">-Local</span><span class="sxs-lookup"><span data-stu-id="ede38-122">-Location</span></span>
<span data-ttu-id="ede38-123">Nome da região</span><span class="sxs-lookup"><span data-stu-id="ede38-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ede38-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede38-124">-ResourceGroupName</span></span>
<span data-ttu-id="ede38-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ede38-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="ede38-126">-Outhealth</span><span class="sxs-lookup"><span data-stu-id="ede38-126">-ServiceHealth</span></span>
<span data-ttu-id="ede38-127">Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-127">Service Health name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ede38-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ede38-128">-SubscriptionId</span></span>
<span data-ttu-id="ede38-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ede38-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ede38-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ede38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede38-131">CommonParameters</span></span>
<span data-ttu-id="ede38-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ede38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede38-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ede38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede38-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ede38-134">INPUTS</span></span>

### <span data-ttu-id="ede38-135">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ede38-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="ede38-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ede38-136">OUTPUTS</span></span>

### <span data-ttu-id="ede38-137">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="ede38-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="ede38-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ede38-138">NOTES</span></span>

<span data-ttu-id="ede38-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ede38-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ede38-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ede38-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ede38-141">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ede38-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ede38-142">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="ede38-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="ede38-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ede38-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ede38-144">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="ede38-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="ede38-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ede38-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ede38-146">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="ede38-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="ede38-147">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="ede38-148">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="ede38-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ede38-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ede38-150">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ede38-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ede38-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ede38-151">RELATED LINKS</span></span>

