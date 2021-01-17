---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433211"
---
# <span data-ttu-id="22272-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="22272-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="22272-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22272-102">SYNOPSIS</span></span>
<span data-ttu-id="22272-103">Obter um comentário sobre o incidente.</span><span class="sxs-lookup"><span data-stu-id="22272-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="22272-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22272-104">SYNTAX</span></span>

### <span data-ttu-id="22272-105">Incidentid (padrão)</span><span class="sxs-lookup"><span data-stu-id="22272-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22272-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="22272-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22272-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="22272-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22272-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22272-108">DESCRIPTION</span></span>
<span data-ttu-id="22272-109">O cmdlet **Get-AzSentinelIncidentComment** Obtém um comentário de incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="22272-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="22272-110">Se você especificar os parâmetros *IncidentCommentId* e *incidentid* , um único objeto **IncidentComment** será retornado.</span><span class="sxs-lookup"><span data-stu-id="22272-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="22272-111">Se você não especificar o parâmetro *IncidentCommentId* , uma matriz que contenha todos os comentários do incidente para o incidente especificado no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="22272-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="22272-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22272-112">EXAMPLES</span></span>

### <span data-ttu-id="22272-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22272-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="22272-114">Este exemplo obtém todos os **IncidentComments** do incidente especificado no espaço de trabalho especificado e, em seguida, armazena-os na variável $IncidentComments.</span><span class="sxs-lookup"><span data-stu-id="22272-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="22272-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22272-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="22272-116">Este exemplo obtém um **IncidentComment** para o incidente especificado no espaço de trabalho especificado e, em seguida, armazena-o na variável $IncidentComment.</span><span class="sxs-lookup"><span data-stu-id="22272-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="22272-117">OS</span><span class="sxs-lookup"><span data-stu-id="22272-117">PARAMETERS</span></span>

### <span data-ttu-id="22272-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22272-118">-DefaultProfile</span></span>
<span data-ttu-id="22272-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22272-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22272-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="22272-120">-IncidentCommentId</span></span>
<span data-ttu-id="22272-121">ID do comentário do incidente.</span><span class="sxs-lookup"><span data-stu-id="22272-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="22272-122">-Incidentid</span><span class="sxs-lookup"><span data-stu-id="22272-122">-IncidentId</span></span>
<span data-ttu-id="22272-123">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="22272-123">Incident Id.</span></span>

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

### <span data-ttu-id="22272-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22272-124">-ResourceGroupName</span></span>
<span data-ttu-id="22272-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="22272-125">Resource group name.</span></span>

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

### <span data-ttu-id="22272-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22272-126">-ResourceId</span></span>
<span data-ttu-id="22272-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="22272-127">Resource Id.</span></span>

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

### <span data-ttu-id="22272-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="22272-128">-WorkspaceName</span></span>
<span data-ttu-id="22272-129">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="22272-129">Workspace Name.</span></span>

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

### <span data-ttu-id="22272-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22272-130">CommonParameters</span></span>
<span data-ttu-id="22272-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22272-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22272-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22272-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22272-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22272-133">INPUTS</span></span>

### <span data-ttu-id="22272-134">System. String</span><span class="sxs-lookup"><span data-stu-id="22272-134">System.String</span></span>
## <span data-ttu-id="22272-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22272-135">OUTPUTS</span></span>

### <span data-ttu-id="22272-136">Microsoft. Azure. Commands. SecurityInsights. Models. IncidentComments. PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="22272-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="22272-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22272-137">NOTES</span></span>

## <span data-ttu-id="22272-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22272-138">RELATED LINKS</span></span>
