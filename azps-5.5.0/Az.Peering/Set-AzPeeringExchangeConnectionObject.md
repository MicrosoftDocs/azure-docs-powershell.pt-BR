---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114060"
---
# <span data-ttu-id="199e7-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="199e7-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="199e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="199e7-102">SYNOPSIS</span></span>
<span data-ttu-id="199e7-103">Define ou atualiza as informações de Conexão do Exchange.</span><span class="sxs-lookup"><span data-stu-id="199e7-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="199e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="199e7-104">SYNTAX</span></span>

### <span data-ttu-id="199e7-105">IPv4Address (Padrão)</span><span class="sxs-lookup"><span data-stu-id="199e7-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199e7-106">Endereço_ipv6</span><span class="sxs-lookup"><span data-stu-id="199e7-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="199e7-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="199e7-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="199e7-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="199e7-108">DESCRIPTION</span></span>
<span data-ttu-id="199e7-109">Usado em conjunto com o Update-AzPeering, esta é uma operação de memória e persistirá apenas `Update-AzPeering` com.</span><span class="sxs-lookup"><span data-stu-id="199e7-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="199e7-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="199e7-110">EXAMPLES</span></span>

### <span data-ttu-id="199e7-111">Atualizar Hash Md5</span><span class="sxs-lookup"><span data-stu-id="199e7-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="199e7-112">Atualiza o Hash Md5 para a primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="199e7-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="199e7-113">Atualizar Endereço de Sessão Bgp</span><span class="sxs-lookup"><span data-stu-id="199e7-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="199e7-114">Atualiza o Endereço de Parimento para a primeira conexão no objeto Peering na memória.</span><span class="sxs-lookup"><span data-stu-id="199e7-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="199e7-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="199e7-115">PARAMETERS</span></span>

### <span data-ttu-id="199e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199e7-116">-DefaultProfile</span></span>
<span data-ttu-id="199e7-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="199e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="199e7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="199e7-118">-InputObject</span></span>
<span data-ttu-id="199e7-119">O objeto de conexão do Exchange</span><span class="sxs-lookup"><span data-stu-id="199e7-119">The exchange connection object</span></span>

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

### <span data-ttu-id="199e7-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="199e7-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="199e7-121">O IPv4 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="199e7-121">The maximum advertised IPv4</span></span>

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

### <span data-ttu-id="199e7-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="199e7-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="199e7-123">O IPv6 máximo anunciado</span><span class="sxs-lookup"><span data-stu-id="199e7-123">The maximum advertised IPv6</span></span>

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

### <span data-ttu-id="199e7-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="199e7-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="199e7-125">A chave de autenticação MD5 para sessão.</span><span class="sxs-lookup"><span data-stu-id="199e7-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="199e7-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="199e7-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="199e7-127">O endereço IPv4 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="199e7-127">The peer session IPv4 address</span></span>

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

### <span data-ttu-id="199e7-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="199e7-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="199e7-129">O endereço IPv6 da sessão de pares</span><span class="sxs-lookup"><span data-stu-id="199e7-129">The peer session IPv6 address</span></span>

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

### <span data-ttu-id="199e7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199e7-130">CommonParameters</span></span>
<span data-ttu-id="199e7-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="199e7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199e7-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="199e7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199e7-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="199e7-133">INPUTS</span></span>

### <span data-ttu-id="199e7-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="199e7-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="199e7-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="199e7-135">OUTPUTS</span></span>

### <span data-ttu-id="199e7-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="199e7-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="199e7-137">Notas</span><span class="sxs-lookup"><span data-stu-id="199e7-137">NOTES</span></span>

## <span data-ttu-id="199e7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="199e7-138">RELATED LINKS</span></span>
