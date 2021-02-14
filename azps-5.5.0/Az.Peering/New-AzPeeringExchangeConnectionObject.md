---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117285"
---
# <span data-ttu-id="a6f57-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="a6f57-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="a6f57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6f57-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f57-103">Cria um PSObject na memória a ser usado para criar ou modificar um Peering.</span><span class="sxs-lookup"><span data-stu-id="a6f57-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="a6f57-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6f57-104">SYNTAX</span></span>

### <span data-ttu-id="a6f57-105">IPv4Address (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6f57-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6f57-106">Endereço_ipv6</span><span class="sxs-lookup"><span data-stu-id="a6f57-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6f57-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="a6f57-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6f57-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6f57-108">DESCRIPTION</span></span>
<span data-ttu-id="a6f57-109">Cria um PSObject na memória</span><span class="sxs-lookup"><span data-stu-id="a6f57-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="a6f57-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6f57-110">EXAMPLES</span></span>

### <span data-ttu-id="a6f57-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6f57-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="a6f57-112">Objeto de conexão local</span><span class="sxs-lookup"><span data-stu-id="a6f57-112">Local connection object</span></span>

## <span data-ttu-id="a6f57-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6f57-113">PARAMETERS</span></span>

### <span data-ttu-id="a6f57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f57-114">-DefaultProfile</span></span>
<span data-ttu-id="a6f57-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6f57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6f57-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="a6f57-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="a6f57-117">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="a6f57-117">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="a6f57-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="a6f57-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="a6f57-119">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="a6f57-119">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="a6f57-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="a6f57-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="a6f57-121">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="a6f57-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="a6f57-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="a6f57-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="a6f57-123">A ID da instalação de paração encontrada em https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="a6f57-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="a6f57-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="a6f57-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="a6f57-125">O endereço IPv4 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="a6f57-125">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="a6f57-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="a6f57-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="a6f57-127">O endereço IPv6 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="a6f57-127">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="a6f57-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f57-128">CommonParameters</span></span>
<span data-ttu-id="a6f57-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f57-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f57-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6f57-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f57-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="a6f57-131">INPUTS</span></span>

### <span data-ttu-id="a6f57-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a6f57-132">None</span></span>

## <span data-ttu-id="a6f57-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="a6f57-133">OUTPUTS</span></span>

### <span data-ttu-id="a6f57-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="a6f57-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="a6f57-135">Notas</span><span class="sxs-lookup"><span data-stu-id="a6f57-135">NOTES</span></span>

## <span data-ttu-id="a6f57-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6f57-136">RELATED LINKS</span></span>
