---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433213"
---
# <span data-ttu-id="bc794-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="bc794-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="bc794-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc794-102">SYNOPSIS</span></span>
<span data-ttu-id="bc794-103">Obter um incidente.</span><span class="sxs-lookup"><span data-stu-id="bc794-103">Get an Incident.</span></span>

## <span data-ttu-id="bc794-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc794-104">SYNTAX</span></span>

### <span data-ttu-id="bc794-105">WorkspaceScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc794-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc794-106">Incidentid</span><span class="sxs-lookup"><span data-stu-id="bc794-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc794-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="bc794-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc794-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc794-108">DESCRIPTION</span></span>
<span data-ttu-id="bc794-109">O cmdlet **Get-AzSentinelIncident** Obtém um incidente do espaço de trabalho especificado.</span><span class="sxs-lookup"><span data-stu-id="bc794-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="bc794-110">Se você especificar o parâmetro *incidentid* , um único objeto de **incidente** será retornado.</span><span class="sxs-lookup"><span data-stu-id="bc794-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="bc794-111">Se você não especificar o parâmetro *incidentid* , uma matriz contendo todos os incidentes no espaço de trabalho especificado será retornada.</span><span class="sxs-lookup"><span data-stu-id="bc794-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="bc794-112">Você pode usar o objeto de **incidente** para atualizar o incidente, por exemplo, você pode adicionar anotações ao **incidente**.</span><span class="sxs-lookup"><span data-stu-id="bc794-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="bc794-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc794-113">EXAMPLES</span></span>

### <span data-ttu-id="bc794-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc794-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="bc794-115">Este exemplo obtém todos os **incidentes** no espaço de trabalho especificado e, em seguida, armazena-os na variável $Incidents.</span><span class="sxs-lookup"><span data-stu-id="bc794-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="bc794-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bc794-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="bc794-117">Este exemplo obtém um **incidente** no espaço de trabalho especificado e, em seguida, armazena-o na variável $Incident.</span><span class="sxs-lookup"><span data-stu-id="bc794-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="bc794-118">OS</span><span class="sxs-lookup"><span data-stu-id="bc794-118">PARAMETERS</span></span>

### <span data-ttu-id="bc794-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc794-119">-DefaultProfile</span></span>
<span data-ttu-id="bc794-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc794-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc794-121">-Incidentid</span><span class="sxs-lookup"><span data-stu-id="bc794-121">-IncidentId</span></span>
<span data-ttu-id="bc794-122">ID do incidente.</span><span class="sxs-lookup"><span data-stu-id="bc794-122">Incident Id.</span></span>

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

### <span data-ttu-id="bc794-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc794-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc794-124">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc794-124">Resource group name.</span></span>

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

### <span data-ttu-id="bc794-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc794-125">-ResourceId</span></span>
<span data-ttu-id="bc794-126">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc794-126">Resource Id.</span></span>

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

### <span data-ttu-id="bc794-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bc794-127">-WorkspaceName</span></span>
<span data-ttu-id="bc794-128">Nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bc794-128">Workspace Name.</span></span>

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

### <span data-ttu-id="bc794-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc794-129">CommonParameters</span></span>
<span data-ttu-id="bc794-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc794-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc794-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc794-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc794-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc794-132">INPUTS</span></span>

### <span data-ttu-id="bc794-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bc794-133">System.String</span></span>
## <span data-ttu-id="bc794-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc794-134">OUTPUTS</span></span>

### <span data-ttu-id="bc794-135">Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="bc794-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="bc794-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc794-136">NOTES</span></span>

## <span data-ttu-id="bc794-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc794-137">RELATED LINKS</span></span>
