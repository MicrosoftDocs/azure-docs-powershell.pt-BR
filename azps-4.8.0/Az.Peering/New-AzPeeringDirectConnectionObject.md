---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112938"
---
# <span data-ttu-id="2f4e5-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2f4e5-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="2f4e5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f4e5-103">Cria um PSObject na memória a ser usado para criar ou modificar um emparelhamento.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="2f4e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f4e5-104">SYNTAX</span></span>

### <span data-ttu-id="2f4e5-105">IPv4PrefixIPv6Prefix (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f4e5-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f4e5-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2f4e5-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f4e5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f4e5-107">DESCRIPTION</span></span>
<span data-ttu-id="2f4e5-108">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="2f4e5-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="2f4e5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f4e5-109">EXAMPLES</span></span>

### <span data-ttu-id="2f4e5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f4e5-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2f4e5-111">Nova conexão local</span><span class="sxs-lookup"><span data-stu-id="2f4e5-111">New local connection</span></span>

### <span data-ttu-id="2f4e5-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2f4e5-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="2f4e5-113">Criar conexão de emparelhamento direto com o uso para o serviço de emparelhamento habilitado e endereços IP fornecidos pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="2f4e5-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="2f4e5-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2f4e5-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2f4e5-115">Criar conexão de emparelhamento direto com o uso para o serviço de emparelhamento habilitado e endereços IP de par fornecido</span><span class="sxs-lookup"><span data-stu-id="2f4e5-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="2f4e5-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="2f4e5-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="2f4e5-117">Criar conexão de emparelhamento direto sem endereços IP da sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="2f4e5-118">O par precisará definir os endereços IP antes que a sessão do BGP possa ser configurada.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="2f4e5-119">OS</span><span class="sxs-lookup"><span data-stu-id="2f4e5-119">PARAMETERS</span></span>

### <span data-ttu-id="2f4e5-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2f4e5-120">-BandwidthInMbps</span></span>
<span data-ttu-id="2f4e5-121">A largura de banda oferecida neste local em Mbps.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f4e5-122">-DefaultProfile</span></span>
<span data-ttu-id="2f4e5-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f4e5-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="2f4e5-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="2f4e5-125">O valor máximo de IPv4 anunciado</span><span class="sxs-lookup"><span data-stu-id="2f4e5-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="2f4e5-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="2f4e5-127">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="2f4e5-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="2f4e5-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="2f4e5-129">A chave de autenticação MD5 para a sessão.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2f4e5-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="2f4e5-131">Habilite o sinalizador que informa à Microsoft para fornecer os endereços da sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="2f4e5-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="2f4e5-133">A ID de recursos de emparelhamento encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="2f4e5-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="2f4e5-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="2f4e5-134">-SessionPrefixV4</span></span>
<span data-ttu-id="2f4e5-135">O endereço IPv4 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="2f4e5-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="2f4e5-136">-SessionPrefixV6</span></span>
<span data-ttu-id="2f4e5-137">O endereço IPv6 da sessão de par</span><span class="sxs-lookup"><span data-stu-id="2f4e5-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2f4e5-138">-UseForPeeringService</span></span>
<span data-ttu-id="2f4e5-139">Habilite para uso com o serviço de emparelhamento da Microsoft (MPS).</span><span class="sxs-lookup"><span data-stu-id="2f4e5-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f4e5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f4e5-140">CommonParameters</span></span>
<span data-ttu-id="2f4e5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f4e5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f4e5-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f4e5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f4e5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f4e5-143">INPUTS</span></span>

### <span data-ttu-id="2f4e5-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2f4e5-144">None</span></span>

## <span data-ttu-id="2f4e5-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f4e5-145">OUTPUTS</span></span>

### <span data-ttu-id="2f4e5-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="2f4e5-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="2f4e5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f4e5-147">NOTES</span></span>

## <span data-ttu-id="2f4e5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f4e5-148">RELATED LINKS</span></span>
