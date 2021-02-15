---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114520"
---
# <span data-ttu-id="83924-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="83924-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="83924-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83924-102">SYNOPSIS</span></span>
<span data-ttu-id="83924-103">Criar objeto Proprietário de Incidentes para atualizar um proprietário de incidente.</span><span class="sxs-lookup"><span data-stu-id="83924-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="83924-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83924-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83924-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="83924-105">DESCRIPTION</span></span>
<span data-ttu-id="83924-106">O cmdlet **New-AzSentinelIncidentOwner** cria um objeto Proprietário de Incidente na memória para atualizar um incidente.</span><span class="sxs-lookup"><span data-stu-id="83924-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="83924-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="83924-107">EXAMPLES</span></span>

### <span data-ttu-id="83924-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="83924-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="83924-109">Este exemplo cria um **IncidentOwner** e atualiza um Incidente para o novo proprietário.</span><span class="sxs-lookup"><span data-stu-id="83924-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="83924-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83924-110">PARAMETERS</span></span>

### <span data-ttu-id="83924-111">-AtribuídoPara</span><span class="sxs-lookup"><span data-stu-id="83924-111">-AssignedTo</span></span>
<span data-ttu-id="83924-112">Proprietário do Incidente – Atribuído a</span><span class="sxs-lookup"><span data-stu-id="83924-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="83924-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83924-113">-DefaultProfile</span></span>
<span data-ttu-id="83924-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83924-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83924-115">-Email</span><span class="sxs-lookup"><span data-stu-id="83924-115">-Email</span></span>
<span data-ttu-id="83924-116">Proprietário de Incidentes - Email</span><span class="sxs-lookup"><span data-stu-id="83924-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="83924-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="83924-117">-ObjectId</span></span>
<span data-ttu-id="83924-118">Proprietário de Incidentes - ObjectId</span><span class="sxs-lookup"><span data-stu-id="83924-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="83924-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="83924-119">-UserPrincipalName</span></span>
<span data-ttu-id="83924-120">Proprietário do Incidente – Nome de Entidade de Usuário</span><span class="sxs-lookup"><span data-stu-id="83924-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="83924-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83924-121">CommonParameters</span></span>
<span data-ttu-id="83924-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83924-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83924-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83924-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83924-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="83924-124">INPUTS</span></span>

### <span data-ttu-id="83924-125">Nenhum</span><span class="sxs-lookup"><span data-stu-id="83924-125">None</span></span>
## <span data-ttu-id="83924-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="83924-126">OUTPUTS</span></span>

### <span data-ttu-id="83924-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="83924-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="83924-128">Notas</span><span class="sxs-lookup"><span data-stu-id="83924-128">NOTES</span></span>

## <span data-ttu-id="83924-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83924-129">RELATED LINKS</span></span>
