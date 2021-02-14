---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117147"
---
# <span data-ttu-id="c8c8a-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c8c8a-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="c8c8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8c8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c8a-103">Adicionar um Comentário de Incidente a um Incidente.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="c8c8a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8c8a-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c8a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8c8a-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c8a-106">O cmdlet **New-AzSentinelIncidentComment cria** um Comentário de Incidente a partir do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="c8c8a-107">Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c8c8a-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8c8a-108">EXAMPLES</span></span>

### <span data-ttu-id="c8c8a-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8c8a-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="c8c8a-110">Este exemplo cria **um IncidentComment** no espaço de trabalho especificado e o armazena na variável $IncidentComment dados.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="c8c8a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8c8a-111">PARAMETERS</span></span>

### <span data-ttu-id="c8c8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c8a-112">-DefaultProfile</span></span>
<span data-ttu-id="c8c8a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c8a-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="c8c8a-114">-IncidentCommentId</span></span>
<span data-ttu-id="c8c8a-115">ID do Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="c8c8a-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c8c8a-116">-IncidentId</span></span>
<span data-ttu-id="c8c8a-117">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-117">Incident Id.</span></span>

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

### <span data-ttu-id="c8c8a-118">-Mensagem</span><span class="sxs-lookup"><span data-stu-id="c8c8a-118">-Message</span></span>
<span data-ttu-id="c8c8a-119">Mensagem de Incidente.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-119">Incident Message.</span></span>

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

### <span data-ttu-id="c8c8a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c8a-120">-ResourceGroupName</span></span>
<span data-ttu-id="c8c8a-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-121">Resource group name.</span></span>

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

### <span data-ttu-id="c8c8a-122">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="c8c8a-122">-WorkspaceName</span></span>
<span data-ttu-id="c8c8a-123">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-123">Workspace Name.</span></span>

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

### <span data-ttu-id="c8c8a-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8c8a-124">-Confirm</span></span>
<span data-ttu-id="c8c8a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c8a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c8a-126">-WhatIf</span></span>
<span data-ttu-id="c8c8a-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8c8a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c8a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c8a-129">CommonParameters</span></span>
<span data-ttu-id="c8c8a-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c8a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c8a-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8c8a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c8a-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8c8a-132">INPUTS</span></span>

### <span data-ttu-id="c8c8a-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c8c8a-133">None</span></span>
## <span data-ttu-id="c8c8a-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8c8a-134">OUTPUTS</span></span>

### <span data-ttu-id="c8c8a-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="c8c8a-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="c8c8a-136">Notas</span><span class="sxs-lookup"><span data-stu-id="c8c8a-136">NOTES</span></span>

## <span data-ttu-id="c8c8a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8c8a-137">RELATED LINKS</span></span>
