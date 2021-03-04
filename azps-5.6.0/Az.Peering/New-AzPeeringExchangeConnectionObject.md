---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c4e57d3d7945f4ae06fc2461e660945bf7edfd6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890145"
---
# <span data-ttu-id="76527-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="76527-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="76527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76527-102">SYNOPSIS</span></span>
<span data-ttu-id="76527-103">Cria um PSObject na memória a ser usado para criar ou modificar um Peering.</span><span class="sxs-lookup"><span data-stu-id="76527-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="76527-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76527-104">SYNTAX</span></span>

### <span data-ttu-id="76527-105">IPv4Address (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76527-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76527-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="76527-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76527-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="76527-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76527-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76527-108">DESCRIPTION</span></span>
<span data-ttu-id="76527-109">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="76527-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="76527-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76527-110">EXAMPLES</span></span>

### <span data-ttu-id="76527-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76527-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="76527-112">Objeto connection local</span><span class="sxs-lookup"><span data-stu-id="76527-112">Local connection object</span></span>

## <span data-ttu-id="76527-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76527-113">PARAMETERS</span></span>

### <span data-ttu-id="76527-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76527-114">-DefaultProfile</span></span>
<span data-ttu-id="76527-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76527-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76527-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="76527-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="76527-117">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="76527-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76527-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="76527-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="76527-119">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="76527-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76527-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="76527-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="76527-121">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="76527-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="76527-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="76527-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="76527-123">A ID do recurso de paração encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="76527-123">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76527-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="76527-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="76527-125">O endereço IPv4 da sessão par</span><span class="sxs-lookup"><span data-stu-id="76527-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76527-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="76527-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="76527-127">O endereço IPv6 de sessão par</span><span class="sxs-lookup"><span data-stu-id="76527-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76527-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76527-128">CommonParameters</span></span>
<span data-ttu-id="76527-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76527-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76527-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76527-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76527-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76527-131">INPUTS</span></span>

### <span data-ttu-id="76527-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="76527-132">None</span></span>

## <span data-ttu-id="76527-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76527-133">OUTPUTS</span></span>

### <span data-ttu-id="76527-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="76527-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="76527-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="76527-135">NOTES</span></span>

## <span data-ttu-id="76527-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76527-136">RELATED LINKS</span></span>
