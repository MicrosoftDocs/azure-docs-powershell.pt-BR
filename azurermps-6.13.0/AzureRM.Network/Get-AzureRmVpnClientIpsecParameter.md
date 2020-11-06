---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 539ae515d664aaeb01ca824603cd8ee3ed38f0fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429491"
---
# <span data-ttu-id="62365-101">Get-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="62365-101">Get-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="62365-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62365-102">SYNOPSIS</span></span>
<span data-ttu-id="62365-103">Obtém os parâmetros de IPSec VPN definidos no gateway de rede virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="62365-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62365-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62365-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62365-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62365-105">DESCRIPTION</span></span>
<span data-ttu-id="62365-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="62365-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="62365-107">O cmdlet **Get-AzureRmVpnClientIpsecParameter** retorna o objeto dos parâmetros de VPN IPSec definidos no gateway do Azure com base no nome do gateway e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62365-107">The **Get-AzureRmVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="62365-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62365-108">EXAMPLES</span></span>

### <span data-ttu-id="62365-109">1: Obtém os parâmetros de VPN IPSec definidos no gateway de rede virtual para conexões ponto a site.</span><span class="sxs-lookup"><span data-stu-id="62365-109">1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```
PS C:\> $VpnClientIPsecParameters = Get-AzureRmVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="62365-110">Retorna o objeto dos parâmetros de VPN IPSec definidos no gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="62365-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="62365-111">OS</span><span class="sxs-lookup"><span data-stu-id="62365-111">PARAMETERS</span></span>

### <span data-ttu-id="62365-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62365-112">-DefaultProfile</span></span>
<span data-ttu-id="62365-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62365-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62365-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="62365-114">-Name</span></span>
<span data-ttu-id="62365-115">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="62365-115">The resource name.</span></span>

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

### <span data-ttu-id="62365-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62365-116">-ResourceGroupName</span></span>
<span data-ttu-id="62365-117">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62365-117">The resource group name.</span></span>

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

### <span data-ttu-id="62365-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62365-118">CommonParameters</span></span>
<span data-ttu-id="62365-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62365-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62365-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62365-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62365-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62365-121">INPUTS</span></span>

### <span data-ttu-id="62365-122">System. String</span><span class="sxs-lookup"><span data-stu-id="62365-122">System.String</span></span>

## <span data-ttu-id="62365-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62365-123">OUTPUTS</span></span>

### <span data-ttu-id="62365-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="62365-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="62365-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62365-125">NOTES</span></span>

## <span data-ttu-id="62365-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62365-126">RELATED LINKS</span></span>
