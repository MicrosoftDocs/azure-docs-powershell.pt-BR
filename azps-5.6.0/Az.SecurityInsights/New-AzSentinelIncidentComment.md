---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 0fe04e773e02a8b6b61f9c57d8316ac8936f05aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886845"
---
# <span data-ttu-id="551ea-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="551ea-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="551ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="551ea-102">SYNOPSIS</span></span>
<span data-ttu-id="551ea-103">Adicione um Comentário de Incidente a um Incidente.</span><span class="sxs-lookup"><span data-stu-id="551ea-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="551ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="551ea-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="551ea-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="551ea-105">DESCRIPTION</span></span>
<span data-ttu-id="551ea-106">O cmdlet **New-AzSentinelIncidentComment** cria um Comentário de Incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="551ea-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="551ea-107">Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.</span><span class="sxs-lookup"><span data-stu-id="551ea-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="551ea-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="551ea-108">EXAMPLES</span></span>

### <span data-ttu-id="551ea-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="551ea-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="551ea-110">Este exemplo cria **um IncidentComment** no espaço de trabalho especificado e o armazena na variável $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="551ea-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="551ea-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="551ea-111">PARAMETERS</span></span>

### <span data-ttu-id="551ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ea-112">-DefaultProfile</span></span>
<span data-ttu-id="551ea-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="551ea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551ea-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="551ea-114">-IncidentCommentId</span></span>
<span data-ttu-id="551ea-115">ID do Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="551ea-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="551ea-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="551ea-116">-IncidentId</span></span>
<span data-ttu-id="551ea-117">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="551ea-117">Incident Id.</span></span>

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

### <span data-ttu-id="551ea-118">-Message</span><span class="sxs-lookup"><span data-stu-id="551ea-118">-Message</span></span>
<span data-ttu-id="551ea-119">Mensagem de Incidente.</span><span class="sxs-lookup"><span data-stu-id="551ea-119">Incident Message.</span></span>

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

### <span data-ttu-id="551ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="551ea-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="551ea-121">Resource group name.</span></span>

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

### <span data-ttu-id="551ea-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="551ea-122">-WorkspaceName</span></span>
<span data-ttu-id="551ea-123">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="551ea-123">Workspace Name.</span></span>

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

### <span data-ttu-id="551ea-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="551ea-124">-Confirm</span></span>
<span data-ttu-id="551ea-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="551ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="551ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="551ea-126">-WhatIf</span></span>
<span data-ttu-id="551ea-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="551ea-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="551ea-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="551ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="551ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ea-129">CommonParameters</span></span>
<span data-ttu-id="551ea-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="551ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ea-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="551ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ea-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="551ea-132">INPUTS</span></span>

### <span data-ttu-id="551ea-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="551ea-133">None</span></span>
## <span data-ttu-id="551ea-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="551ea-134">OUTPUTS</span></span>

### <span data-ttu-id="551ea-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="551ea-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="551ea-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="551ea-136">NOTES</span></span>

## <span data-ttu-id="551ea-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="551ea-137">RELATED LINKS</span></span>
