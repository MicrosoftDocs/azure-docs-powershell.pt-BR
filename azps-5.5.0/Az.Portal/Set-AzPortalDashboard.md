---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114576"
---
# <span data-ttu-id="0d8ab-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="0d8ab-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="0d8ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d8ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8ab-103">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0d8ab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d8ab-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d8ab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d8ab-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8ab-106">Cria ou atualiza um Painel.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="0d8ab-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d8ab-107">EXAMPLES</span></span>

### <span data-ttu-id="0d8ab-108">Exemplo 1: Atualizar a definição do painel usando um modelo de painel</span><span class="sxs-lookup"><span data-stu-id="0d8ab-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="0d8ab-109">Atualize uma definição de painel usando um arquivo de modelo dashbaord.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="0d8ab-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d8ab-110">PARAMETERS</span></span>

### <span data-ttu-id="0d8ab-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="0d8ab-111">-DashboardPath</span></span>
<span data-ttu-id="0d8ab-112">O Caminho para um modelo de painel existente.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="0d8ab-113">Os modelos de painel podem ser baixados do portal.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="0d8ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8ab-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="0d8ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d8ab-115">-Name</span></span>


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

### <span data-ttu-id="0d8ab-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8ab-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="0d8ab-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d8ab-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="0d8ab-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0d8ab-118">-Confirm</span></span>
<span data-ttu-id="0d8ab-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d8ab-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8ab-120">-WhatIf</span></span>
<span data-ttu-id="0d8ab-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d8ab-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d8ab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8ab-123">CommonParameters</span></span>
<span data-ttu-id="0d8ab-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8ab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8ab-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d8ab-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8ab-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="0d8ab-126">INPUTS</span></span>

## <span data-ttu-id="0d8ab-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="0d8ab-127">OUTPUTS</span></span>

### <span data-ttu-id="0d8ab-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="0d8ab-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="0d8ab-129">Notas</span><span class="sxs-lookup"><span data-stu-id="0d8ab-129">NOTES</span></span>

<span data-ttu-id="0d8ab-130">Aliases</span><span class="sxs-lookup"><span data-stu-id="0d8ab-130">ALIASES</span></span>

## <span data-ttu-id="0d8ab-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d8ab-131">RELATED LINKS</span></span>

