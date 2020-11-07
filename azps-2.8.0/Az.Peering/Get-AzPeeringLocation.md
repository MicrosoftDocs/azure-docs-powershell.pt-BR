---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: cc8e0c5e4ce47b3157d5518ce1e5bc6b9919ff41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772862"
---
# <span data-ttu-id="8eb94-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8eb94-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="8eb94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8eb94-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb94-103">Obtém os locais de emparelhamento oferecidos pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="8eb94-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="8eb94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8eb94-104">SYNTAX</span></span>

### <span data-ttu-id="8eb94-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="8eb94-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8eb94-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="8eb94-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eb94-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="8eb94-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType] <String>
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eb94-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8eb94-108">DESCRIPTION</span></span>
<span data-ttu-id="8eb94-109">Obtém os recursos de emparelhamento em que os usuários podem se conectar com o ARM.</span><span class="sxs-lookup"><span data-stu-id="8eb94-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="8eb94-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8eb94-110">EXAMPLES</span></span>

### <span data-ttu-id="8eb94-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8eb94-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="8eb94-112">Uma longa lista de locais.</span><span class="sxs-lookup"><span data-stu-id="8eb94-112">Its a long list of locations.</span></span> <span data-ttu-id="8eb94-113">Obtém todos os recursos de emparelhamento direto.</span><span class="sxs-lookup"><span data-stu-id="8eb94-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="8eb94-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8eb94-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="8eb94-115">Obtém o local de emparelhamento do Exchange para Honolulu.</span><span class="sxs-lookup"><span data-stu-id="8eb94-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="8eb94-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8eb94-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="8eb94-117">Obtém o local de emparelhamento do Exchange para a identificação de recursos de emparelhamento 71.</span><span class="sxs-lookup"><span data-stu-id="8eb94-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="8eb94-118">OS</span><span class="sxs-lookup"><span data-stu-id="8eb94-118">PARAMETERS</span></span>

### <span data-ttu-id="8eb94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb94-119">-DefaultProfile</span></span>
<span data-ttu-id="8eb94-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8eb94-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb94-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="8eb94-121">-DirectPeeringType</span></span>
<span data-ttu-id="8eb94-122">Selecione ' Edge ', ' CDN ' e ' trânsito '.</span><span class="sxs-lookup"><span data-stu-id="8eb94-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb94-123">-Kind</span><span class="sxs-lookup"><span data-stu-id="8eb94-123">-Kind</span></span>
<span data-ttu-id="8eb94-124">Mostra todos os recursos de emparelhamento por tipo.</span><span class="sxs-lookup"><span data-stu-id="8eb94-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb94-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="8eb94-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="8eb94-126">A ID do recurso PeeringDB.com</span><span class="sxs-lookup"><span data-stu-id="8eb94-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb94-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8eb94-127">-PeeringLocation</span></span>
<span data-ttu-id="8eb94-128">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8eb94-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb94-129">CommonParameters</span></span>
<span data-ttu-id="8eb94-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb94-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8eb94-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb94-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8eb94-132">INPUTS</span></span>

### <span data-ttu-id="8eb94-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8eb94-133">None</span></span>

## <span data-ttu-id="8eb94-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8eb94-134">OUTPUTS</span></span>

### <span data-ttu-id="8eb94-135">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="8eb94-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="8eb94-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8eb94-136">NOTES</span></span>

## <span data-ttu-id="8eb94-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8eb94-137">RELATED LINKS</span></span>
