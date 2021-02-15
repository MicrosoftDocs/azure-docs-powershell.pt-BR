---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112725"
---
# <span data-ttu-id="fceca-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fceca-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="fceca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fceca-102">SYNOPSIS</span></span>
<span data-ttu-id="fceca-103">Cria um PSObject na memória a ser usado para criar ou modificar um Peering.</span><span class="sxs-lookup"><span data-stu-id="fceca-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="fceca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fceca-104">SYNTAX</span></span>

### <span data-ttu-id="fceca-105">IPv4PrefixIPv6Prefix (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fceca-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fceca-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="fceca-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fceca-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="fceca-107">DESCRIPTION</span></span>
<span data-ttu-id="fceca-108">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="fceca-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="fceca-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fceca-109">EXAMPLES</span></span>

### <span data-ttu-id="fceca-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fceca-110">Example 1</span></span>
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

<span data-ttu-id="fceca-111">Nova conexão local</span><span class="sxs-lookup"><span data-stu-id="fceca-111">New local connection</span></span>

### <span data-ttu-id="fceca-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fceca-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="fceca-113">Criar conexão de paridade direta com o uso para o serviço de peering habilitado e endereços IP fornecidos pela Microsoft</span><span class="sxs-lookup"><span data-stu-id="fceca-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="fceca-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fceca-114">Example 3</span></span>
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

<span data-ttu-id="fceca-115">Criar conexão de peering direto com o uso para endereços IP habilitados para serviço de par e fornecidos por pares</span><span class="sxs-lookup"><span data-stu-id="fceca-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="fceca-116">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fceca-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="fceca-117">Crie uma conexão de paridade direta sem endereços IP de sessão bgp.</span><span class="sxs-lookup"><span data-stu-id="fceca-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="fceca-118">O ponto terá que definir os endereços IP antes que a sessão bgp possa ser configurada.</span><span class="sxs-lookup"><span data-stu-id="fceca-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="fceca-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fceca-119">PARAMETERS</span></span>

### <span data-ttu-id="fceca-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="fceca-120">-BandwidthInMbps</span></span>
<span data-ttu-id="fceca-121">A largura de banda oferecida neste local em Mbps.</span><span class="sxs-lookup"><span data-stu-id="fceca-121">The Bandwidth offered at this location in Mbps.</span></span>

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

### <span data-ttu-id="fceca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fceca-122">-DefaultProfile</span></span>
<span data-ttu-id="fceca-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fceca-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fceca-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="fceca-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="fceca-125">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="fceca-125">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="fceca-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="fceca-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="fceca-127">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="fceca-127">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="fceca-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="fceca-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="fceca-129">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="fceca-129">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="fceca-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="fceca-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="fceca-131">Habilita o sinalizador que informa à Microsoft para fornecer os endereços de sessão BGP.</span><span class="sxs-lookup"><span data-stu-id="fceca-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

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

### <span data-ttu-id="fceca-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="fceca-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="fceca-133">A ID da instalação de paração encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="fceca-133">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="fceca-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="fceca-134">-SessionPrefixV4</span></span>
<span data-ttu-id="fceca-135">O endereço IPv4 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="fceca-135">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="fceca-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="fceca-136">-SessionPrefixV6</span></span>
<span data-ttu-id="fceca-137">O endereço IPv6 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="fceca-137">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="fceca-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="fceca-138">-UseForPeeringService</span></span>
<span data-ttu-id="fceca-139">Habilitar para uso com o Serviço de Peering (MPS) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fceca-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

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

### <span data-ttu-id="fceca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fceca-140">CommonParameters</span></span>
<span data-ttu-id="fceca-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fceca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fceca-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fceca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fceca-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="fceca-143">INPUTS</span></span>

### <span data-ttu-id="fceca-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fceca-144">None</span></span>

## <span data-ttu-id="fceca-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="fceca-145">OUTPUTS</span></span>

### <span data-ttu-id="fceca-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="fceca-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="fceca-147">Notas</span><span class="sxs-lookup"><span data-stu-id="fceca-147">NOTES</span></span>

## <span data-ttu-id="fceca-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fceca-148">RELATED LINKS</span></span>
