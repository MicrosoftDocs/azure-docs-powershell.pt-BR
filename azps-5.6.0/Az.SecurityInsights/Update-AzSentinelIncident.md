---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: 03062015b1f9d14688488887ed226f1b697589ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901575"
---
# <span data-ttu-id="05e8f-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="05e8f-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="05e8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="05e8f-103">Atualizar um Incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-103">Update an Incident.</span></span>

## <span data-ttu-id="05e8f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="05e8f-104">SYNTAX</span></span>

### <span data-ttu-id="05e8f-105">IncidentId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05e8f-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e8f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="05e8f-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05e8f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="05e8f-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05e8f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="05e8f-108">DESCRIPTION</span></span>
<span data-ttu-id="05e8f-109">O cmdlet **Update-AzSentinelIncident** atualiza o Incidente no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="05e8f-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="05e8f-110">Você pode passar um **objeto Incident** como um parâmetro ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="05e8f-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="05e8f-111">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="05e8f-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="05e8f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05e8f-112">EXAMPLES</span></span>

### <span data-ttu-id="05e8f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="05e8f-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="05e8f-114">O comando obtém o Incidente por *IncidentId* e define a propriedade *Severity* como *High*.</span><span class="sxs-lookup"><span data-stu-id="05e8f-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="05e8f-115">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="05e8f-115">All other properties remain the same.</span></span>

## <span data-ttu-id="05e8f-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="05e8f-116">PARAMETERS</span></span>

### <span data-ttu-id="05e8f-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="05e8f-117">-Classification</span></span>
<span data-ttu-id="05e8f-118">Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="05e8f-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="05e8f-119">-ClassificationComment</span></span>
<span data-ttu-id="05e8f-120">Comentário classificaiton de incidentes.</span><span class="sxs-lookup"><span data-stu-id="05e8f-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="05e8f-121">-ClassificationReason</span></span>
<span data-ttu-id="05e8f-122">Motivo de Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="05e8f-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e8f-123">-DefaultProfile</span></span>
<span data-ttu-id="05e8f-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05e8f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-125">-Description</span><span class="sxs-lookup"><span data-stu-id="05e8f-125">-Description</span></span>
<span data-ttu-id="05e8f-126">Descrição.</span><span class="sxs-lookup"><span data-stu-id="05e8f-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="05e8f-127">-IncidentID</span></span>
<span data-ttu-id="05e8f-128">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05e8f-129">-InputObject</span></span>
<span data-ttu-id="05e8f-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="05e8f-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-131">-Label</span><span class="sxs-lookup"><span data-stu-id="05e8f-131">-Label</span></span>
<span data-ttu-id="05e8f-132">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="05e8f-132">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-133">-Owner</span><span class="sxs-lookup"><span data-stu-id="05e8f-133">-Owner</span></span>
<span data-ttu-id="05e8f-134">Proprietário do Incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e8f-135">-ResourceGroupName</span></span>
<span data-ttu-id="05e8f-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05e8f-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05e8f-137">-ResourceId</span></span>
<span data-ttu-id="05e8f-138">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="05e8f-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-139">-Severity</span><span class="sxs-lookup"><span data-stu-id="05e8f-139">-Severity</span></span>
<span data-ttu-id="05e8f-140">Gravidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-141">-Status</span><span class="sxs-lookup"><span data-stu-id="05e8f-141">-Status</span></span>
<span data-ttu-id="05e8f-142">Status do Incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-143">-Title</span><span class="sxs-lookup"><span data-stu-id="05e8f-143">-Title</span></span>
<span data-ttu-id="05e8f-144">Título do Incidente.</span><span class="sxs-lookup"><span data-stu-id="05e8f-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="05e8f-145">-WorkspaceName</span></span>
<span data-ttu-id="05e8f-146">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="05e8f-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05e8f-147">-Confirm</span></span>
<span data-ttu-id="05e8f-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e8f-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e8f-149">-WhatIf</span></span>
<span data-ttu-id="05e8f-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05e8f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05e8f-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05e8f-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e8f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e8f-152">CommonParameters</span></span>
<span data-ttu-id="05e8f-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e8f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e8f-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05e8f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e8f-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05e8f-155">INPUTS</span></span>

### <span data-ttu-id="05e8f-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="05e8f-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="05e8f-157">System.String</span><span class="sxs-lookup"><span data-stu-id="05e8f-157">System.String</span></span>

### <span data-ttu-id="05e8f-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="05e8f-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="05e8f-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="05e8f-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="05e8f-160">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="05e8f-160">OUTPUTS</span></span>

### <span data-ttu-id="05e8f-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="05e8f-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="05e8f-162">NOTES</span><span class="sxs-lookup"><span data-stu-id="05e8f-162">NOTES</span></span>

## <span data-ttu-id="05e8f-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05e8f-163">RELATED LINKS</span></span>
