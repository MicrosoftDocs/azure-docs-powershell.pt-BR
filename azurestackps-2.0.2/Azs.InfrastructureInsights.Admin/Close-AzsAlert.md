---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/08/2020
ms.locfileid: "93946975"
---
# <span data-ttu-id="24e25-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="24e25-101">Close-AzsAlert</span></span>

## <span data-ttu-id="24e25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24e25-102">SYNOPSIS</span></span>
<span data-ttu-id="24e25-103">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="24e25-103">Closes the given alert.</span></span>

## <span data-ttu-id="24e25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24e25-104">SYNTAX</span></span>

### <span data-ttu-id="24e25-105">CloseExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="24e25-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24e25-106">Proximidade</span><span class="sxs-lookup"><span data-stu-id="24e25-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="24e25-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24e25-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="24e25-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="24e25-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24e25-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24e25-109">DESCRIPTION</span></span>
<span data-ttu-id="24e25-110">Fecha o alerta fornecido.</span><span class="sxs-lookup"><span data-stu-id="24e25-110">Closes the given alert.</span></span>

## <span data-ttu-id="24e25-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24e25-111">EXAMPLES</span></span>

### <span data-ttu-id="24e25-112">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="24e25-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="24e25-113">Fechar um alerta por nome.</span><span class="sxs-lookup"><span data-stu-id="24e25-113">Close an alert by Name.</span></span>

### <span data-ttu-id="24e25-114">Exemplo 2:</span><span class="sxs-lookup"><span data-stu-id="24e25-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="24e25-115">Fechar um alerta por meio do encanamento.</span><span class="sxs-lookup"><span data-stu-id="24e25-115">Close an alert through piping.</span></span>

## <span data-ttu-id="24e25-116">OS</span><span class="sxs-lookup"><span data-stu-id="24e25-116">PARAMETERS</span></span>

### <span data-ttu-id="24e25-117">-Alerta</span><span class="sxs-lookup"><span data-stu-id="24e25-117">-Alert</span></span>
<span data-ttu-id="24e25-118">Esse objeto representa um recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-118">This object represents an alert resource.</span></span>
<span data-ttu-id="24e25-119">Para construir, consulte a seção anotações para obter as propriedades do alerta e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="24e25-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-120">-Alertid</span><span class="sxs-lookup"><span data-stu-id="24e25-120">-AlertId</span></span>
<span data-ttu-id="24e25-121">Obtém ou define a ID do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-122">-Alertproperty</span><span class="sxs-lookup"><span data-stu-id="24e25-122">-AlertProperty</span></span>
<span data-ttu-id="24e25-123">Propriedades do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="24e25-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="24e25-125">Alias do usuário que fechou o alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="24e25-126">-ClosedTimestamp</span></span>
<span data-ttu-id="24e25-127">Carimbo de data/hora em que o alerta foi fechado.</span><span class="sxs-lookup"><span data-stu-id="24e25-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="24e25-128">-CreatedTimestamp</span></span>
<span data-ttu-id="24e25-129">Carimbo de data/hora em que o alerta foi criado.</span><span class="sxs-lookup"><span data-stu-id="24e25-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e25-130">-DefaultProfile</span></span>
<span data-ttu-id="24e25-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24e25-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24e25-132">-Descrição</span><span class="sxs-lookup"><span data-stu-id="24e25-132">-Description</span></span>
<span data-ttu-id="24e25-133">Descrição do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-134">-Faultid</span><span class="sxs-lookup"><span data-stu-id="24e25-134">-FaultId</span></span>
<span data-ttu-id="24e25-135">Obtém ou define a identificação da falha do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="24e25-136">-FaultTypeId</span></span>
<span data-ttu-id="24e25-137">Obtém ou define a ID do tipo de falha do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="24e25-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="24e25-139">Indica se o alerta pode ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="24e25-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="24e25-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="24e25-141">Nome para exibição do item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="24e25-142">-ImpactedResourceId</span></span>
<span data-ttu-id="24e25-143">Obtém ou define a ID do recurso para o item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24e25-144">-InputObject</span></span>
<span data-ttu-id="24e25-145">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="24e25-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="24e25-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="24e25-147">Carimbo de data/hora em que o alerta foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="24e25-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-148">-Local</span><span class="sxs-lookup"><span data-stu-id="24e25-148">-Location</span></span>
<span data-ttu-id="24e25-149">Nome da região</span><span class="sxs-lookup"><span data-stu-id="24e25-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="24e25-150">-Location1</span></span>
<span data-ttu-id="24e25-151">A região do Azure na qual o recurso reside</span><span class="sxs-lookup"><span data-stu-id="24e25-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="24e25-152">-Name</span></span>
<span data-ttu-id="24e25-153">Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-154">-Correção</span><span class="sxs-lookup"><span data-stu-id="24e25-154">-Remediation</span></span>
<span data-ttu-id="24e25-155">Obtém ou define as instruções de correção amigável do administrador para o alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e25-156">-ResourceGroupName</span></span>
<span data-ttu-id="24e25-157">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e25-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="24e25-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="24e25-159">Obtém ou define a ID de registro do serviço ao qual o alerta pertence.</span><span class="sxs-lookup"><span data-stu-id="24e25-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="24e25-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="24e25-161">Obtém ou define a identificação de registro do recurso associado ao alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="24e25-162">Se o alerta não estiver associado a um recurso, a identificação de registro do recurso será nula.</span><span class="sxs-lookup"><span data-stu-id="24e25-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-163">-Severidade</span><span class="sxs-lookup"><span data-stu-id="24e25-163">-Severity</span></span>
<span data-ttu-id="24e25-164">Gravidade do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-165">-Estado</span><span class="sxs-lookup"><span data-stu-id="24e25-165">-State</span></span>
<span data-ttu-id="24e25-166">Estado do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24e25-167">-SubscriptionId</span></span>
<span data-ttu-id="24e25-168">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24e25-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24e25-169">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="24e25-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-170">-Marca</span><span class="sxs-lookup"><span data-stu-id="24e25-170">-Tag</span></span>
<span data-ttu-id="24e25-171">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="24e25-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-172">-Título</span><span class="sxs-lookup"><span data-stu-id="24e25-172">-Title</span></span>
<span data-ttu-id="24e25-173">Obtém ou define a ID do recurso para o item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="24e25-174">-Usuário</span><span class="sxs-lookup"><span data-stu-id="24e25-174">-User</span></span>
<span data-ttu-id="24e25-175">O nome de usuário usado para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="24e25-175">The username used to perform the operation.</span></span>

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

### <span data-ttu-id="24e25-176">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24e25-176">-Confirm</span></span>
<span data-ttu-id="24e25-177">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e25-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e25-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e25-178">-WhatIf</span></span>
<span data-ttu-id="24e25-179">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24e25-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e25-180">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24e25-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e25-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e25-181">CommonParameters</span></span>
<span data-ttu-id="24e25-182">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e25-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e25-183">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24e25-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e25-184">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24e25-184">INPUTS</span></span>

### <span data-ttu-id="24e25-185">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="24e25-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="24e25-186">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="24e25-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="24e25-187">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24e25-187">OUTPUTS</span></span>

### <span data-ttu-id="24e25-188">Microsoft. Azure. PowerShell. cmdlets. InfrastructureInsightsAdmin. Models. Api20160501. IAlert</span><span class="sxs-lookup"><span data-stu-id="24e25-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="24e25-189">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24e25-189">NOTES</span></span>

<span data-ttu-id="24e25-190">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="24e25-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24e25-191">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="24e25-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="24e25-192">ALERTA <IAlert> : esse objeto representa um recurso de alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="24e25-193">`[Location <String>]`: A região do Azure na qual o recurso reside</span><span class="sxs-lookup"><span data-stu-id="24e25-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="24e25-194">`[Tag <ITrackedResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="24e25-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="24e25-195">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="24e25-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="24e25-196">`[AlertId <String>]`: Obtém ou define a ID do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="24e25-197">`[AlertProperty <IAlertModelAlertProperties>]`: Propriedades do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="24e25-198">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="24e25-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="24e25-199">`[ClosedByUserAlias <String>]`: Alias do usuário que fechou o alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="24e25-200">`[ClosedTimestamp <String>]`: Carimbo de data/hora quando o alerta foi fechado.</span><span class="sxs-lookup"><span data-stu-id="24e25-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="24e25-201">`[CreatedTimestamp <String>]`: Carimbo de data/hora quando o alerta foi criado.</span><span class="sxs-lookup"><span data-stu-id="24e25-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="24e25-202">`[Description <IDictionary[]>]`: Descrição do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="24e25-203">`[FaultId <String>]`: Obtém ou define a identificação da falha do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="24e25-204">`[FaultTypeId <String>]`: Obtém ou define a ID do tipo de falha do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="24e25-205">`[HasValidRemediationAction <Boolean?>]`: Indica se o alerta pode ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="24e25-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="24e25-206">`[ImpactedResourceDisplayName <String>]`: Exibir o nome do item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="24e25-207">`[ImpactedResourceId <String>]`: Obtém ou define a ID do recurso para o item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="24e25-208">`[LastUpdatedTimestamp <String>]`: Carimbo de data/hora em que o alerta foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="24e25-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="24e25-209">`[Remediation <IDictionary[]>]`: Obtém ou define as instruções de correção amigável do administrador para o alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="24e25-210">`[ResourceProviderRegistrationId <String>]`: Obtém ou define a ID de registro do serviço ao qual o alerta pertence.</span><span class="sxs-lookup"><span data-stu-id="24e25-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="24e25-211">`[ResourceRegistrationId <String>]`: Obtém ou define a identificação de registro do recurso associado ao alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="24e25-212">Se o alerta não estiver associado a um recurso, a identificação de registro do recurso será nula.</span><span class="sxs-lookup"><span data-stu-id="24e25-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="24e25-213">`[Severity <String>]`: Severidade do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="24e25-214">`[State <String>]`: Estado do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="24e25-215">`[Title <String>]`: Obtém ou define a ID do recurso para o item afetado.</span><span class="sxs-lookup"><span data-stu-id="24e25-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="24e25-216">INPUTobject <IInfrastructureInsightsAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="24e25-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24e25-217">`[AlertName <String>]`: Nome do alerta.</span><span class="sxs-lookup"><span data-stu-id="24e25-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="24e25-218">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="24e25-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24e25-219">`[Location <String>]`: Nome da região</span><span class="sxs-lookup"><span data-stu-id="24e25-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="24e25-220">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e25-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="24e25-221">`[ResourceRegistrationId <String>]`: ID de registro do recurso.</span><span class="sxs-lookup"><span data-stu-id="24e25-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="24e25-222">`[ServiceHealth <String>]`: Nome da integridade do serviço.</span><span class="sxs-lookup"><span data-stu-id="24e25-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="24e25-223">`[ServiceRegistrationId <String>]`: ID de registro de serviço.</span><span class="sxs-lookup"><span data-stu-id="24e25-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="24e25-224">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="24e25-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="24e25-225">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="24e25-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="24e25-226">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24e25-226">RELATED LINKS</span></span>

