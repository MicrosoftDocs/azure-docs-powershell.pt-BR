---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116188"
---
# <span data-ttu-id="f098c-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f098c-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="f098c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f098c-102">SYNOPSIS</span></span>
<span data-ttu-id="f098c-103">Excluir um Incidente.</span><span class="sxs-lookup"><span data-stu-id="f098c-103">Delete an Incident.</span></span>

## <span data-ttu-id="f098c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f098c-104">SYNTAX</span></span>

### <span data-ttu-id="f098c-105">IncidentId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f098c-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f098c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f098c-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f098c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f098c-107">DESCRIPTION</span></span>
<span data-ttu-id="f098c-108">O cmdlet **Remove-AzSentinelIncident** exclui permanentemente um Incidente de um espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="f098c-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="f098c-109">Você pode passar um **objeto Incident** usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros necessários.</span><span class="sxs-lookup"><span data-stu-id="f098c-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="f098c-110">Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f098c-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f098c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f098c-111">EXAMPLES</span></span>

### <span data-ttu-id="f098c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f098c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="f098c-113">Esse comando remove o Incidente do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f098c-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="f098c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f098c-114">PARAMETERS</span></span>

### <span data-ttu-id="f098c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f098c-115">-DefaultProfile</span></span>
<span data-ttu-id="f098c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f098c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f098c-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="f098c-117">-IncidentId</span></span>
<span data-ttu-id="f098c-118">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="f098c-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f098c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f098c-119">-InputObject</span></span>
<span data-ttu-id="f098c-120">Inputobject.</span><span class="sxs-lookup"><span data-stu-id="f098c-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f098c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f098c-121">-PassThru</span></span>
<span data-ttu-id="f098c-122">Passthru</span><span class="sxs-lookup"><span data-stu-id="f098c-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f098c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f098c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f098c-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f098c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f098c-125">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="f098c-125">-WorkspaceName</span></span>
<span data-ttu-id="f098c-126">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f098c-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f098c-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f098c-127">-Confirm</span></span>
<span data-ttu-id="f098c-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f098c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f098c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f098c-129">-WhatIf</span></span>
<span data-ttu-id="f098c-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f098c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f098c-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f098c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f098c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f098c-132">CommonParameters</span></span>
<span data-ttu-id="f098c-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f098c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f098c-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f098c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f098c-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="f098c-135">INPUTS</span></span>

### <span data-ttu-id="f098c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f098c-136">System.String</span></span>
### <span data-ttu-id="f098c-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f098c-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="f098c-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="f098c-138">OUTPUTS</span></span>

### <span data-ttu-id="f098c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f098c-139">System.Boolean</span></span>
## <span data-ttu-id="f098c-140">Notas</span><span class="sxs-lookup"><span data-stu-id="f098c-140">NOTES</span></span>

## <span data-ttu-id="f098c-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f098c-141">RELATED LINKS</span></span>
