---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 89106b6474e52863514c65614d334cf5d8382f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610867"
---
# <span data-ttu-id="a1833-101">New-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="a1833-101">New-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="a1833-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1833-102">SYNOPSIS</span></span>
<span data-ttu-id="a1833-103">Esse comando permite que os usuários criem o objeto de parâmetros IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="a1833-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1833-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1833-104">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1833-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1833-105">DESCRIPTION</span></span>
<span data-ttu-id="a1833-106">Esse comando permite que os usuários criem o objeto de parâmetros IPSec VPN especificando um ou todos os valores, como IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="a1833-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="a1833-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1833-107">EXAMPLES</span></span>

### <span data-ttu-id="a1833-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1833-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="a1833-109">New-AzureRmVpnClientIpsecParameter cmdlet é usado para criar o objeto de parâmetros de IPSec VPN do uso dos valores passados um ou todos os parâmetros que o usuário pode definir para qualquer gateway de rede virtual existente no grupo de Resource.</span><span class="sxs-lookup"><span data-stu-id="a1833-109">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="a1833-110">Esse objeto VpnClientIPsecParameters criado é passado para o comando Set-AzureRmVpnClientIpsecParameter para definir a política personalizada IPSec IPSec especificada no gateway de rede virtual, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="a1833-110">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="a1833-111">Esse comando retorna o objeto do VpnClientIPsecParameters que mostra Set Parameters.</span><span class="sxs-lookup"><span data-stu-id="a1833-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="a1833-112">OS</span><span class="sxs-lookup"><span data-stu-id="a1833-112">PARAMETERS</span></span>

### <span data-ttu-id="a1833-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1833-113">-DefaultProfile</span></span>
<span data-ttu-id="a1833-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1833-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1833-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="a1833-115">-DhGroup</span></span>
<span data-ttu-id="a1833-116">Os grupos DH do vpnclient usados na fase 1 do IKE para SA inicial.</span><span class="sxs-lookup"><span data-stu-id="a1833-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="a1833-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="a1833-117">-IkeEncryption</span></span>
<span data-ttu-id="a1833-118">O algoritmo de criptografia IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="a1833-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="a1833-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="a1833-119">-IkeIntegrity</span></span>
<span data-ttu-id="a1833-120">O algoritmo de integridade IKE do vpnclient (fase 2 da IKE)</span><span class="sxs-lookup"><span data-stu-id="a1833-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="a1833-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="a1833-121">-IpsecEncryption</span></span>
<span data-ttu-id="a1833-122">O algoritmo de criptografia IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="a1833-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="a1833-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="a1833-123">-IpsecIntegrity</span></span>
<span data-ttu-id="a1833-124">O algoritmo de integridade IPSec do vpnclient (fase 1 da IKE)</span><span class="sxs-lookup"><span data-stu-id="a1833-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="a1833-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="a1833-125">-PfsGroup</span></span>
<span data-ttu-id="a1833-126">Os grupos de PFS do vpnclient usados na fase 2 do IKE para novas associações de SA filho</span><span class="sxs-lookup"><span data-stu-id="a1833-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="a1833-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="a1833-127">-SADataSize</span></span>
<span data-ttu-id="a1833-128">O tamanho da carga de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 do SA) em KB</span><span class="sxs-lookup"><span data-stu-id="a1833-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="a1833-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="a1833-129">-SALifeTime</span></span>
<span data-ttu-id="a1833-130">O tempo de vida da Associação de segurança IPSec do vpnclient (também chamado de modo rápido ou da fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="a1833-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="a1833-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1833-131">CommonParameters</span></span>
<span data-ttu-id="a1833-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1833-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1833-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1833-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1833-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1833-134">INPUTS</span></span>

### <span data-ttu-id="a1833-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1833-135">None</span></span>

## <span data-ttu-id="a1833-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1833-136">OUTPUTS</span></span>

### <span data-ttu-id="a1833-137">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="a1833-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="a1833-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1833-138">NOTES</span></span>

## <span data-ttu-id="a1833-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1833-139">RELATED LINKS</span></span>
