---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: c09ff4ad7762eafc18d7890f9611c9b989841c95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777888"
---
# <span data-ttu-id="9bffb-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="9bffb-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="9bffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bffb-102">SYNOPSIS</span></span>
<span data-ttu-id="9bffb-103">Define ou atualiza as informações de conexão do Exchange.</span><span class="sxs-lookup"><span data-stu-id="9bffb-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="9bffb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bffb-104">SYNTAX</span></span>

### <span data-ttu-id="9bffb-105">IPv6Address (padrão)</span><span class="sxs-lookup"><span data-stu-id="9bffb-105">IPv6Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bffb-106">IPv4Address</span><span class="sxs-lookup"><span data-stu-id="9bffb-106">IPv4Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bffb-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="9bffb-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bffb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bffb-108">DESCRIPTION</span></span>
<span data-ttu-id="9bffb-109">Usado em conjunto com Update-AzPeering, essa é uma operação de memória em memória e só será persistente `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="9bffb-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="9bffb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bffb-110">EXAMPLES</span></span>

### <span data-ttu-id="9bffb-111">Atualizar hash MD5</span><span class="sxs-lookup"><span data-stu-id="9bffb-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="9bffb-112">Atualiza o hash MD5 para a primeira conexão no objeto de emparelhamento na memória.</span><span class="sxs-lookup"><span data-stu-id="9bffb-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="9bffb-113">Atualizar o endereço da sessão do BGP</span><span class="sxs-lookup"><span data-stu-id="9bffb-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="9bffb-114">Atualiza o endereço de emparelhamento da primeira conexão no objeto de emparelhamento na memória.</span><span class="sxs-lookup"><span data-stu-id="9bffb-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="9bffb-115">OS</span><span class="sxs-lookup"><span data-stu-id="9bffb-115">PARAMETERS</span></span>

### <span data-ttu-id="9bffb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bffb-116">-DefaultProfile</span></span>
<span data-ttu-id="9bffb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bffb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bffb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bffb-118">-InputObject</span></span>
<span data-ttu-id="9bffb-119">O objeto de conexão do Exchange</span><span class="sxs-lookup"><span data-stu-id="9bffb-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="9bffb-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="9bffb-121">O valor máximo de IPv4 anunciado</span><span class="sxs-lookup"><span data-stu-id="9bffb-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="9bffb-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="9bffb-123">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="9bffb-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="9bffb-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="9bffb-125">A chave de autenticação MD5 para a sessão.</span><span class="sxs-lookup"><span data-stu-id="9bffb-125">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="9bffb-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="9bffb-127">O endereço IPv4 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="9bffb-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="9bffb-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="9bffb-129">O endereço IPv6 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="9bffb-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bffb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bffb-130">CommonParameters</span></span>
<span data-ttu-id="9bffb-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bffb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bffb-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bffb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bffb-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bffb-133">INPUTS</span></span>

### <span data-ttu-id="9bffb-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="9bffb-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="9bffb-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bffb-135">OUTPUTS</span></span>

### <span data-ttu-id="9bffb-136">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="9bffb-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="9bffb-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bffb-137">NOTES</span></span>

## <span data-ttu-id="9bffb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bffb-138">RELATED LINKS</span></span>
