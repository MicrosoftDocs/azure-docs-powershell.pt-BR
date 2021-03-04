---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d935f980b776ad6f61fe705a14e0da2a375d1e1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890124"
---
# <span data-ttu-id="b7cad-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b7cad-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="b7cad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cad-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cad-103">Define ou atualiza as informações do Exchange Connection.</span><span class="sxs-lookup"><span data-stu-id="b7cad-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="b7cad-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7cad-104">SYNTAX</span></span>

### <span data-ttu-id="b7cad-105">IPv4Address (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7cad-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7cad-106">IPv6Address</span><span class="sxs-lookup"><span data-stu-id="b7cad-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7cad-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="b7cad-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7cad-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7cad-108">DESCRIPTION</span></span>
<span data-ttu-id="b7cad-109">Usada em conjunto com Update-AzPeering, esta é uma operação na memória e só persistirá com `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="b7cad-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="b7cad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7cad-110">EXAMPLES</span></span>

### <span data-ttu-id="b7cad-111">Atualizar Hash Md5</span><span class="sxs-lookup"><span data-stu-id="b7cad-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="b7cad-112">Atualiza o Hash Md5 para a primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="b7cad-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="b7cad-113">Atualizar Endereço de Sessão Bgp</span><span class="sxs-lookup"><span data-stu-id="b7cad-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="b7cad-114">Atualiza o Endereço de Peering para a primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="b7cad-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="b7cad-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7cad-115">PARAMETERS</span></span>

### <span data-ttu-id="b7cad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cad-116">-DefaultProfile</span></span>
<span data-ttu-id="b7cad-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7cad-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cad-118">-InputObject</span></span>
<span data-ttu-id="b7cad-119">O objeto de conexão do Exchange</span><span class="sxs-lookup"><span data-stu-id="b7cad-119">The exchange connection object</span></span>

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

### <span data-ttu-id="b7cad-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b7cad-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b7cad-121">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="b7cad-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="b7cad-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b7cad-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b7cad-123">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="b7cad-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="b7cad-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b7cad-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b7cad-125">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="b7cad-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="b7cad-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b7cad-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="b7cad-127">O endereço IPv4 da sessão par</span><span class="sxs-lookup"><span data-stu-id="b7cad-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="b7cad-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b7cad-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="b7cad-129">O endereço IPv6 de sessão par</span><span class="sxs-lookup"><span data-stu-id="b7cad-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="b7cad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cad-130">CommonParameters</span></span>
<span data-ttu-id="b7cad-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cad-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7cad-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cad-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7cad-133">INPUTS</span></span>

### <span data-ttu-id="b7cad-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b7cad-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b7cad-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7cad-135">OUTPUTS</span></span>

### <span data-ttu-id="b7cad-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b7cad-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b7cad-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7cad-137">NOTES</span></span>

## <span data-ttu-id="b7cad-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7cad-138">RELATED LINKS</span></span>
