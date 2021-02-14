---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117148"
---
# <span data-ttu-id="55cf3-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="55cf3-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="55cf3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55cf3-102">SYNOPSIS</span></span>
<span data-ttu-id="55cf3-103">Criar um Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-103">Create an Incident.</span></span>

## <span data-ttu-id="55cf3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55cf3-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55cf3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="55cf3-105">DESCRIPTION</span></span>
<span data-ttu-id="55cf3-106">O cmdlet **New-AzSentinelIncident** cria um Incidente a partir do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="55cf3-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="55cf3-107">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="55cf3-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="55cf3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55cf3-108">EXAMPLES</span></span>

### <span data-ttu-id="55cf3-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="55cf3-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="55cf3-110">Este exemplo cria **um Incidente** no espaço de trabalho especificado e o armazena na variável $Incident dados.</span><span class="sxs-lookup"><span data-stu-id="55cf3-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="55cf3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55cf3-111">PARAMETERS</span></span>

### <span data-ttu-id="55cf3-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="55cf3-112">-ClassificationComment</span></span>
<span data-ttu-id="55cf3-113">Comentário classificaiton de incidentes.</span><span class="sxs-lookup"><span data-stu-id="55cf3-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="55cf3-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="55cf3-114">-ClassificationReason</span></span>
<span data-ttu-id="55cf3-115">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="55cf3-115">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="55cf3-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="55cf3-116">-Classificaton</span></span>
<span data-ttu-id="55cf3-117">Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="55cf3-117">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="55cf3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cf3-118">-DefaultProfile</span></span>
<span data-ttu-id="55cf3-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55cf3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55cf3-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="55cf3-120">-Description</span></span>
<span data-ttu-id="55cf3-121">Descrição.</span><span class="sxs-lookup"><span data-stu-id="55cf3-121">Description.</span></span>

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

### <span data-ttu-id="55cf3-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="55cf3-122">-IncidentId</span></span>
<span data-ttu-id="55cf3-123">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-123">Incident Id.</span></span>

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

### <span data-ttu-id="55cf3-124">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="55cf3-124">-Label</span></span>
<span data-ttu-id="55cf3-125">Rótulos de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="55cf3-125">Incident Labels.</span></span>

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

### <span data-ttu-id="55cf3-126">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="55cf3-126">-Owner</span></span>
<span data-ttu-id="55cf3-127">Proprietário do Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-127">Incident Owner.</span></span>

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

### <span data-ttu-id="55cf3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55cf3-128">-ResourceGroupName</span></span>
<span data-ttu-id="55cf3-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="55cf3-129">Resource group name.</span></span>

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

### <span data-ttu-id="55cf3-130">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="55cf3-130">-Severity</span></span>
<span data-ttu-id="55cf3-131">Gravidade do Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-131">Incident Severity.</span></span>

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

### <span data-ttu-id="55cf3-132">-Status</span><span class="sxs-lookup"><span data-stu-id="55cf3-132">-Status</span></span>
<span data-ttu-id="55cf3-133">Status do Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-133">Incident Status.</span></span>

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

### <span data-ttu-id="55cf3-134">-Título</span><span class="sxs-lookup"><span data-stu-id="55cf3-134">-Title</span></span>
<span data-ttu-id="55cf3-135">Título do Incidente.</span><span class="sxs-lookup"><span data-stu-id="55cf3-135">Incident Title.</span></span>

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

### <span data-ttu-id="55cf3-136">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="55cf3-136">-WorkspaceName</span></span>
<span data-ttu-id="55cf3-137">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="55cf3-137">Workspace Name.</span></span>

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

### <span data-ttu-id="55cf3-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55cf3-138">-Confirm</span></span>
<span data-ttu-id="55cf3-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55cf3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55cf3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55cf3-140">-WhatIf</span></span>
<span data-ttu-id="55cf3-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55cf3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55cf3-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55cf3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55cf3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cf3-143">CommonParameters</span></span>
<span data-ttu-id="55cf3-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cf3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cf3-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55cf3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cf3-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="55cf3-146">INPUTS</span></span>

### <span data-ttu-id="55cf3-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="55cf3-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="55cf3-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="55cf3-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="55cf3-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="55cf3-149">OUTPUTS</span></span>

### <span data-ttu-id="55cf3-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="55cf3-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="55cf3-151">Notas</span><span class="sxs-lookup"><span data-stu-id="55cf3-151">NOTES</span></span>

## <span data-ttu-id="55cf3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55cf3-152">RELATED LINKS</span></span>
