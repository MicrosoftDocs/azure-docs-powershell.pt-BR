---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: fd91ea79cbad51d03c0986ed5f55601af240de16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115830"
---
# <span data-ttu-id="09d3a-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="09d3a-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="09d3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09d3a-102">SYNOPSIS</span></span>
<span data-ttu-id="09d3a-103">Listar itens do menu Iniciar no grupo de aplicativos determinado.</span><span class="sxs-lookup"><span data-stu-id="09d3a-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="09d3a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09d3a-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="09d3a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="09d3a-105">DESCRIPTION</span></span>
<span data-ttu-id="09d3a-106">Listar itens do menu Iniciar no grupo de aplicativos determinado.</span><span class="sxs-lookup"><span data-stu-id="09d3a-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="09d3a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09d3a-107">EXAMPLES</span></span>

### <span data-ttu-id="09d3a-108">Exemplo 2: Listar itens do menu Iniciar da Área de Trabalho Virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="09d3a-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="09d3a-109">Este comando lista os Itens do Menu Iniciar da Área de Trabalho Virtual do Windows em um Grupo de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="09d3a-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="09d3a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09d3a-110">PARAMETERS</span></span>

### <span data-ttu-id="09d3a-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="09d3a-111">-ApplicationGroupName</span></span>
<span data-ttu-id="09d3a-112">O nome do grupo de aplicativos</span><span class="sxs-lookup"><span data-stu-id="09d3a-112">The name of the application group</span></span>

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

### <span data-ttu-id="09d3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d3a-113">-DefaultProfile</span></span>
<span data-ttu-id="09d3a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09d3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09d3a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d3a-115">-ResourceGroupName</span></span>
<span data-ttu-id="09d3a-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09d3a-116">The name of the resource group.</span></span>
<span data-ttu-id="09d3a-117">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="09d3a-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="09d3a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09d3a-118">-SubscriptionId</span></span>
<span data-ttu-id="09d3a-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="09d3a-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="09d3a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d3a-120">CommonParameters</span></span>
<span data-ttu-id="09d3a-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d3a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d3a-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09d3a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d3a-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="09d3a-123">INPUTS</span></span>

## <span data-ttu-id="09d3a-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="09d3a-124">OUTPUTS</span></span>

### <span data-ttu-id="09d3a-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="09d3a-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="09d3a-126">Notas</span><span class="sxs-lookup"><span data-stu-id="09d3a-126">NOTES</span></span>

<span data-ttu-id="09d3a-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="09d3a-127">ALIASES</span></span>

## <span data-ttu-id="09d3a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09d3a-128">RELATED LINKS</span></span>

