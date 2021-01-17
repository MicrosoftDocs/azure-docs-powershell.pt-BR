---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433197"
---
# <span data-ttu-id="6e0ee-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="6e0ee-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="6e0ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e0ee-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0ee-103">Adicionar um comentário de incidente a um incidente.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="6e0ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e0ee-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e0ee-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e0ee-105">DESCRIPTION</span></span>
<span data-ttu-id="6e0ee-106">O cmdlet **New-AzSentinelIncidentComment** cria um comentário de incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="6e0ee-107">Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6e0ee-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e0ee-108">EXAMPLES</span></span>

### <span data-ttu-id="6e0ee-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6e0ee-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="6e0ee-110">Este exemplo cria um **IncidentComment** no espaço de trabalho especificado e, em seguida, armazena-o na variável $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="6e0ee-111">OS</span><span class="sxs-lookup"><span data-stu-id="6e0ee-111">PARAMETERS</span></span>

### <span data-ttu-id="6e0ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0ee-112">-DefaultProfile</span></span>
<span data-ttu-id="6e0ee-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0ee-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="6e0ee-114">-IncidentCommentId</span></span>
<span data-ttu-id="6e0ee-115">ID do comentário do incidente.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="6e0ee-116">-Incidentid</span><span class="sxs-lookup"><span data-stu-id="6e0ee-116">-IncidentId</span></span>
<span data-ttu-id="6e0ee-117">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-117">Incident Id.</span></span>

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

### <span data-ttu-id="6e0ee-118">-Mensagem</span><span class="sxs-lookup"><span data-stu-id="6e0ee-118">-Message</span></span>
<span data-ttu-id="6e0ee-119">Mensagem de incidente.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-119">Incident Message.</span></span>

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

### <span data-ttu-id="6e0ee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e0ee-120">-ResourceGroupName</span></span>
<span data-ttu-id="6e0ee-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-121">Resource group name.</span></span>

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

### <span data-ttu-id="6e0ee-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e0ee-122">-WorkspaceName</span></span>
<span data-ttu-id="6e0ee-123">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-123">Workspace Name.</span></span>

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

### <span data-ttu-id="6e0ee-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e0ee-124">-Confirm</span></span>
<span data-ttu-id="6e0ee-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e0ee-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e0ee-126">-WhatIf</span></span>
<span data-ttu-id="6e0ee-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e0ee-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e0ee-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0ee-129">CommonParameters</span></span>
<span data-ttu-id="6e0ee-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0ee-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0ee-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e0ee-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0ee-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e0ee-132">INPUTS</span></span>

### <span data-ttu-id="6e0ee-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6e0ee-133">None</span></span>
## <span data-ttu-id="6e0ee-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e0ee-134">OUTPUTS</span></span>

### <span data-ttu-id="6e0ee-135">Microsoft. Azure. Commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="6e0ee-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="6e0ee-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e0ee-136">NOTES</span></span>

## <span data-ttu-id="6e0ee-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e0ee-137">RELATED LINKS</span></span>
