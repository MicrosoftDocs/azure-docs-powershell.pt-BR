---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112601"
---
# <span data-ttu-id="396fc-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="396fc-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="396fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="396fc-102">SYNOPSIS</span></span>
<span data-ttu-id="396fc-103">Obter um Incidente.</span><span class="sxs-lookup"><span data-stu-id="396fc-103">Get an Incident.</span></span>

## <span data-ttu-id="396fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="396fc-104">SYNTAX</span></span>

### <span data-ttu-id="396fc-105">WorkspaceScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="396fc-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="396fc-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="396fc-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="396fc-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="396fc-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="396fc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="396fc-108">DESCRIPTION</span></span>
<span data-ttu-id="396fc-109">O cmdlet **Get-AzSentinelIncident** obtém um Incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="396fc-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="396fc-110">Se você especificar o parâmetro *IncidentId,* um único **objeto Incident** será retornado.</span><span class="sxs-lookup"><span data-stu-id="396fc-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="396fc-111">Se você não especificar o parâmetro *IncidentId,* uma matriz contendo todos os Incidentes no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="396fc-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="396fc-112">Você pode usar o **objeto Incidente** para atualizar o Incidente, por exemplo, você pode adicionar Anotações do **Incidente.**</span><span class="sxs-lookup"><span data-stu-id="396fc-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="396fc-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="396fc-113">EXAMPLES</span></span>

### <span data-ttu-id="396fc-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="396fc-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="396fc-115">Este exemplo obtém todos os **Incidentes** no espaço de trabalho especificado e, em seguida, o armazena na variável $Incidents dados.</span><span class="sxs-lookup"><span data-stu-id="396fc-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="396fc-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="396fc-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="396fc-117">Este exemplo obtém **um Incidente** no espaço de trabalho especificado e o armazena na variável $Incident dados.</span><span class="sxs-lookup"><span data-stu-id="396fc-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="396fc-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="396fc-118">PARAMETERS</span></span>

### <span data-ttu-id="396fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396fc-119">-DefaultProfile</span></span>
<span data-ttu-id="396fc-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="396fc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="396fc-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="396fc-121">-IncidentId</span></span>
<span data-ttu-id="396fc-122">ID do Incidente.</span><span class="sxs-lookup"><span data-stu-id="396fc-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="396fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="396fc-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="396fc-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396fc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="396fc-125">-ResourceId</span></span>
<span data-ttu-id="396fc-126">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="396fc-126">Resource Id.</span></span>

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

### <span data-ttu-id="396fc-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="396fc-127">-WorkspaceName</span></span>
<span data-ttu-id="396fc-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="396fc-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396fc-129">CommonParameters</span></span>
<span data-ttu-id="396fc-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396fc-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="396fc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396fc-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="396fc-132">INPUTS</span></span>

### <span data-ttu-id="396fc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="396fc-133">System.String</span></span>
## <span data-ttu-id="396fc-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="396fc-134">OUTPUTS</span></span>

### <span data-ttu-id="396fc-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="396fc-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="396fc-136">Notas</span><span class="sxs-lookup"><span data-stu-id="396fc-136">NOTES</span></span>

## <span data-ttu-id="396fc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="396fc-137">RELATED LINKS</span></span>
