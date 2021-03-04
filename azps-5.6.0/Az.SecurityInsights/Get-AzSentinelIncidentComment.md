---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: b25e99766c4dc0433b14810352968300fd5bd129
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889723"
---
# <span data-ttu-id="95133-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="95133-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="95133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95133-102">SYNOPSIS</span></span>
<span data-ttu-id="95133-103">Obter um Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="95133-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="95133-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="95133-104">SYNTAX</span></span>

### <span data-ttu-id="95133-105">IncidentId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="95133-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95133-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="95133-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95133-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="95133-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95133-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="95133-108">DESCRIPTION</span></span>
<span data-ttu-id="95133-109">O cmdlet **Get-AzSentinelIncidentComment** obtém um Comentário de Incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="95133-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="95133-110">Se você especificar os *parâmetros IncidentCommentId* e *IncidentId,* um único **objeto IncidentComment** será retornado.</span><span class="sxs-lookup"><span data-stu-id="95133-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="95133-111">Se você não especificar o parâmetro *IncidentCommentId,* será retornada uma matriz contendo todos os Comentários de Incidente para o Incidente especificado no espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="95133-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="95133-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95133-112">EXAMPLES</span></span>

### <span data-ttu-id="95133-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95133-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="95133-114">Este exemplo obtém todos os **IncidentComments** do Incidente especificado no espaço de trabalho especificado e o armazena na variável $IncidentComments.</span><span class="sxs-lookup"><span data-stu-id="95133-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="95133-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="95133-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="95133-116">Este exemplo obtém **um IncidentComment** para o Incidente especificado no espaço de trabalho especificado e o armazena na variável $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="95133-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="95133-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="95133-117">PARAMETERS</span></span>

### <span data-ttu-id="95133-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95133-118">-DefaultProfile</span></span>
<span data-ttu-id="95133-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95133-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95133-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="95133-120">-IncidentCommentId</span></span>
<span data-ttu-id="95133-121">ID do Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="95133-121">Incident Comment Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95133-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="95133-122">-IncidentId</span></span>
<span data-ttu-id="95133-123">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="95133-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95133-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95133-124">-ResourceGroupName</span></span>
<span data-ttu-id="95133-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95133-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95133-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95133-126">-ResourceId</span></span>
<span data-ttu-id="95133-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="95133-127">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95133-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="95133-128">-WorkspaceName</span></span>
<span data-ttu-id="95133-129">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="95133-129">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId, IncidentCommentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95133-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95133-130">CommonParameters</span></span>
<span data-ttu-id="95133-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95133-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95133-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95133-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95133-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95133-133">INPUTS</span></span>

### <span data-ttu-id="95133-134">System.String</span><span class="sxs-lookup"><span data-stu-id="95133-134">System.String</span></span>
## <span data-ttu-id="95133-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="95133-135">OUTPUTS</span></span>

### <span data-ttu-id="95133-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="95133-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="95133-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="95133-137">NOTES</span></span>

## <span data-ttu-id="95133-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95133-138">RELATED LINKS</span></span>
