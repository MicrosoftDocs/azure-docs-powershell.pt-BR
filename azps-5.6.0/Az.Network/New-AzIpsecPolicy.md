---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 059f94c8289b601d5a368266310e61d665e217fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892099"
---
# <span data-ttu-id="7cded-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7cded-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="7cded-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cded-102">SYNOPSIS</span></span>
<span data-ttu-id="7cded-103">Cria uma Política IPSec.</span><span class="sxs-lookup"><span data-stu-id="7cded-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="7cded-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7cded-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cded-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7cded-105">DESCRIPTION</span></span>
<span data-ttu-id="7cded-106">O New-AzIpsecPolicy cmdlet cria uma proposta de política IPSec a ser usada em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7cded-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="7cded-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7cded-107">EXAMPLES</span></span>

### <span data-ttu-id="7cded-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7cded-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="7cded-109">Criar uma política IPSec a ser usada para uma nova conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="7cded-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="7cded-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7cded-110">PARAMETERS</span></span>

### <span data-ttu-id="7cded-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cded-111">-DefaultProfile</span></span>
<span data-ttu-id="7cded-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7cded-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cded-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="7cded-113">-DhGroup</span></span>
<span data-ttu-id="7cded-114">Os grupos DH usados na Fase 1 do IKE para SA inicial</span><span class="sxs-lookup"><span data-stu-id="7cded-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DHGroup1, DHGroup14, DHGroup2, DHGroup2048, DHGroup24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="7cded-115">-IkeEncryption</span></span>
<span data-ttu-id="7cded-116">O algoritmo de criptografia IKE (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="7cded-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DES, DES3, AES128, AES192, AES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="7cded-117">-IkeIntegrity</span></span>
<span data-ttu-id="7cded-118">O algoritmo de integridade IKE (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="7cded-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, SHA384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="7cded-119">-IpsecEncryption</span></span>
<span data-ttu-id="7cded-120">O algoritmo de criptografia IPSec (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="7cded-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, DES, DES3, AES128, AES192, AES256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="7cded-121">-IpsecIntegrity</span></span>
<span data-ttu-id="7cded-122">O algoritmo de integridade IPSec (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="7cded-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MD5, SHA1, SHA256, GCMAES128, GCMAES192, GCMAES256

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="7cded-123">-PfsGroup</span></span>
<span data-ttu-id="7cded-124">Os Grupos de DH usados na Fase 2 do IKE para o NOVO SA filho</span><span class="sxs-lookup"><span data-stu-id="7cded-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, PFS1, PFS2, PFS2048, PFS24, ECP256, ECP384

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="7cded-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="7cded-126">O tamanho da carga da Associação de Segurança IPSec (também chamada de Modo Rápido ou Fase 2 SA) no KB</span><span class="sxs-lookup"><span data-stu-id="7cded-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="7cded-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="7cded-128">A vida útil da Associação de Segurança IPSec (também chamada de Modo Rápido ou Fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="7cded-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cded-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cded-129">CommonParameters</span></span>
<span data-ttu-id="7cded-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cded-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cded-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cded-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cded-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7cded-132">INPUTS</span></span>

### <span data-ttu-id="7cded-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7cded-133">None</span></span>

## <span data-ttu-id="7cded-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7cded-134">OUTPUTS</span></span>

### <span data-ttu-id="7cded-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="7cded-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="7cded-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="7cded-136">NOTES</span></span>

## <span data-ttu-id="7cded-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cded-137">RELATED LINKS</span></span>
