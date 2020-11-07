---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955866"
---
# <span data-ttu-id="8f6d7-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8f6d7-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="8f6d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f6d7-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6d7-103">Obtém os parâmetros de IPSec VPN definidos no gateway de rede virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="8f6d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f6d7-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f6d7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f6d7-105">DESCRIPTION</span></span>
<span data-ttu-id="8f6d7-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="8f6d7-107">O cmdlet **Get-AzVpnClientIpsecParameter** retorna o objeto dos parâmetros de VPN IPSec definidos no gateway do Azure com base no nome do gateway e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="8f6d7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f6d7-108">EXAMPLES</span></span>

### <span data-ttu-id="8f6d7-109">Exemplo 1: Obtém os parâmetros de IPSec VPN definidos no gateway de rede virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="8f6d7-110">Retorna o objeto dos parâmetros de VPN IPSec definidos no gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="8f6d7-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="8f6d7-111">OS</span><span class="sxs-lookup"><span data-stu-id="8f6d7-111">PARAMETERS</span></span>

### <span data-ttu-id="8f6d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6d7-112">-DefaultProfile</span></span>
<span data-ttu-id="8f6d7-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6d7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f6d7-114">-Name</span></span>
<span data-ttu-id="8f6d7-115">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-115">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6d7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6d7-116">-ResourceGroupName</span></span>
<span data-ttu-id="8f6d7-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f6d7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6d7-118">CommonParameters</span></span>
<span data-ttu-id="8f6d7-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6d7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6d7-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f6d7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6d7-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f6d7-121">INPUTS</span></span>

### <span data-ttu-id="8f6d7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8f6d7-122">System.String</span></span>

## <span data-ttu-id="8f6d7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f6d7-123">OUTPUTS</span></span>

### <span data-ttu-id="8f6d7-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="8f6d7-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="8f6d7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f6d7-125">NOTES</span></span>

## <span data-ttu-id="8f6d7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f6d7-126">RELATED LINKS</span></span>

[<span data-ttu-id="8f6d7-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8f6d7-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8f6d7-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8f6d7-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="8f6d7-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="8f6d7-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
