---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775988"
---
# <span data-ttu-id="27ae4-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27ae4-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="27ae4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="27ae4-103">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="27ae4-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="27ae4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27ae4-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="27ae4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="27ae4-106">Obter uma lista de todas as redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="27ae4-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="27ae4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="27ae4-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27ae4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="27ae4-109">Retornar uma lista de redes virtuais para o selo de pilha do Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae4-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="27ae4-110">OS</span><span class="sxs-lookup"><span data-stu-id="27ae4-110">PARAMETERS</span></span>

### <span data-ttu-id="27ae4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ae4-111">-DefaultProfile</span></span>
<span data-ttu-id="27ae4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ae4-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="27ae4-113">-Filter</span></span>
<span data-ttu-id="27ae4-114">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="27ae4-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="27ae4-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="27ae4-115">-InlineCount</span></span>
<span data-ttu-id="27ae4-116">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="27ae4-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="27ae4-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="27ae4-117">-OrderBy</span></span>
<span data-ttu-id="27ae4-118">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="27ae4-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="27ae4-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="27ae4-119">-Skip</span></span>
<span data-ttu-id="27ae4-120">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="27ae4-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="27ae4-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27ae4-121">-SubscriptionId</span></span>
<span data-ttu-id="27ae4-122">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="27ae4-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="27ae4-123">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="27ae4-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="27ae4-124">-Início</span><span class="sxs-lookup"><span data-stu-id="27ae4-124">-Top</span></span>
<span data-ttu-id="27ae4-125">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="27ae4-125">OData top parameter.</span></span>

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

### <span data-ttu-id="27ae4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ae4-126">CommonParameters</span></span>
<span data-ttu-id="27ae4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ae4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ae4-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27ae4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ae4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27ae4-129">INPUTS</span></span>

## <span data-ttu-id="27ae4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27ae4-130">OUTPUTS</span></span>

### <span data-ttu-id="27ae4-131">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="27ae4-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="27ae4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27ae4-132">NOTES</span></span>

## <span data-ttu-id="27ae4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27ae4-133">RELATED LINKS</span></span>

