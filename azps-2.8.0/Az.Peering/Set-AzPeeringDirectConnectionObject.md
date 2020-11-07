---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: ca9235ddfb4b16b80cd0df9ad61bd6936672b889
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772838"
---
# <span data-ttu-id="6a9a6-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="6a9a6-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="6a9a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9a6-103">Define ou atualiza as informações de conexão direta.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="6a9a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a9a6-104">SYNTAX</span></span>

### <span data-ttu-id="6a9a6-105">Largura de banda (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a9a6-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a6-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="6a9a6-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a6-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="6a9a6-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a6-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="6a9a6-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9a6-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="6a9a6-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9a6-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a9a6-110">DESCRIPTION</span></span>
<span data-ttu-id="6a9a6-111">Usado em conjunto com Update-AzPeering, essa é uma operação de memória em memória e só será persistente `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="6a9a6-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="6a9a6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a9a6-112">EXAMPLES</span></span>

### <span data-ttu-id="6a9a6-113">Atualizar largura de banda</span><span class="sxs-lookup"><span data-stu-id="6a9a6-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="6a9a6-114">Atualiza a largura de banda da primeira conexão no objeto de emparelhamento na memória.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="6a9a6-115">Atualizar o endereço da sessão do BGP</span><span class="sxs-lookup"><span data-stu-id="6a9a6-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="6a9a6-116">Atualiza o endereço de emparelhamento da primeira conexão no objeto de emparelhamento na memória.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="6a9a6-117">Usar atualização para serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="6a9a6-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="6a9a6-118">Atualiza a conexão para uso com o serviço de emparelhamento</span><span class="sxs-lookup"><span data-stu-id="6a9a6-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="6a9a6-119">OS</span><span class="sxs-lookup"><span data-stu-id="6a9a6-119">PARAMETERS</span></span>

### <span data-ttu-id="6a9a6-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="6a9a6-120">-BandwidthInMbps</span></span>
<span data-ttu-id="6a9a6-121">A largura de banda oferecida neste local em Mbps.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9a6-122">-DefaultProfile</span></span>
<span data-ttu-id="6a9a6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9a6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a9a6-124">-InputObject</span></span>
<span data-ttu-id="6a9a6-125">O objeto conexão direta</span><span class="sxs-lookup"><span data-stu-id="6a9a6-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="6a9a6-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="6a9a6-127">O valor máximo de IPv4 anunciado</span><span class="sxs-lookup"><span data-stu-id="6a9a6-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="6a9a6-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="6a9a6-129">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="6a9a6-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="6a9a6-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="6a9a6-131">A chave de autenticação MD5 para a sessão.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="6a9a6-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="6a9a6-132">-SessionPrefixV4</span></span>
<span data-ttu-id="6a9a6-133">O endereço IPv4 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="6a9a6-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="6a9a6-134">-SessionPrefixV6</span></span>
<span data-ttu-id="6a9a6-135">O endereço IPv6 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="6a9a6-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="6a9a6-136">-UseForPeeringService</span></span>
<span data-ttu-id="6a9a6-137">Habilite para uso com o serviço de emparelhamento da Microsoft (MPS).</span><span class="sxs-lookup"><span data-stu-id="6a9a6-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9a6-138">CommonParameters</span></span>
<span data-ttu-id="6a9a6-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9a6-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a9a6-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9a6-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a9a6-141">INPUTS</span></span>

### <span data-ttu-id="6a9a6-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="6a9a6-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="6a9a6-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a9a6-143">OUTPUTS</span></span>

### <span data-ttu-id="6a9a6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="6a9a6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="6a9a6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a9a6-145">NOTES</span></span>

## <span data-ttu-id="6a9a6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a9a6-146">RELATED LINKS</span></span>