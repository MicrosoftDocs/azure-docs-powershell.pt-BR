---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775998"
---
# <span data-ttu-id="213f7-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213f7-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="213f7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="213f7-102">SYNOPSIS</span></span>
<span data-ttu-id="213f7-103">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="213f7-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="213f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="213f7-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="213f7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="213f7-105">DESCRIPTION</span></span>
<span data-ttu-id="213f7-106">Obtenha uma lista de todos os balanceadores de carga.</span><span class="sxs-lookup"><span data-stu-id="213f7-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="213f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="213f7-107">EXAMPLES</span></span>

### <span data-ttu-id="213f7-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="213f7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="213f7-109">OS</span><span class="sxs-lookup"><span data-stu-id="213f7-109">PARAMETERS</span></span>

### <span data-ttu-id="213f7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="213f7-110">-DefaultProfile</span></span>
<span data-ttu-id="213f7-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="213f7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="213f7-112">-Filtro</span><span class="sxs-lookup"><span data-stu-id="213f7-112">-Filter</span></span>
<span data-ttu-id="213f7-113">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="213f7-113">OData filter parameter.</span></span>

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

### <span data-ttu-id="213f7-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="213f7-114">-InlineCount</span></span>
<span data-ttu-id="213f7-115">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="213f7-115">OData inline count parameter.</span></span>

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

### <span data-ttu-id="213f7-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="213f7-116">-OrderBy</span></span>
<span data-ttu-id="213f7-117">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="213f7-117">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="213f7-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="213f7-118">-Skip</span></span>
<span data-ttu-id="213f7-119">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="213f7-119">OData skip parameter.</span></span>

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

### <span data-ttu-id="213f7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="213f7-120">-SubscriptionId</span></span>
<span data-ttu-id="213f7-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="213f7-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="213f7-122">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="213f7-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="213f7-123">-Início</span><span class="sxs-lookup"><span data-stu-id="213f7-123">-Top</span></span>
<span data-ttu-id="213f7-124">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="213f7-124">OData top parameter.</span></span>

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

### <span data-ttu-id="213f7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="213f7-125">CommonParameters</span></span>
<span data-ttu-id="213f7-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="213f7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="213f7-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="213f7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="213f7-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="213f7-128">INPUTS</span></span>

## <span data-ttu-id="213f7-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="213f7-129">OUTPUTS</span></span>

### <span data-ttu-id="213f7-130">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. ILoadBalancer</span><span class="sxs-lookup"><span data-stu-id="213f7-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="213f7-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="213f7-131">NOTES</span></span>

## <span data-ttu-id="213f7-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="213f7-132">RELATED LINKS</span></span>

