---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 6966ff42fad202bfec62048a56ac6b49398a4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890126"
---
# <span data-ttu-id="8231c-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8231c-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="8231c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8231c-102">SYNOPSIS</span></span>
<span data-ttu-id="8231c-103">Define ou atualiza as informações de Conexão Direta.</span><span class="sxs-lookup"><span data-stu-id="8231c-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="8231c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8231c-104">SYNTAX</span></span>

### <span data-ttu-id="8231c-105">Largura de banda (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8231c-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8231c-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="8231c-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8231c-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="8231c-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8231c-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="8231c-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8231c-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="8231c-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8231c-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8231c-110">DESCRIPTION</span></span>
<span data-ttu-id="8231c-111">Usada em conjunto com Update-AzPeering, esta é uma operação na memória e só persistirá com `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="8231c-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="8231c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8231c-112">EXAMPLES</span></span>

### <span data-ttu-id="8231c-113">Atualizar Largura de Banda</span><span class="sxs-lookup"><span data-stu-id="8231c-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="8231c-114">Atualiza a largura de banda da primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="8231c-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="8231c-115">Atualizar Endereço de Sessão Bgp</span><span class="sxs-lookup"><span data-stu-id="8231c-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="8231c-116">Atualiza o Endereço de Peering para a primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="8231c-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="8231c-117">Atualizar Uso para o serviço de par</span><span class="sxs-lookup"><span data-stu-id="8231c-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="8231c-118">Atualiza a conexão para uso com o serviço de peering</span><span class="sxs-lookup"><span data-stu-id="8231c-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="8231c-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8231c-119">PARAMETERS</span></span>

### <span data-ttu-id="8231c-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="8231c-120">-BandwidthInMbps</span></span>
<span data-ttu-id="8231c-121">A Largura de Banda oferecida neste local em Mbps.</span><span class="sxs-lookup"><span data-stu-id="8231c-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="8231c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8231c-122">-DefaultProfile</span></span>
<span data-ttu-id="8231c-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8231c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8231c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8231c-124">-InputObject</span></span>
<span data-ttu-id="8231c-125">O objeto de conexão direta</span><span class="sxs-lookup"><span data-stu-id="8231c-125">The direct connection Object</span></span>

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

### <span data-ttu-id="8231c-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="8231c-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="8231c-127">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="8231c-127">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="8231c-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="8231c-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="8231c-129">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="8231c-129">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="8231c-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="8231c-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="8231c-131">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="8231c-131">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="8231c-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="8231c-132">-SessionPrefixV4</span></span>
<span data-ttu-id="8231c-133">O endereço IPv4 da sessão par</span><span class="sxs-lookup"><span data-stu-id="8231c-133">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="8231c-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="8231c-134">-SessionPrefixV6</span></span>
<span data-ttu-id="8231c-135">O endereço IPv6 de sessão par</span><span class="sxs-lookup"><span data-stu-id="8231c-135">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="8231c-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="8231c-136">-UseForPeeringService</span></span>
<span data-ttu-id="8231c-137">Habilitar para uso com o Microsoft Peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="8231c-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="8231c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8231c-138">CommonParameters</span></span>
<span data-ttu-id="8231c-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8231c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8231c-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8231c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8231c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8231c-141">INPUTS</span></span>

### <span data-ttu-id="8231c-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="8231c-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="8231c-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8231c-143">OUTPUTS</span></span>

### <span data-ttu-id="8231c-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="8231c-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="8231c-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="8231c-145">NOTES</span></span>

## <span data-ttu-id="8231c-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8231c-146">RELATED LINKS</span></span>
