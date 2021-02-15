---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncidentComment.md
ms.openlocfilehash: d33c126da2a77736871a9ec1f950382168f52bee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111366"
---
# <span data-ttu-id="36804-101">Get-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="36804-101">Get-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="36804-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36804-102">SYNOPSIS</span></span>
<span data-ttu-id="36804-103">Obter um Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="36804-103">Get an Incident Comment.</span></span>

## <span data-ttu-id="36804-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36804-104">SYNTAX</span></span>

### <span data-ttu-id="36804-105">IncidentId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36804-105">IncidentId (Default)</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36804-106">IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="36804-106">IncidentCommentId</span></span>
```
Get-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 -IncidentCommentId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36804-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="36804-107">ResourceId</span></span>
```
Get-AzSentinelIncidentComment -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36804-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="36804-108">DESCRIPTION</span></span>
<span data-ttu-id="36804-109">O cmdlet **Get-AzSentinelIncidentComment** obtém um Comentário de Incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="36804-109">The **Get-AzSentinelIncidentComment** cmdlet gets a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="36804-110">Se você especificar os parâmetros *IncidentCommentId* e *IncidentId,* um único objeto **IncidentComment** será retornado.</span><span class="sxs-lookup"><span data-stu-id="36804-110">If you specify the *IncidentCommentId* and *IncidentId* parameters, a single **IncidentComment** object is returned.</span></span>
<span data-ttu-id="36804-111">Se você não especificar o parâmetro *IncidentCommentId,* uma matriz contendo todos os Comentários de Incidente do Incidente especificado no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="36804-111">If you do not specify the *IncidentCommentId* parameter, an array containing all of the Incident Comments for the specified Incident in the specified workspace are returned.</span></span>

## <span data-ttu-id="36804-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36804-112">EXAMPLES</span></span>

### <span data-ttu-id="36804-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="36804-113">Example 1</span></span>
```powershell
PS C:\> $IncidentComments = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="36804-114">Este exemplo obtém todos os **IncidentComments** do Incidente especificado no espaço de trabalho especificado e o armazena na variável $IncidentComments dados.</span><span class="sxs-lookup"><span data-stu-id="36804-114">This example gets all of the **IncidentComments** for the specified Incident in the specified workspace, and then stores it in the $IncidentComments variable.</span></span>

### <span data-ttu-id="36804-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="36804-115">Example 2</span></span>
```powershell
PS C:\> $IncidentComment = Get-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -IncidentCommentId "MyIncidentCommentId"
```

<span data-ttu-id="36804-116">Este exemplo obtém um **IncidentComment** para o Incidente especificado no espaço de trabalho especificado e o armazena na variável $IncidentComment dados.</span><span class="sxs-lookup"><span data-stu-id="36804-116">This example gets an **IncidentComment** for the specified Incident in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="36804-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36804-117">PARAMETERS</span></span>

### <span data-ttu-id="36804-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36804-118">-DefaultProfile</span></span>
<span data-ttu-id="36804-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36804-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36804-120">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="36804-120">-IncidentCommentId</span></span>
<span data-ttu-id="36804-121">ID do Comentário de Incidente.</span><span class="sxs-lookup"><span data-stu-id="36804-121">Incident Comment Id.</span></span>

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

### <span data-ttu-id="36804-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="36804-122">-IncidentId</span></span>
<span data-ttu-id="36804-123">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="36804-123">Incident Id.</span></span>

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

### <span data-ttu-id="36804-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36804-124">-ResourceGroupName</span></span>
<span data-ttu-id="36804-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="36804-125">Resource group name.</span></span>

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

### <span data-ttu-id="36804-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36804-126">-ResourceId</span></span>
<span data-ttu-id="36804-127">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="36804-127">Resource Id.</span></span>

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

### <span data-ttu-id="36804-128">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="36804-128">-WorkspaceName</span></span>
<span data-ttu-id="36804-129">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="36804-129">Workspace Name.</span></span>

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

### <span data-ttu-id="36804-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36804-130">CommonParameters</span></span>
<span data-ttu-id="36804-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36804-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36804-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36804-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36804-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="36804-133">INPUTS</span></span>

### <span data-ttu-id="36804-134">System.String</span><span class="sxs-lookup"><span data-stu-id="36804-134">System.String</span></span>
## <span data-ttu-id="36804-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="36804-135">OUTPUTS</span></span>

### <span data-ttu-id="36804-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="36804-136">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="36804-137">Notas</span><span class="sxs-lookup"><span data-stu-id="36804-137">NOTES</span></span>

## <span data-ttu-id="36804-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36804-138">RELATED LINKS</span></span>
