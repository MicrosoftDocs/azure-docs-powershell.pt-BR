---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257920"
---
# <span data-ttu-id="736cf-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="736cf-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="736cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="736cf-102">SYNOPSIS</span></span>
<span data-ttu-id="736cf-103">Cria ou atualiza um painel.</span><span class="sxs-lookup"><span data-stu-id="736cf-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="736cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="736cf-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="736cf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="736cf-105">DESCRIPTION</span></span>
<span data-ttu-id="736cf-106">Cria ou atualiza um painel.</span><span class="sxs-lookup"><span data-stu-id="736cf-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="736cf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="736cf-107">EXAMPLES</span></span>

### <span data-ttu-id="736cf-108">Exemplo 1: atualizar a definição do painel usando um modelo de painel</span><span class="sxs-lookup"><span data-stu-id="736cf-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="736cf-109">Atualize uma definição de painel usando um arquivo de modelo do dashbaord.</span><span class="sxs-lookup"><span data-stu-id="736cf-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="736cf-110">OS</span><span class="sxs-lookup"><span data-stu-id="736cf-110">PARAMETERS</span></span>

### <span data-ttu-id="736cf-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="736cf-111">-DashboardPath</span></span>
<span data-ttu-id="736cf-112">O caminho para um modelo de painel existente.</span><span class="sxs-lookup"><span data-stu-id="736cf-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="736cf-113">Os modelos de painel podem ser baixados do Portal.</span><span class="sxs-lookup"><span data-stu-id="736cf-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="736cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736cf-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="736cf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="736cf-115">-Name</span></span>


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

### <span data-ttu-id="736cf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="736cf-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="736cf-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="736cf-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="736cf-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="736cf-118">-Confirm</span></span>
<span data-ttu-id="736cf-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="736cf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="736cf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="736cf-120">-WhatIf</span></span>
<span data-ttu-id="736cf-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="736cf-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="736cf-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="736cf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="736cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736cf-123">CommonParameters</span></span>
<span data-ttu-id="736cf-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="736cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736cf-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="736cf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736cf-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="736cf-126">INPUTS</span></span>

## <span data-ttu-id="736cf-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="736cf-127">OUTPUTS</span></span>

### <span data-ttu-id="736cf-128">Microsoft. Azure. PowerShell. cmdlets. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="736cf-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="736cf-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="736cf-129">NOTES</span></span>

<span data-ttu-id="736cf-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="736cf-130">ALIASES</span></span>

## <span data-ttu-id="736cf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="736cf-131">RELATED LINKS</span></span>

