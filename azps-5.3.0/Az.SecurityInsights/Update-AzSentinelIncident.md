---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433177"
---
# <span data-ttu-id="70031-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="70031-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="70031-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70031-102">SYNOPSIS</span></span>
<span data-ttu-id="70031-103">Atualizar um incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-103">Update an Incident.</span></span>

## <span data-ttu-id="70031-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70031-104">SYNTAX</span></span>

### <span data-ttu-id="70031-105">Incidentid (padrão)</span><span class="sxs-lookup"><span data-stu-id="70031-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70031-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="70031-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70031-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="70031-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70031-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70031-108">DESCRIPTION</span></span>
<span data-ttu-id="70031-109">O cmdlet **Update-AzSentinelIncident** atualiza o incidente no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="70031-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="70031-110">Você pode passar um objeto de **incidente** como um parâmetro ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="70031-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="70031-111">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="70031-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="70031-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70031-112">EXAMPLES</span></span>

### <span data-ttu-id="70031-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="70031-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="70031-114">O comando obtém o incidente por *incidenteid* e define a propriedade *Severity* como *High*.</span><span class="sxs-lookup"><span data-stu-id="70031-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="70031-115">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="70031-115">All other properties remain the same.</span></span>

## <span data-ttu-id="70031-116">OS</span><span class="sxs-lookup"><span data-stu-id="70031-116">PARAMETERS</span></span>

### <span data-ttu-id="70031-117">-Classificação</span><span class="sxs-lookup"><span data-stu-id="70031-117">-Classification</span></span>
<span data-ttu-id="70031-118">Incidente Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="70031-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="70031-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="70031-119">-ClassificationComment</span></span>
<span data-ttu-id="70031-120">Comentário Classificaiton do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="70031-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="70031-121">-ClassificationReason</span></span>
<span data-ttu-id="70031-122">Motivo Classificaiton do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="70031-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70031-123">-DefaultProfile</span></span>
<span data-ttu-id="70031-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70031-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70031-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="70031-125">-Description</span></span>
<span data-ttu-id="70031-126">Descritivo.</span><span class="sxs-lookup"><span data-stu-id="70031-126">Description.</span></span>

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

### <span data-ttu-id="70031-127">-Incidentid</span><span class="sxs-lookup"><span data-stu-id="70031-127">-IncidentID</span></span>
<span data-ttu-id="70031-128">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-128">Incident Id.</span></span>

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

### <span data-ttu-id="70031-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70031-129">-InputObject</span></span>
<span data-ttu-id="70031-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="70031-130">InputObject.</span></span>

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

### <span data-ttu-id="70031-131">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="70031-131">-Label</span></span>
<span data-ttu-id="70031-132">Rótulos de incidentes.</span><span class="sxs-lookup"><span data-stu-id="70031-132">Incident Labels.</span></span>

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

### <span data-ttu-id="70031-133">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="70031-133">-Owner</span></span>
<span data-ttu-id="70031-134">Proprietário do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-134">Incident Owner.</span></span>

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

### <span data-ttu-id="70031-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70031-135">-ResourceGroupName</span></span>
<span data-ttu-id="70031-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70031-136">Resource group name.</span></span>

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

### <span data-ttu-id="70031-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70031-137">-ResourceId</span></span>
<span data-ttu-id="70031-138">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="70031-138">Resource Id.</span></span>

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

### <span data-ttu-id="70031-139">-Severidade</span><span class="sxs-lookup"><span data-stu-id="70031-139">-Severity</span></span>
<span data-ttu-id="70031-140">Severidade do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-140">Incident Severity.</span></span>

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

### <span data-ttu-id="70031-141">-Status</span><span class="sxs-lookup"><span data-stu-id="70031-141">-Status</span></span>
<span data-ttu-id="70031-142">Status do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-142">Incident Status.</span></span>

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

### <span data-ttu-id="70031-143">-Título</span><span class="sxs-lookup"><span data-stu-id="70031-143">-Title</span></span>
<span data-ttu-id="70031-144">Título do incidente.</span><span class="sxs-lookup"><span data-stu-id="70031-144">Incident Title.</span></span>

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

### <span data-ttu-id="70031-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="70031-145">-WorkspaceName</span></span>
<span data-ttu-id="70031-146">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="70031-146">Workspace Name.</span></span>

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

### <span data-ttu-id="70031-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70031-147">-Confirm</span></span>
<span data-ttu-id="70031-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70031-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70031-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70031-149">-WhatIf</span></span>
<span data-ttu-id="70031-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70031-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70031-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70031-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70031-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70031-152">CommonParameters</span></span>
<span data-ttu-id="70031-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70031-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70031-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70031-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70031-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70031-155">INPUTS</span></span>

### <span data-ttu-id="70031-156">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="70031-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="70031-157">System. String</span><span class="sxs-lookup"><span data-stu-id="70031-157">System.String</span></span>

### <span data-ttu-id="70031-158">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncidentLabel, Microsoft. Azure. PowerShell. cmdlets. SecurityInsights, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="70031-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="70031-159">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="70031-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="70031-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70031-160">OUTPUTS</span></span>

### <span data-ttu-id="70031-161">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="70031-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="70031-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70031-162">NOTES</span></span>

## <span data-ttu-id="70031-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70031-163">RELATED LINKS</span></span>
