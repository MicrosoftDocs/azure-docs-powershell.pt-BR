---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890087"
---
# <span data-ttu-id="24355-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="24355-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="24355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24355-102">SYNOPSIS</span></span>
<span data-ttu-id="24355-103">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="24355-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="24355-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24355-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24355-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24355-105">DESCRIPTION</span></span>
<span data-ttu-id="24355-106">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="24355-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="24355-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24355-107">EXAMPLES</span></span>

### <span data-ttu-id="24355-108">Exemplo 1: atualizar a definição do painel usando um modelo de painel</span><span class="sxs-lookup"><span data-stu-id="24355-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="24355-109">Atualize uma definição de painel usando um arquivo de modelo dashbaord.</span><span class="sxs-lookup"><span data-stu-id="24355-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="24355-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24355-110">PARAMETERS</span></span>

### <span data-ttu-id="24355-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="24355-111">-DashboardPath</span></span>
<span data-ttu-id="24355-112">O Caminho para um modelo de painel existente.</span><span class="sxs-lookup"><span data-stu-id="24355-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="24355-113">Modelos de painel podem ser baixados do portal.</span><span class="sxs-lookup"><span data-stu-id="24355-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="24355-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24355-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24355-115">-Name</span><span class="sxs-lookup"><span data-stu-id="24355-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24355-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24355-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="24355-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24355-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24355-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24355-118">-Confirm</span></span>
<span data-ttu-id="24355-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24355-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24355-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24355-120">-WhatIf</span></span>
<span data-ttu-id="24355-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24355-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24355-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24355-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24355-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24355-123">CommonParameters</span></span>
<span data-ttu-id="24355-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24355-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24355-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24355-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24355-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24355-126">INPUTS</span></span>

## <span data-ttu-id="24355-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24355-127">OUTPUTS</span></span>

### <span data-ttu-id="24355-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="24355-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="24355-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="24355-129">NOTES</span></span>

<span data-ttu-id="24355-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="24355-130">ALIASES</span></span>

## <span data-ttu-id="24355-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24355-131">RELATED LINKS</span></span>

