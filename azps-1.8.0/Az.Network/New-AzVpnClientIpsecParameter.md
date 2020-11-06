---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: e547389518bce61c3c3654011bdc0107dc5a112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600247"
---
# <span data-ttu-id="fc9d4-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc9d4-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="fc9d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc9d4-103">Esse comando permite que os usuários criem o objeto de parâmetros IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="fc9d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc9d4-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc9d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc9d4-106">Esse comando permite que os usuários criem o objeto de parâmetros IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="fc9d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc9d4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc9d4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc9d4-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="fc9d4-109">New-AzVpnClientIpsecParameter cmdlet é usado para criar o objeto de parâmetros de IPSec VPN do uso dos valores passados um ou todos os parâmetros que o usuário pode definir para qualquer gateway de rede virtual existente no grupo de Resource.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="fc9d4-110">Esse objeto VpnClientIPsecParameters criado é passado para o comando Set-AzVpnClientIpsecParameter para definir a política personalizada IPSec IPSec especificada no gateway de rede virtual, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="fc9d4-111">Esse comando retorna o objeto do VpnClientIPsecParameters que mostra Set Parameters.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="fc9d4-112">OS</span><span class="sxs-lookup"><span data-stu-id="fc9d4-112">PARAMETERS</span></span>

### <span data-ttu-id="fc9d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc9d4-113">-DefaultProfile</span></span>
<span data-ttu-id="fc9d4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc9d4-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="fc9d4-115">-DhGroup</span></span>
<span data-ttu-id="fc9d4-116">Os grupos DH do vpnclient usados na fase 1 do IKE para SA inicial.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="fc9d4-117">-IkeEncryption</span></span>
<span data-ttu-id="fc9d4-118">O algoritmo de criptografia IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="fc9d4-119">-IkeIntegrity</span></span>
<span data-ttu-id="fc9d4-120">O algoritmo de integridade IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="fc9d4-121">-IpsecEncryption</span></span>
<span data-ttu-id="fc9d4-122">O algoritmo de criptografia IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="fc9d4-123">-IpsecIntegrity</span></span>
<span data-ttu-id="fc9d4-124">O algoritmo de integridade IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="fc9d4-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="fc9d4-125">-PfsGroup</span></span>
<span data-ttu-id="fc9d4-126">Os grupos de PFS do vpnclient usados na fase 2 do IKE para novas associações de SA filho</span><span class="sxs-lookup"><span data-stu-id="fc9d4-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc9d4-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="fc9d4-127">-SADataSize</span></span>
<span data-ttu-id="fc9d4-128">O tamanho da carga de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 do SA) em KB</span><span class="sxs-lookup"><span data-stu-id="fc9d4-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="fc9d4-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="fc9d4-129">-SALifeTime</span></span>
<span data-ttu-id="fc9d4-130">O tempo de vida da Associação de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="fc9d4-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="fc9d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc9d4-131">CommonParameters</span></span>
<span data-ttu-id="fc9d4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc9d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc9d4-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc9d4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc9d4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc9d4-134">INPUTS</span></span>

### <span data-ttu-id="fc9d4-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fc9d4-135">None</span></span>

## <span data-ttu-id="fc9d4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc9d4-136">OUTPUTS</span></span>

### <span data-ttu-id="fc9d4-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="fc9d4-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="fc9d4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc9d4-138">NOTES</span></span>

## <span data-ttu-id="fc9d4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc9d4-139">RELATED LINKS</span></span>

[<span data-ttu-id="fc9d4-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc9d4-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fc9d4-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc9d4-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="fc9d4-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="fc9d4-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
