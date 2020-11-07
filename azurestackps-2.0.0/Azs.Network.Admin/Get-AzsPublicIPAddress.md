---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
schema: 2.0.0
ms.openlocfilehash: d63133d082af8a9938b2e39318d05ec4ba0d0eb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775986"
---
# <span data-ttu-id="7734a-101">Get-AzsPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="7734a-101">Get-AzsPublicIPAddress</span></span>

## <span data-ttu-id="7734a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7734a-102">SYNOPSIS</span></span>
<span data-ttu-id="7734a-103">Lista de endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="7734a-103">List of public ip addresses.</span></span>

## <span data-ttu-id="7734a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7734a-104">SYNTAX</span></span>

```
Get-AzsPublicIPAddress [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7734a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7734a-105">DESCRIPTION</span></span>
<span data-ttu-id="7734a-106">Lista de endereços IP públicos.</span><span class="sxs-lookup"><span data-stu-id="7734a-106">List of public ip addresses.</span></span>

## <span data-ttu-id="7734a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7734a-107">EXAMPLES</span></span>

### <span data-ttu-id="7734a-108">--------------------------EXEMPLO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7734a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsPublicIPAddress
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azspublicipaddress
```

<span data-ttu-id="7734a-109">Obter a lista de endereços IP públicos, atribuídos ou não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="7734a-109">Get the list of public ip addresses, either allocated or not allocated.</span></span>

## <span data-ttu-id="7734a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7734a-110">PARAMETERS</span></span>

### <span data-ttu-id="7734a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7734a-111">-DefaultProfile</span></span>
<span data-ttu-id="7734a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7734a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7734a-113">-Filtro</span><span class="sxs-lookup"><span data-stu-id="7734a-113">-Filter</span></span>
<span data-ttu-id="7734a-114">Parâmetro de filtro OData.</span><span class="sxs-lookup"><span data-stu-id="7734a-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="7734a-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="7734a-115">-InlineCount</span></span>
<span data-ttu-id="7734a-116">Parâmetro de contagem embutida do OData.</span><span class="sxs-lookup"><span data-stu-id="7734a-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="7734a-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="7734a-117">-OrderBy</span></span>
<span data-ttu-id="7734a-118">Parâmetro orderBy do OData.</span><span class="sxs-lookup"><span data-stu-id="7734a-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="7734a-119">-Skip</span><span class="sxs-lookup"><span data-stu-id="7734a-119">-Skip</span></span>
<span data-ttu-id="7734a-120">Parâmetro de ignorar OData.</span><span class="sxs-lookup"><span data-stu-id="7734a-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="7734a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7734a-121">-SubscriptionId</span></span>
<span data-ttu-id="7734a-122">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7734a-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7734a-123">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7734a-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7734a-124">-Início</span><span class="sxs-lookup"><span data-stu-id="7734a-124">-Top</span></span>
<span data-ttu-id="7734a-125">Parâmetro de topo do OData.</span><span class="sxs-lookup"><span data-stu-id="7734a-125">OData top parameter.</span></span>

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

### <span data-ttu-id="7734a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7734a-126">CommonParameters</span></span>
<span data-ttu-id="7734a-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7734a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7734a-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7734a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7734a-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7734a-129">INPUTS</span></span>

## <span data-ttu-id="7734a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7734a-130">OUTPUTS</span></span>

### <span data-ttu-id="7734a-131">Microsoft. Azure. PowerShell. cmdlets. NetworkAdmin. Models. Api20150615. IPublicIPAddress</span><span class="sxs-lookup"><span data-stu-id="7734a-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IPublicIPAddress</span></span>



## <span data-ttu-id="7734a-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7734a-132">NOTES</span></span>

## <span data-ttu-id="7734a-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7734a-133">RELATED LINKS</span></span>

