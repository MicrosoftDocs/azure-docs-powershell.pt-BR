---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113998"
---
# <span data-ttu-id="d494e-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d494e-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="d494e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d494e-102">SYNOPSIS</span></span>
<span data-ttu-id="d494e-103">Atualizar um Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-103">Update an Incident.</span></span>

## <span data-ttu-id="d494e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d494e-104">SYNTAX</span></span>

### <span data-ttu-id="d494e-105">IncidentId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d494e-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d494e-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d494e-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d494e-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="d494e-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d494e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d494e-108">DESCRIPTION</span></span>
<span data-ttu-id="d494e-109">O cmdlet **Update-AzSentinelIncident** atualiza o Incidente no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="d494e-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="d494e-110">Você pode passar um **objeto Incident** como um parâmetro ou usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="d494e-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d494e-111">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="d494e-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d494e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d494e-112">EXAMPLES</span></span>

### <span data-ttu-id="d494e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d494e-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="d494e-114">O comando obtém o Incidente por *IncidentId* e define a propriedade *Gravidade* como *Alta.*</span><span class="sxs-lookup"><span data-stu-id="d494e-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="d494e-115">Todas as outras propriedades permanecem as mesmas.</span><span class="sxs-lookup"><span data-stu-id="d494e-115">All other properties remain the same.</span></span>

## <span data-ttu-id="d494e-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d494e-116">PARAMETERS</span></span>

### <span data-ttu-id="d494e-117">-Classificação</span><span class="sxs-lookup"><span data-stu-id="d494e-117">-Classification</span></span>
<span data-ttu-id="d494e-118">Classificaiton de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="d494e-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="d494e-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="d494e-119">-ClassificationComment</span></span>
<span data-ttu-id="d494e-120">Comentário classificaiton de incidentes.</span><span class="sxs-lookup"><span data-stu-id="d494e-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="d494e-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="d494e-121">-ClassificationReason</span></span>
<span data-ttu-id="d494e-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="d494e-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="d494e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d494e-123">-DefaultProfile</span></span>
<span data-ttu-id="d494e-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d494e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d494e-125">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d494e-125">-Description</span></span>
<span data-ttu-id="d494e-126">Descrição.</span><span class="sxs-lookup"><span data-stu-id="d494e-126">Description.</span></span>

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

### <span data-ttu-id="d494e-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="d494e-127">-IncidentID</span></span>
<span data-ttu-id="d494e-128">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-128">Incident Id.</span></span>

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

### <span data-ttu-id="d494e-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d494e-129">-InputObject</span></span>
<span data-ttu-id="d494e-130">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="d494e-130">InputObject.</span></span>

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

### <span data-ttu-id="d494e-131">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="d494e-131">-Label</span></span>
<span data-ttu-id="d494e-132">Rótulos de Incidentes.</span><span class="sxs-lookup"><span data-stu-id="d494e-132">Incident Labels.</span></span>

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

### <span data-ttu-id="d494e-133">-Proprietário</span><span class="sxs-lookup"><span data-stu-id="d494e-133">-Owner</span></span>
<span data-ttu-id="d494e-134">Proprietário do Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-134">Incident Owner.</span></span>

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

### <span data-ttu-id="d494e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d494e-135">-ResourceGroupName</span></span>
<span data-ttu-id="d494e-136">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d494e-136">Resource group name.</span></span>

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

### <span data-ttu-id="d494e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d494e-137">-ResourceId</span></span>
<span data-ttu-id="d494e-138">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="d494e-138">Resource Id.</span></span>

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

### <span data-ttu-id="d494e-139">-Gravidade</span><span class="sxs-lookup"><span data-stu-id="d494e-139">-Severity</span></span>
<span data-ttu-id="d494e-140">Gravidade do Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-140">Incident Severity.</span></span>

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

### <span data-ttu-id="d494e-141">-Status</span><span class="sxs-lookup"><span data-stu-id="d494e-141">-Status</span></span>
<span data-ttu-id="d494e-142">Status do Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-142">Incident Status.</span></span>

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

### <span data-ttu-id="d494e-143">-Título</span><span class="sxs-lookup"><span data-stu-id="d494e-143">-Title</span></span>
<span data-ttu-id="d494e-144">Título do Incidente.</span><span class="sxs-lookup"><span data-stu-id="d494e-144">Incident Title.</span></span>

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

### <span data-ttu-id="d494e-145">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="d494e-145">-WorkspaceName</span></span>
<span data-ttu-id="d494e-146">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d494e-146">Workspace Name.</span></span>

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

### <span data-ttu-id="d494e-147">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d494e-147">-Confirm</span></span>
<span data-ttu-id="d494e-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d494e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d494e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d494e-149">-WhatIf</span></span>
<span data-ttu-id="d494e-150">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d494e-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d494e-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d494e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d494e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d494e-152">CommonParameters</span></span>
<span data-ttu-id="d494e-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d494e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d494e-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d494e-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d494e-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="d494e-155">INPUTS</span></span>

### <span data-ttu-id="d494e-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d494e-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="d494e-157">System.String</span><span class="sxs-lookup"><span data-stu-id="d494e-157">System.String</span></span>

### <span data-ttu-id="d494e-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0,0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d494e-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d494e-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="d494e-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="d494e-160">Saídas</span><span class="sxs-lookup"><span data-stu-id="d494e-160">OUTPUTS</span></span>

### <span data-ttu-id="d494e-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d494e-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="d494e-162">Notas</span><span class="sxs-lookup"><span data-stu-id="d494e-162">NOTES</span></span>

## <span data-ttu-id="d494e-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d494e-163">RELATED LINKS</span></span>
