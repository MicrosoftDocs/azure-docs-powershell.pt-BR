---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 0db0f7ae4358e49ff62f94132701be1f4bd4d0b7
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945337"
---
# <span data-ttu-id="b4d8a-101">New-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="b4d8a-101">New-AzsAcquiredPlan</span></span>

## <span data-ttu-id="b4d8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4d8a-102">SYNOPSIS</span></span>


## <span data-ttu-id="b4d8a-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4d8a-103">SYNTAX</span></span>

### <span data-ttu-id="b4d8a-104">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4d8a-104">CreateExpanded (Default)</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> [-PlanAcquisitionId <String>] [-SubscriptionId <String>]
 [-AcquisitionTime <DateTime>] [-ExternalReferenceId <String>] [-Id <String>] [-PlanId <String>]
 [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d8a-105">Criados</span><span class="sxs-lookup"><span data-stu-id="b4d8a-105">Create</span></span>
```
New-AzsAcquiredPlan -TargetSubscriptionId <String> -AcquiredPlanDefinition <IPlanAcquisition>
 [-PlanAcquisitionId <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b4d8a-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4d8a-106">DESCRIPTION</span></span>


## <span data-ttu-id="b4d8a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4d8a-107">EXAMPLES</span></span>

### <span data-ttu-id="b4d8a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b4d8a-108">Example 1</span></span>
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

<span data-ttu-id="b4d8a-109">Crie um plano de assinatura.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-109">Create a subscription plan.</span></span>

## <span data-ttu-id="b4d8a-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4d8a-110">PARAMETERS</span></span>

### <span data-ttu-id="b4d8a-111">-AcquiredPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="b4d8a-111">-AcquiredPlanDefinition</span></span>
<span data-ttu-id="b4d8a-112">Para construir, consulte a seção notas para propriedades ACQUIREDPLANDEFINITION e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-112">To construct, see NOTES section for ACQUIREDPLANDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="b4d8a-113">-Acquisitiontime</span><span class="sxs-lookup"><span data-stu-id="b4d8a-113">-AcquisitionTime</span></span>


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

### <span data-ttu-id="b4d8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d8a-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="b4d8a-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="b4d8a-115">-ExternalReferenceId</span></span>


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

### <span data-ttu-id="b4d8a-116">-ID</span><span class="sxs-lookup"><span data-stu-id="b4d8a-116">-Id</span></span>


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

### <span data-ttu-id="b4d8a-117">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="b4d8a-117">-PlanAcquisitionId</span></span>


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

### <span data-ttu-id="b4d8a-118">-PlanID</span><span class="sxs-lookup"><span data-stu-id="b4d8a-118">-PlanId</span></span>


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

### <span data-ttu-id="b4d8a-119">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="b4d8a-119">-ProvisioningState</span></span>


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

### <span data-ttu-id="b4d8a-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4d8a-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="b4d8a-121">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4d8a-121">-TargetSubscriptionId</span></span>


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

### <span data-ttu-id="b4d8a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4d8a-122">-Confirm</span></span>
<span data-ttu-id="b4d8a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d8a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d8a-124">-WhatIf</span></span>
<span data-ttu-id="b4d8a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4d8a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d8a-127">CommonParameters</span></span>
<span data-ttu-id="b4d8a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d8a-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4d8a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d8a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4d8a-130">INPUTS</span></span>

### <span data-ttu-id="b4d8a-131">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="b4d8a-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

## <span data-ttu-id="b4d8a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4d8a-132">OUTPUTS</span></span>

### <span data-ttu-id="b4d8a-133">Microsoft. Azure. PowerShell. cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="b4d8a-133">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="b4d8a-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b4d8a-134">ALIASES</span></span>

<span data-ttu-id="b4d8a-135">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="b4d8a-135">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="b4d8a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4d8a-136">NOTES</span></span>

<span data-ttu-id="b4d8a-137">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b4d8a-138">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b4d8a-139">ACQUIREDPLANDEFINITION <IPlanAcquisition> :</span><span class="sxs-lookup"><span data-stu-id="b4d8a-139">ACQUIREDPLANDEFINITION <IPlanAcquisition>:</span></span> 
  - <span data-ttu-id="b4d8a-140">`[AcquisitionId <String>]`: Identificador de aquisição.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-140">`[AcquisitionId <String>]`: Acquisition identifier.</span></span>
  - <span data-ttu-id="b4d8a-141">`[AcquisitionTime <DateTime?>]`: Tempo de aquisição.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-141">`[AcquisitionTime <DateTime?>]`: Acquisition time.</span></span>
  - <span data-ttu-id="b4d8a-142">`[ExternalReferenceId <String>]`: Identificador de referência externa.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-142">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="b4d8a-143">`[Id <String>]`: Identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-143">`[Id <String>]`: Identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="b4d8a-144">`[PlanId <String>]`: Planejar identificador no contexto de assinatura do locatário.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-144">`[PlanId <String>]`: Plan identifier in the tenant subscription context.</span></span>
  - <span data-ttu-id="b4d8a-145">`[ProvisioningState <ProvisioningState?>]`: Estado do provisionamento.</span><span class="sxs-lookup"><span data-stu-id="b4d8a-145">`[ProvisioningState <ProvisioningState?>]`: State of the provisioning.</span></span>

## <span data-ttu-id="b4d8a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4d8a-146">RELATED LINKS</span></span>

