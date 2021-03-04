---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: b8981d40f3412dd77ca120cd80d29fb160915e8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885256"
---
# <span data-ttu-id="39b75-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="39b75-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="39b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b75-102">SYNOPSIS</span></span>
<span data-ttu-id="39b75-103">Crie o objeto Proprietário de Incidentes para atualizar um proprietário de incidentes.</span><span class="sxs-lookup"><span data-stu-id="39b75-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="39b75-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="39b75-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b75-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="39b75-105">DESCRIPTION</span></span>
<span data-ttu-id="39b75-106">O cmdlet **New-AzSentinelIncidentOwner** cria um objeto Incident Owner na memória para atualizar um incidente.</span><span class="sxs-lookup"><span data-stu-id="39b75-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="39b75-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39b75-107">EXAMPLES</span></span>

### <span data-ttu-id="39b75-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39b75-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="39b75-109">Este exemplo cria um **IncidentOwner** e atualiza um Incidente para o novo proprietário.</span><span class="sxs-lookup"><span data-stu-id="39b75-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="39b75-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="39b75-110">PARAMETERS</span></span>

### <span data-ttu-id="39b75-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="39b75-111">-AssignedTo</span></span>
<span data-ttu-id="39b75-112">Proprietário de Incidentes - Atribuído a</span><span class="sxs-lookup"><span data-stu-id="39b75-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="39b75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b75-113">-DefaultProfile</span></span>
<span data-ttu-id="39b75-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39b75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b75-115">-Email</span><span class="sxs-lookup"><span data-stu-id="39b75-115">-Email</span></span>
<span data-ttu-id="39b75-116">Proprietário de Incidentes - Email</span><span class="sxs-lookup"><span data-stu-id="39b75-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="39b75-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="39b75-117">-ObjectId</span></span>
<span data-ttu-id="39b75-118">Proprietário do Incidente - ObjectId</span><span class="sxs-lookup"><span data-stu-id="39b75-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="39b75-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="39b75-119">-UserPrincipalName</span></span>
<span data-ttu-id="39b75-120">Proprietário do Incidente - Nome principal do usuário</span><span class="sxs-lookup"><span data-stu-id="39b75-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="39b75-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b75-121">CommonParameters</span></span>
<span data-ttu-id="39b75-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b75-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b75-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39b75-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b75-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39b75-124">INPUTS</span></span>

### <span data-ttu-id="39b75-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="39b75-125">None</span></span>
## <span data-ttu-id="39b75-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="39b75-126">OUTPUTS</span></span>

### <span data-ttu-id="39b75-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="39b75-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="39b75-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="39b75-128">NOTES</span></span>

## <span data-ttu-id="39b75-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39b75-129">RELATED LINKS</span></span>
