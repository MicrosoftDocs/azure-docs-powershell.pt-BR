---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2020
ms.locfileid: "93945215"
---
# <span data-ttu-id="e0993-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0993-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="e0993-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0993-102">SYNOPSIS</span></span>
<span data-ttu-id="e0993-103">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="e0993-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e0993-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0993-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e0993-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0993-105">DESCRIPTION</span></span>
<span data-ttu-id="e0993-106">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="e0993-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="e0993-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0993-107">EXAMPLES</span></span>

### <span data-ttu-id="e0993-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e0993-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="e0993-109">OS</span><span class="sxs-lookup"><span data-stu-id="e0993-109">PARAMETERS</span></span>

### <span data-ttu-id="e0993-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0993-110">-DefaultProfile</span></span>
<span data-ttu-id="e0993-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0993-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0993-112">-Filtro</span><span class="sxs-lookup"><span data-stu-id="e0993-112">-Filter</span></span>
<span data-ttu-id="e0993-113">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="e0993-113">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0993-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="e0993-114">-InlineCount</span></span>
<span data-ttu-id="e0993-115">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="e0993-115">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0993-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e0993-116">-OrderBy</span></span>
<span data-ttu-id="e0993-117">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="e0993-117">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0993-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="e0993-118">-Skip</span></span>
<span data-ttu-id="e0993-119">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="e0993-119">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0993-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0993-120">-SubscriptionId</span></span>
<span data-ttu-id="e0993-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e0993-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0993-122">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="e0993-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0993-123">-Início</span><span class="sxs-lookup"><span data-stu-id="e0993-123">-Top</span></span>
<span data-ttu-id="e0993-124">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="e0993-124">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e0993-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0993-125">CommonParameters</span></span>
<span data-ttu-id="e0993-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0993-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0993-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0993-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0993-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0993-128">INPUTS</span></span>

## <span data-ttu-id="e0993-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0993-129">OUTPUTS</span></span>

### <span data-ttu-id="e0993-130">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0993-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="e0993-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0993-131">NOTES</span></span>

## <span data-ttu-id="e0993-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0993-132">RELATED LINKS</span></span>

