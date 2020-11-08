---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpsecPolicy.md
ms.openlocfilehash: 5a6cbbc007c372d2e1765e4e2369d2f3d60d0a07
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117271"
---
# <span data-ttu-id="461e3-101">New-AzIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="461e3-101">New-AzIpsecPolicy</span></span>

## <span data-ttu-id="461e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="461e3-102">SYNOPSIS</span></span>
<span data-ttu-id="461e3-103">Cria uma política IPSec.</span><span class="sxs-lookup"><span data-stu-id="461e3-103">Creates an IPSec Policy.</span></span>

## <span data-ttu-id="461e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="461e3-104">SYNTAX</span></span>

```
New-AzIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="461e3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="461e3-105">DESCRIPTION</span></span>
<span data-ttu-id="461e3-106">O cmdlet New-AzIpsecPolicy cria uma proposta de política IPSec para ser usada em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="461e3-106">The New-AzIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="461e3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="461e3-107">EXAMPLES</span></span>

### <span data-ttu-id="461e3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="461e3-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="461e3-109">Criar uma diretiva IPSec para ser usada para uma nova conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="461e3-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="461e3-110">OS</span><span class="sxs-lookup"><span data-stu-id="461e3-110">PARAMETERS</span></span>

### <span data-ttu-id="461e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="461e3-111">-DefaultProfile</span></span>
<span data-ttu-id="461e3-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="461e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="461e3-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="461e3-113">-DhGroup</span></span>
<span data-ttu-id="461e3-114">Os grupos DH usados na fase 1 da IKE para SA inicial</span><span class="sxs-lookup"><span data-stu-id="461e3-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="461e3-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="461e3-115">-IkeEncryption</span></span>
<span data-ttu-id="461e3-116">O algoritmo de criptografia IKE (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="461e3-116">The IKE encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="461e3-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="461e3-117">-IkeIntegrity</span></span>
<span data-ttu-id="461e3-118">O algoritmo de integridade IKE (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="461e3-118">The IKE integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="461e3-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="461e3-119">-IpsecEncryption</span></span>
<span data-ttu-id="461e3-120">O algoritmo de criptografia IPSec (fase 2 de IKE)</span><span class="sxs-lookup"><span data-stu-id="461e3-120">The IPSec encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="461e3-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="461e3-121">-IpsecIntegrity</span></span>
<span data-ttu-id="461e3-122">O algoritmo de integridade IPSec (fase 2 de IKE)</span><span class="sxs-lookup"><span data-stu-id="461e3-122">The IPSec integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="461e3-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="461e3-123">-PfsGroup</span></span>
<span data-ttu-id="461e3-124">Os grupos DH usados na fase 2 do IKE para novas associações de senha filho</span><span class="sxs-lookup"><span data-stu-id="461e3-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="461e3-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="461e3-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="461e3-126">O tamanho da carga de segurança IPSec (também chamado de modo rápido ou da fase 2 SA) em KB</span><span class="sxs-lookup"><span data-stu-id="461e3-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="461e3-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="461e3-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="461e3-128">O tempo de vida da Associação de segurança IPSec (também chamado de modo rápido ou da fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="461e3-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="461e3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="461e3-129">CommonParameters</span></span>
<span data-ttu-id="461e3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="461e3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="461e3-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="461e3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="461e3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="461e3-132">INPUTS</span></span>

### <span data-ttu-id="461e3-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="461e3-133">None</span></span>

## <span data-ttu-id="461e3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="461e3-134">OUTPUTS</span></span>

### <span data-ttu-id="461e3-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="461e3-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="461e3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="461e3-136">NOTES</span></span>

## <span data-ttu-id="461e3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="461e3-137">RELATED LINKS</span></span>
