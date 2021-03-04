---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888956"
---
# <span data-ttu-id="8673a-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="8673a-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="8673a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8673a-102">SYNOPSIS</span></span>
<span data-ttu-id="8673a-103">Listar itens do menu iniciar no grupo de aplicativos determinado.</span><span class="sxs-lookup"><span data-stu-id="8673a-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="8673a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8673a-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8673a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8673a-105">DESCRIPTION</span></span>
<span data-ttu-id="8673a-106">Listar itens do menu iniciar no grupo de aplicativos determinado.</span><span class="sxs-lookup"><span data-stu-id="8673a-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="8673a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8673a-107">EXAMPLES</span></span>

### <span data-ttu-id="8673a-108">Exemplo 2: Listar itens do menu Iniciar da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="8673a-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="8673a-109">Este comando lista os itens do menu Iniciar da Área de Trabalho Virtual do Windows em um grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8673a-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="8673a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8673a-110">PARAMETERS</span></span>

### <span data-ttu-id="8673a-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="8673a-111">-ApplicationGroupName</span></span>
<span data-ttu-id="8673a-112">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8673a-112">The name of the application group</span></span>

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

### <span data-ttu-id="8673a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8673a-113">-DefaultProfile</span></span>
<span data-ttu-id="8673a-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8673a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8673a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8673a-115">-ResourceGroupName</span></span>
<span data-ttu-id="8673a-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8673a-116">The name of the resource group.</span></span>
<span data-ttu-id="8673a-117">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8673a-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8673a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8673a-118">-SubscriptionId</span></span>
<span data-ttu-id="8673a-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8673a-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8673a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8673a-120">CommonParameters</span></span>
<span data-ttu-id="8673a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8673a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8673a-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8673a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8673a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8673a-123">INPUTS</span></span>

## <span data-ttu-id="8673a-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8673a-124">OUTPUTS</span></span>

### <span data-ttu-id="8673a-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="8673a-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="8673a-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="8673a-126">NOTES</span></span>

<span data-ttu-id="8673a-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8673a-127">ALIASES</span></span>

## <span data-ttu-id="8673a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8673a-128">RELATED LINKS</span></span>

