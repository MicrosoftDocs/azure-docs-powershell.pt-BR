---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892358"
---
# <span data-ttu-id="46975-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="46975-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="46975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46975-102">SYNOPSIS</span></span>
<span data-ttu-id="46975-103">Criar um incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-103">Create an Incident.</span></span>

## <span data-ttu-id="46975-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="46975-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46975-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="46975-105">DESCRIPTION</span></span>
<span data-ttu-id="46975-106">O cmdlet **New-AzSentinelIncident** cria um Incidente a partir do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="46975-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="46975-107">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="46975-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="46975-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46975-108">EXAMPLES</span></span>

### <span data-ttu-id="46975-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="46975-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="46975-110">Este exemplo cria um **Incidente** no espaço de trabalho especificado e o armazena na variável $Incident.</span><span class="sxs-lookup"><span data-stu-id="46975-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="46975-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="46975-111">PARAMETERS</span></span>

### <span data-ttu-id="46975-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="46975-112">-ClassificationComment</span></span>
<span data-ttu-id="46975-113">Comentário classificaiton de incidentes.</span><span class="sxs-lookup"><span data-stu-id="46975-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="46975-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="46975-114">-ClassificationReason</span></span>
<span data-ttu-id="46975-115">Motivo de Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="46975-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46975-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="46975-116">-Classificaton</span></span>
<span data-ttu-id="46975-117">Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="46975-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46975-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46975-118">-DefaultProfile</span></span>
<span data-ttu-id="46975-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46975-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46975-120">-Description</span><span class="sxs-lookup"><span data-stu-id="46975-120">-Description</span></span>
<span data-ttu-id="46975-121">Descrição.</span><span class="sxs-lookup"><span data-stu-id="46975-121">Description.</span></span>

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

### <span data-ttu-id="46975-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="46975-122">-IncidentId</span></span>
<span data-ttu-id="46975-123">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-123">Incident Id.</span></span>

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

### <span data-ttu-id="46975-124">-Label</span><span class="sxs-lookup"><span data-stu-id="46975-124">-Label</span></span>
<span data-ttu-id="46975-125">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="46975-125">Incident Labels.</span></span>

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

### <span data-ttu-id="46975-126">-Owner</span><span class="sxs-lookup"><span data-stu-id="46975-126">-Owner</span></span>
<span data-ttu-id="46975-127">Proprietário do Incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46975-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46975-128">-ResourceGroupName</span></span>
<span data-ttu-id="46975-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="46975-129">Resource group name.</span></span>

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

### <span data-ttu-id="46975-130">-Severity</span><span class="sxs-lookup"><span data-stu-id="46975-130">-Severity</span></span>
<span data-ttu-id="46975-131">Gravidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46975-132">-Status</span><span class="sxs-lookup"><span data-stu-id="46975-132">-Status</span></span>
<span data-ttu-id="46975-133">Status do Incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46975-134">-Title</span><span class="sxs-lookup"><span data-stu-id="46975-134">-Title</span></span>
<span data-ttu-id="46975-135">Título do Incidente.</span><span class="sxs-lookup"><span data-stu-id="46975-135">Incident Title.</span></span>

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

### <span data-ttu-id="46975-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46975-136">-WorkspaceName</span></span>
<span data-ttu-id="46975-137">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="46975-137">Workspace Name.</span></span>

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

### <span data-ttu-id="46975-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46975-138">-Confirm</span></span>
<span data-ttu-id="46975-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46975-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46975-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46975-140">-WhatIf</span></span>
<span data-ttu-id="46975-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46975-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46975-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46975-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46975-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46975-143">CommonParameters</span></span>
<span data-ttu-id="46975-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46975-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46975-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46975-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46975-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46975-146">INPUTS</span></span>

### <span data-ttu-id="46975-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="46975-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="46975-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="46975-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="46975-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="46975-149">OUTPUTS</span></span>

### <span data-ttu-id="46975-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="46975-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="46975-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="46975-151">NOTES</span></span>

## <span data-ttu-id="46975-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46975-152">RELATED LINKS</span></span>
