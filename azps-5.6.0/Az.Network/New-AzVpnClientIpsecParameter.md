---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 3b34fb1de6b661a622690f93808eaf0660da461b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890997"
---
# <span data-ttu-id="3d2bd-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d2bd-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="3d2bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3d2bd-103">Este comando permite que os usuários criem o objeto de parâmetros ipsec vpn especificando um ou todos os valores, como IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="3d2bd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d2bd-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d2bd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d2bd-105">DESCRIPTION</span></span>
<span data-ttu-id="3d2bd-106">Este comando permite que os usuários criem o objeto de parâmetros ipsec vpn especificando um ou todos os valores, como IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup para definir no gateway VPN existente.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="3d2bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-107">EXAMPLES</span></span>

### <span data-ttu-id="3d2bd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3d2bd-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="3d2bd-109">New-AzVpnClientIpsecParameter cmdlet é usado para criar o objeto de parâmetros ipsec vpn de usar os valores de um ou todos os parâmetros passados que o usuário pode definir para qualquer gateway de rede virtual existente no ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="3d2bd-110">Este objeto VpnClientIPsecParameters criado é passado para o comando Set-AzVpnClientIpsecParameter para definir a política personalizada ipsec vpn especificada no gateway de rede virtual, conforme mostrado no exemplo acima.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="3d2bd-111">Este comando retorna o objeto VpnClientIPsecParameters que mostra parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="3d2bd-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-112">PARAMETERS</span></span>

### <span data-ttu-id="3d2bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d2bd-113">-DefaultProfile</span></span>
<span data-ttu-id="3d2bd-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d2bd-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="3d2bd-115">-DhGroup</span></span>
<span data-ttu-id="3d2bd-116">Os Grupos DH VpnClient usados na Fase 1 do IKE para SA inicial.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-116">The VpnClient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="3d2bd-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="3d2bd-117">-IkeEncryption</span></span>
<span data-ttu-id="3d2bd-118">O algoritmo de criptografia IKE VpnClient (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="3d2bd-118">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="3d2bd-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="3d2bd-119">-IkeIntegrity</span></span>
<span data-ttu-id="3d2bd-120">O algoritmo de integridade IKE VpnClient (Fase 2 do IKE)</span><span class="sxs-lookup"><span data-stu-id="3d2bd-120">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="3d2bd-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="3d2bd-121">-IpsecEncryption</span></span>
<span data-ttu-id="3d2bd-122">O algoritmo de criptografia IPSec VpnClient (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="3d2bd-122">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="3d2bd-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="3d2bd-123">-IpsecIntegrity</span></span>
<span data-ttu-id="3d2bd-124">O algoritmo de integridade IPSec VpnClient (Fase 1 do IKE)</span><span class="sxs-lookup"><span data-stu-id="3d2bd-124">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="3d2bd-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="3d2bd-125">-PfsGroup</span></span>
<span data-ttu-id="3d2bd-126">Os Grupos PFS vpnClient usados na Fase 2 do IKE para o novo SA filho</span><span class="sxs-lookup"><span data-stu-id="3d2bd-126">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="3d2bd-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="3d2bd-127">-SADataSize</span></span>
<span data-ttu-id="3d2bd-128">O tamanho da carga vpnClient IPSec Security Association (também chamado de Modo Rápido ou Fase 2 SA) no KB</span><span class="sxs-lookup"><span data-stu-id="3d2bd-128">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="3d2bd-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="3d2bd-129">-SALifeTime</span></span>
<span data-ttu-id="3d2bd-130">A vida útil da VpnClient IPSec Security Association (também chamada de Modo Rápido ou Fase 2 SA) em segundos</span><span class="sxs-lookup"><span data-stu-id="3d2bd-130">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="3d2bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d2bd-131">CommonParameters</span></span>
<span data-ttu-id="3d2bd-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d2bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d2bd-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d2bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d2bd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-134">INPUTS</span></span>

### <span data-ttu-id="3d2bd-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d2bd-135">None</span></span>

## <span data-ttu-id="3d2bd-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-136">OUTPUTS</span></span>

### <span data-ttu-id="3d2bd-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3d2bd-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="3d2bd-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d2bd-138">NOTES</span></span>

## <span data-ttu-id="3d2bd-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d2bd-139">RELATED LINKS</span></span>

[<span data-ttu-id="3d2bd-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d2bd-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="3d2bd-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d2bd-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="3d2bd-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d2bd-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
