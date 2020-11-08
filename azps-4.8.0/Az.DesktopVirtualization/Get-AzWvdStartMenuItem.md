---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112793"
---
# <span data-ttu-id="94929-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="94929-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="94929-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94929-102">SYNOPSIS</span></span>
<span data-ttu-id="94929-103">Listar itens do menu iniciar no grupo de aplicativos específico.</span><span class="sxs-lookup"><span data-stu-id="94929-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="94929-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94929-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94929-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94929-105">DESCRIPTION</span></span>
<span data-ttu-id="94929-106">Listar itens do menu iniciar no grupo de aplicativos específico.</span><span class="sxs-lookup"><span data-stu-id="94929-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="94929-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94929-107">EXAMPLES</span></span>

### <span data-ttu-id="94929-108">Exemplo 2: listar os itens do menu Iniciar da área de trabalho virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="94929-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="94929-109">Este comando lista os itens do menu Iniciar da área de trabalho virtual do Windows em um grupo do applicaton.</span><span class="sxs-lookup"><span data-stu-id="94929-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="94929-110">OS</span><span class="sxs-lookup"><span data-stu-id="94929-110">PARAMETERS</span></span>

### <span data-ttu-id="94929-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="94929-111">-ApplicationGroupName</span></span>
<span data-ttu-id="94929-112">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="94929-112">The name of the application group</span></span>

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

### <span data-ttu-id="94929-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94929-113">-DefaultProfile</span></span>
<span data-ttu-id="94929-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94929-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94929-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94929-115">-ResourceGroupName</span></span>
<span data-ttu-id="94929-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94929-116">The name of the resource group.</span></span>
<span data-ttu-id="94929-117">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="94929-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="94929-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94929-118">-SubscriptionId</span></span>
<span data-ttu-id="94929-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="94929-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="94929-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94929-120">CommonParameters</span></span>
<span data-ttu-id="94929-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94929-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94929-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94929-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94929-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94929-123">INPUTS</span></span>

## <span data-ttu-id="94929-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94929-124">OUTPUTS</span></span>

### <span data-ttu-id="94929-125">Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="94929-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="94929-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94929-126">NOTES</span></span>

<span data-ttu-id="94929-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="94929-127">ALIASES</span></span>

## <span data-ttu-id="94929-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94929-128">RELATED LINKS</span></span>

