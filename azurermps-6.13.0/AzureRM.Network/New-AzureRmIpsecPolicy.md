---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmIpsecPolicy.md
ms.openlocfilehash: 1b68b8ac6e480c93a9158d77a635c497fe9d1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433206"
---
# <span data-ttu-id="bed83-101">New-AzureRmIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bed83-101">New-AzureRmIpsecPolicy</span></span>

## <span data-ttu-id="bed83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bed83-102">SYNOPSIS</span></span>
<span data-ttu-id="bed83-103">Cria uma política IPSec.</span><span class="sxs-lookup"><span data-stu-id="bed83-103">Creates an IPSec Policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bed83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bed83-104">SYNTAX</span></span>

```
New-AzureRmIpsecPolicy [-SALifeTimeSeconds <Int32>] [-SADataSizeKilobytes <Int32>] -IpsecEncryption <String>
 -IpsecIntegrity <String> -IkeEncryption <String> -IkeIntegrity <String> -DhGroup <String> -PfsGroup <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bed83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bed83-105">DESCRIPTION</span></span>
<span data-ttu-id="bed83-106">O cmdlet New-AzureRmIpsecPolicy cria uma proposta de política IPSec para ser usada em uma conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bed83-106">The New-AzureRmIpsecPolicy cmdlet creates an IPSec policy proposal to be used in a virtual network gateway connection.</span></span>

## <span data-ttu-id="bed83-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bed83-107">EXAMPLES</span></span>

### <span data-ttu-id="bed83-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bed83-108">Example 1</span></span>
```
PS C:\> $ipsecPolicy = New-AzureRmIpsecPolicy -SALifeTimeSeconds 1000 -SADataSizeKilobytes 2000 -IpsecEncryption "GCMAES256" -IpsecIntegrity "GCMAES256" -IkeEncryption "AES256" -IkeIntegrity "SHA256" -DhGroup "DHGroup14" -PfsGroup "PFS2048"
PS C:\> New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName $rgname -name $vnetConnectionName -location $location -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -RoutingWeight 3 -SharedKey $sharedKey -UsePolicyBasedTrafficSelectors $true -IpsecPolicies $ipsecPolicy
```

<span data-ttu-id="bed83-109">Criar uma diretiva IPSec para ser usada para uma nova conexão de gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bed83-109">Creating an IPSec policy to be used for a new virtual network gateway connection.</span></span>

## <span data-ttu-id="bed83-110">OS</span><span class="sxs-lookup"><span data-stu-id="bed83-110">PARAMETERS</span></span>

### <span data-ttu-id="bed83-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bed83-111">-DefaultProfile</span></span>
<span data-ttu-id="bed83-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bed83-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bed83-113">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="bed83-113">-DhGroup</span></span>
<span data-ttu-id="bed83-114">Os grupos DH usados na fase 1 da IKE para SA inicial</span><span class="sxs-lookup"><span data-stu-id="bed83-114">The DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="bed83-115">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="bed83-115">-IkeEncryption</span></span>
<span data-ttu-id="bed83-116">O algoritmo de criptografia IKE (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="bed83-116">The IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bed83-117">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="bed83-117">-IkeIntegrity</span></span>
<span data-ttu-id="bed83-118">O algoritmo de integridade de IKE (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="bed83-118">The IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="bed83-119">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="bed83-119">-IpsecEncryption</span></span>
<span data-ttu-id="bed83-120">O algoritmo de criptografia IPSec (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="bed83-120">The IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bed83-121">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="bed83-121">-IpsecIntegrity</span></span>
<span data-ttu-id="bed83-122">O algoritmo de integridade IPSec (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="bed83-122">The IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="bed83-123">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="bed83-123">-PfsGroup</span></span>
<span data-ttu-id="bed83-124">Os grupos DH usados na fase 2 do IKE para novas associações de senha filho</span><span class="sxs-lookup"><span data-stu-id="bed83-124">The DH Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="bed83-125">-SADataSizeKilobytes</span><span class="sxs-lookup"><span data-stu-id="bed83-125">-SADataSizeKilobytes</span></span>
<span data-ttu-id="bed83-126">O tamanho da carga de segurança IPSec (também chamado de modo rápido ou da fase 2 SA) em KB</span><span class="sxs-lookup"><span data-stu-id="bed83-126">The IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="bed83-127">-SALifeTimeSeconds</span><span class="sxs-lookup"><span data-stu-id="bed83-127">-SALifeTimeSeconds</span></span>
<span data-ttu-id="bed83-128">O tempo de vida da Associação de segurança IPSec (também chamado de modo rápido ou da fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="bed83-128">The IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="bed83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bed83-129">CommonParameters</span></span>
<span data-ttu-id="bed83-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bed83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bed83-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bed83-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bed83-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bed83-132">INPUTS</span></span>

### <span data-ttu-id="bed83-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bed83-133">None</span></span>

## <span data-ttu-id="bed83-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bed83-134">OUTPUTS</span></span>

### <span data-ttu-id="bed83-135">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="bed83-135">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="bed83-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bed83-136">NOTES</span></span>

## <span data-ttu-id="bed83-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bed83-137">RELATED LINKS</span></span>
