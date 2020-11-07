---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777107"
---
# <span data-ttu-id="aaef8-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="aaef8-101">Get-AzsAlert</span></span>

## <span data-ttu-id="aaef8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aaef8-102">SYNOPSIS</span></span>
<span data-ttu-id="aaef8-103">Retorna o alerta solicitado.</span><span class="sxs-lookup"><span data-stu-id="aaef8-103">Returns the requested alert.</span></span>

## <span data-ttu-id="aaef8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aaef8-104">SYNTAX</span></span>

### <span data-ttu-id="aaef8-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="aaef8-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaef8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="aaef8-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="aaef8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaef8-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="aaef8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aaef8-108">DESCRIPTION</span></span>
<span data-ttu-id="aaef8-109">Retorna o alerta solicitado.</span><span class="sxs-lookup"><span data-stu-id="aaef8-109">Returns the requested alert.</span></span>

## <span data-ttu-id="aaef8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aaef8-110">EXAMPLES</span></span>

### <span data-ttu-id="aaef8-111">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="aaef8-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="aaef8-112">Obter um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="aaef8-112">Get an alert by Name.</span></span>

### <span data-ttu-id="aaef8-113">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="aaef8-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="aaef8-114">Obter todos os alertas ativos e exibir a falha e o cargo.</span><span class="sxs-lookup"><span data-stu-id="aaef8-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="aaef8-115">OS</span><span class="sxs-lookup"><span data-stu-id="aaef8-115">PARAMETERS</span></span>

### <span data-ttu-id="aaef8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaef8-116">-DefaultProfile</span></span>
<span data-ttu-id="aaef8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aaef8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaef8-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="aaef8-118">-Filter</span></span>
<span data-ttu-id="aaef8-119">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="aaef8-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="aaef8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaef8-120">-InputObject</span></span>
<span data-ttu-id="aaef8-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="aaef8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aaef8-122">-Local</span><span class="sxs-lookup"><span data-stu-id="aaef8-122">-Location</span></span>
<span data-ttu-id="aaef8-123">Nome da região</span><span class="sxs-lookup"><span data-stu-id="aaef8-123">Name of the region</span></span>

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

### <span data-ttu-id="aaef8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="aaef8-124">-Name</span></span>
<span data-ttu-id="aaef8-125">Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="aaef8-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aaef8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaef8-126">-ResourceGroupName</span></span>
<span data-ttu-id="aaef8-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aaef8-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="aaef8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaef8-128">-SubscriptionId</span></span>
<span data-ttu-id="aaef8-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aaef8-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aaef8-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aaef8-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aaef8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaef8-131">CommonParameters</span></span>
<span data-ttu-id="aaef8-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaef8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaef8-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaef8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaef8-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aaef8-134">INPUTS</span></span>

### <span data-ttu-id="aaef8-135">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="aaef8-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="aaef8-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aaef8-136">OUTPUTS</span></span>

### <span data-ttu-id="aaef8-137">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="aaef8-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="aaef8-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aaef8-138">NOTES</span></span>

<span data-ttu-id="aaef8-139">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="aaef8-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaef8-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaef8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aaef8-141">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="aaef8-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaef8-142">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="aaef8-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="aaef8-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="aaef8-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaef8-144">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="aaef8-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="aaef8-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aaef8-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="aaef8-146">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="aaef8-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="aaef8-147">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="aaef8-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="aaef8-148">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="aaef8-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="aaef8-149">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aaef8-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aaef8-150">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="aaef8-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="aaef8-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aaef8-151">RELATED LINKS</span></span>

