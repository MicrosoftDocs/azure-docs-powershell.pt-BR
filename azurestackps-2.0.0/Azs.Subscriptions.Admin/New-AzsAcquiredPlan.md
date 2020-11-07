---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945146"
---
# <span data-ttu-id="8fc23-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="8fc23-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="8fc23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8fc23-102">SYNOPSIS</span></span>


## <span data-ttu-id="8fc23-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8fc23-103">SYNTAX</span></span>

### <span data-ttu-id="8fc23-104">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="8fc23-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8fc23-105">Criados</span><span class="sxs-lookup"><span data-stu-id="8fc23-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8fc23-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8fc23-106">DESCRIPTION</span></span>


## <span data-ttu-id="8fc23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8fc23-107">EXAMPLES</span></span>

### <span data-ttu-id="8fc23-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8fc23-108">Example 1</span></span>
```powershell
PS C:\> New-AzsAcquiredPlan -PlanAcquisitionId $([Guid]::NewGuid()) -PlanId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="8fc23-109">Crie um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="8fc23-109">Create a subscription plan.</span></span>

## <span data-ttu-id="8fc23-110">OS</span><span class="sxs-lookup"><span data-stu-id="8fc23-110">PARAMETERS</span></span>

### <span data-ttu-id="8fc23-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="8fc23-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="8fc23-112">Para construir, consulte a seção notas para propriedades ACQUIREDPLANDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8fc23-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-113">-Acquisitiontime</span><span class="sxs-lookup"><span data-stu-id="8fc23-113">-AcquisitionTime</span></span>


```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc23-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8fc23-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8fc23-115">-ExternalReferenceId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-116">-ID</span><span class="sxs-lookup"><span data-stu-id="8fc23-116">-Id</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="8fc23-117">-PlanAcquisitionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-118">-PlanID</span><span class="sxs-lookup"><span data-stu-id="8fc23-118">-PlanId</span></span>


```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="8fc23-119">-ProvisioningState</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fc23-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8fc23-121">-TargetSubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8fc23-122">-Confirm</span></span>
<span data-ttu-id="8fc23-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8fc23-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc23-124">-WhatIf</span></span>
<span data-ttu-id="8fc23-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8fc23-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc23-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8fc23-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8fc23-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc23-127">CommonParameters</span></span>
<span data-ttu-id="8fc23-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fc23-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc23-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fc23-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc23-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8fc23-130">INPUTS</span></span>

### <span data-ttu-id="8fc23-131">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fc23-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="8fc23-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8fc23-132">OUTPUTS</span></span>

### <span data-ttu-id="8fc23-133">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="8fc23-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="8fc23-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8fc23-134">ALIASES</span></span>

<span data-ttu-id="8fc23-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="8fc23-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="8fc23-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8fc23-136">NOTES</span></span>

<span data-ttu-id="8fc23-137">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8fc23-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8fc23-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8fc23-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8fc23-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="8fc23-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="8fc23-140">`[AcquisitionId <String>]`: Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="8fc23-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="8fc23-141">`[AcquisitionTime <DateTime?>]`: Tempo de aquisição.</span><span class="sxs-lookup"><span data-stu-id="8fc23-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="8fc23-142">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="8fc23-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="8fc23-143">`[Id <String>]`: Identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="8fc23-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="8fc23-144">`[PlanId <String>]`: Planejar identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="8fc23-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="8fc23-145">`[ProvisioningState <ProvisioningState?>]`: Estado do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="8fc23-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="8fc23-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8fc23-146">RELATED LINKS</span></span>

