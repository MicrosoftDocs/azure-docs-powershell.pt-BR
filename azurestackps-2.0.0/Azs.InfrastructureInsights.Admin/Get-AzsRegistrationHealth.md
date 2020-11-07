---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776002"
---
# <span data-ttu-id="15085-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="15085-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="15085-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15085-102">SYNOPSIS</span></span>
<span data-ttu-id="15085-103">Retorna as informações de integridade solicitadas sobre um recurso.</span><span class="sxs-lookup"><span data-stu-id="15085-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="15085-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15085-104">SYNTAX</span></span>

### <span data-ttu-id="15085-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="15085-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15085-106">Obter</span><span class="sxs-lookup"><span data-stu-id="15085-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15085-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15085-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="15085-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15085-108">DESCRIPTION</span></span>
<span data-ttu-id="15085-109">Retorna as informações de integridade solicitadas sobre um recurso.</span><span class="sxs-lookup"><span data-stu-id="15085-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="15085-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15085-110">EXAMPLES</span></span>

### <span data-ttu-id="15085-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="15085-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="15085-112">Retorna uma lista da integridade de cada recurso em um serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="15085-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="15085-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="15085-114">Retorna o status de integridade em a para Microsoft. Fabric. admin.</span><span class="sxs-lookup"><span data-stu-id="15085-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="15085-115">OS</span><span class="sxs-lookup"><span data-stu-id="15085-115">PARAMETERS</span></span>

### <span data-ttu-id="15085-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15085-116">-DefaultProfile</span></span>
<span data-ttu-id="15085-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15085-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15085-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="15085-118">-Filter</span></span>
<span data-ttu-id="15085-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="15085-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15085-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15085-120">-InputObject</span></span>
<span data-ttu-id="15085-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="15085-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15085-122">-Local</span><span class="sxs-lookup"><span data-stu-id="15085-122">-Location</span></span>
<span data-ttu-id="15085-123">Nome da região</span><span class="sxs-lookup"><span data-stu-id="15085-123">Name of the region</span></span>

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

### <span data-ttu-id="15085-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15085-124">-ResourceGroupName</span></span>
<span data-ttu-id="15085-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15085-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="15085-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="15085-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="15085-127">ID do registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="15085-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="15085-128">-Registroid</span><span class="sxs-lookup"><span data-stu-id="15085-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="15085-129">ID de registro do serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-129">Service registration ID.</span></span>

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

### <span data-ttu-id="15085-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15085-130">-SubscriptionId</span></span>
<span data-ttu-id="15085-131">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="15085-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="15085-132">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15085-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15085-133">CommonParameters</span></span>
<span data-ttu-id="15085-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15085-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15085-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15085-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15085-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15085-136">INPUTS</span></span>

### <span data-ttu-id="15085-137">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="15085-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="15085-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15085-138">OUTPUTS</span></span>

### <span data-ttu-id="15085-139">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IResourceHealth</span><span class="sxs-lookup"><span data-stu-id="15085-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="15085-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15085-140">NOTES</span></span>

<span data-ttu-id="15085-141">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="15085-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15085-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15085-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="15085-143">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="15085-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15085-144">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="15085-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="15085-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="15085-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15085-146">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="15085-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="15085-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15085-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="15085-148">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="15085-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="15085-149">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="15085-150">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="15085-151">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="15085-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="15085-152">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="15085-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="15085-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15085-153">RELATED LINKS</span></span>

