---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272545"
---
# <span data-ttu-id="f518e-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f518e-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="f518e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f518e-102">SYNOPSIS</span></span>
<span data-ttu-id="f518e-103">Cria um PSObject na memória a ser usado para criar ou modificar um emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="f518e-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="f518e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f518e-104">SYNTAX</span></span>

### <span data-ttu-id="f518e-105">IPv4Address (padrão)</span><span class="sxs-lookup"><span data-stu-id="f518e-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f518e-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="f518e-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f518e-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="f518e-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f518e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f518e-108">DESCRIPTION</span></span>
<span data-ttu-id="f518e-109">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="f518e-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="f518e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f518e-110">EXAMPLES</span></span>

### <span data-ttu-id="f518e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f518e-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="f518e-112">Objeto de conexão local</span><span class="sxs-lookup"><span data-stu-id="f518e-112">Local connection object</span></span>

## <span data-ttu-id="f518e-113">OS</span><span class="sxs-lookup"><span data-stu-id="f518e-113">PARAMETERS</span></span>

### <span data-ttu-id="f518e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f518e-114">-DefaultProfile</span></span>
<span data-ttu-id="f518e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f518e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f518e-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="f518e-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="f518e-117">O valor máximo de IPv4 anunciado</span><span class="sxs-lookup"><span data-stu-id="f518e-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="f518e-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="f518e-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="f518e-119">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="f518e-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="f518e-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="f518e-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="f518e-121">A chave de autenticação MD5 para a sessão.</span><span class="sxs-lookup"><span data-stu-id="f518e-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="f518e-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="f518e-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="f518e-123">A ID de recursos de emparelhamento encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="f518e-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="f518e-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="f518e-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="f518e-125">O endereço IPv4 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="f518e-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="f518e-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="f518e-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="f518e-127">O endereço IPv6 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="f518e-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="f518e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f518e-128">CommonParameters</span></span>
<span data-ttu-id="f518e-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f518e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f518e-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f518e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f518e-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f518e-131">INPUTS</span></span>

### <span data-ttu-id="f518e-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f518e-132">None</span></span>

## <span data-ttu-id="f518e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f518e-133">OUTPUTS</span></span>

### <span data-ttu-id="f518e-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="f518e-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="f518e-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f518e-135">NOTES</span></span>

## <span data-ttu-id="f518e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f518e-136">RELATED LINKS</span></span>
