---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 2903b06d95a053b522203e9c590fe136e02ebf83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890156"
---
# <span data-ttu-id="0ffd4-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="0ffd4-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="0ffd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-102">SYNOPSIS</span></span>
<span data-ttu-id="0ffd4-103">Cria um PSObject na memória a ser usado para criar ou modificar um Peering.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="0ffd4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0ffd4-104">SYNTAX</span></span>

### <span data-ttu-id="0ffd4-105">IPv4PrefixIPv6Prefix (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0ffd4-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ffd4-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ffd4-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ffd4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0ffd4-107">DESCRIPTION</span></span>
<span data-ttu-id="0ffd4-108">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="0ffd4-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="0ffd4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-109">EXAMPLES</span></span>

### <span data-ttu-id="0ffd4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0ffd4-110">Example 1</span></span>
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

<span data-ttu-id="0ffd4-111">Nova conexão local</span><span class="sxs-lookup"><span data-stu-id="0ffd4-111">New local connection</span></span>

### <span data-ttu-id="0ffd4-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0ffd4-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="0ffd4-113">Criar conexão de paração direta com o uso para o serviço de paração habilitado e endereços IP fornecidos pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="0ffd4-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="0ffd4-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0ffd4-114">Example 3</span></span>
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

<span data-ttu-id="0ffd4-115">Criar conexão de paração direta com o uso para o serviço de peering habilitado e endereços IP fornecidos por pares</span><span class="sxs-lookup"><span data-stu-id="0ffd4-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="0ffd4-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0ffd4-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="0ffd4-117">Crie conexão de paração direta sem endereços IP de sessão bgp.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="0ffd4-118">O par terá que definir os endereços IP antes que a sessão bgp possa ser configurada.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="0ffd4-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-119">PARAMETERS</span></span>

### <span data-ttu-id="0ffd4-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="0ffd4-120">-BandwidthInMbps</span></span>
<span data-ttu-id="0ffd4-121">A Largura de Banda oferecida neste local em Mbps.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="0ffd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ffd4-122">-DefaultProfile</span></span>
<span data-ttu-id="0ffd4-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ffd4-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="0ffd4-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="0ffd4-125">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="0ffd4-125">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="0ffd4-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="0ffd4-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="0ffd4-127">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="0ffd4-127">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="0ffd4-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="0ffd4-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="0ffd4-129">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-129">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="0ffd4-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="0ffd4-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="0ffd4-131">Habilita o sinalizador que informa à Microsoft para fornecer os endereços de sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

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

### <span data-ttu-id="0ffd4-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="0ffd4-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="0ffd4-133">A ID do recurso de paração encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="0ffd4-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="0ffd4-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="0ffd4-134">-SessionPrefixV4</span></span>
<span data-ttu-id="0ffd4-135">O endereço IPv4 da sessão par</span><span class="sxs-lookup"><span data-stu-id="0ffd4-135">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="0ffd4-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="0ffd4-136">-SessionPrefixV6</span></span>
<span data-ttu-id="0ffd4-137">O endereço IPv6 de sessão par</span><span class="sxs-lookup"><span data-stu-id="0ffd4-137">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="0ffd4-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="0ffd4-138">-UseForPeeringService</span></span>
<span data-ttu-id="0ffd4-139">Habilitar para uso com o Microsoft Peering Service (MPS).</span><span class="sxs-lookup"><span data-stu-id="0ffd4-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="0ffd4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ffd4-140">CommonParameters</span></span>
<span data-ttu-id="0ffd4-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ffd4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ffd4-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ffd4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ffd4-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-143">INPUTS</span></span>

### <span data-ttu-id="0ffd4-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0ffd4-144">None</span></span>

## <span data-ttu-id="0ffd4-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-145">OUTPUTS</span></span>

### <span data-ttu-id="0ffd4-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="0ffd4-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="0ffd4-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="0ffd4-147">NOTES</span></span>

## <span data-ttu-id="0ffd4-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0ffd4-148">RELATED LINKS</span></span>
