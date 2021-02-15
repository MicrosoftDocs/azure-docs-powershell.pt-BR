---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111521"
---
# <span data-ttu-id="e4996-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e4996-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="e4996-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4996-102">SYNOPSIS</span></span>
<span data-ttu-id="e4996-103">Obtém os locais de peering oferecidos pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="e4996-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="e4996-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4996-104">SYNTAX</span></span>

### <span data-ttu-id="e4996-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e4996-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4996-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="e4996-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4996-107">LocalByDirectType</span><span class="sxs-lookup"><span data-stu-id="e4996-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4996-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4996-108">DESCRIPTION</span></span>
<span data-ttu-id="e4996-109">Obtém as Instalações de Peering onde os usuários podem se conectar com ARM.</span><span class="sxs-lookup"><span data-stu-id="e4996-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="e4996-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4996-110">EXAMPLES</span></span>

### <span data-ttu-id="e4996-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e4996-111">Example 1</span></span>
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

<span data-ttu-id="e4996-112">É uma longa lista de locais.</span><span class="sxs-lookup"><span data-stu-id="e4996-112">Its a long list of locations.</span></span> <span data-ttu-id="e4996-113">Obtém todas as Instalações de Peering Direto.</span><span class="sxs-lookup"><span data-stu-id="e4996-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="e4996-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e4996-114">Example 2</span></span>
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

<span data-ttu-id="e4996-115">Obtém o local de paridade do exchange para Honolulu.</span><span class="sxs-lookup"><span data-stu-id="e4996-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="e4996-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e4996-116">Example 3</span></span>
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

<span data-ttu-id="e4996-117">Obtém o local de peering do Exchange para a ID da instalação de paração 71.</span><span class="sxs-lookup"><span data-stu-id="e4996-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="e4996-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4996-118">PARAMETERS</span></span>

### <span data-ttu-id="e4996-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4996-119">-DefaultProfile</span></span>
<span data-ttu-id="e4996-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4996-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4996-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="e4996-121">-DirectPeeringType</span></span>
<span data-ttu-id="e4996-122">Selecione "Borda", "CDN" e "Trânsito".</span><span class="sxs-lookup"><span data-stu-id="e4996-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4996-123">-Tipo</span><span class="sxs-lookup"><span data-stu-id="e4996-123">-Kind</span></span>
<span data-ttu-id="e4996-124">Mostra todos os recursos de Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="e4996-124">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="e4996-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="e4996-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="e4996-126">A PeeringDB.com de instalação</span><span class="sxs-lookup"><span data-stu-id="e4996-126">The PeeringDB.com Facility ID</span></span>

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

### <span data-ttu-id="e4996-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e4996-127">-PeeringLocation</span></span>
<span data-ttu-id="e4996-128">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="e4996-128">The location of the resource.</span></span>

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

### <span data-ttu-id="e4996-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4996-129">CommonParameters</span></span>
<span data-ttu-id="e4996-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4996-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4996-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4996-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4996-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4996-132">INPUTS</span></span>

### <span data-ttu-id="e4996-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e4996-133">None</span></span>

## <span data-ttu-id="e4996-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4996-134">OUTPUTS</span></span>

### <span data-ttu-id="e4996-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="e4996-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="e4996-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e4996-136">NOTES</span></span>

## <span data-ttu-id="e4996-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4996-137">RELATED LINKS</span></span>
