---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: c0599f599770467c3528cff902d2d60434c335e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785706"
---
# <span data-ttu-id="7f20f-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7f20f-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7f20f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f20f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f20f-103">Obtém uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7f20f-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f20f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f20f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f20f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f20f-105">DESCRIPTION</span></span>
<span data-ttu-id="7f20f-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="7f20f-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="7f20f-107">O cmdlet **Get-AzureRmVirtualNetworkGatewayConnection** retorna o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7f20f-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7f20f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f20f-108">EXAMPLES</span></span>

### <span data-ttu-id="7f20f-109">1: obter uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="7f20f-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="7f20f-110">Retorna o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="7f20f-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="7f20f-111">OS</span><span class="sxs-lookup"><span data-stu-id="7f20f-111">PARAMETERS</span></span>

### <span data-ttu-id="7f20f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f20f-112">-DefaultProfile</span></span>
<span data-ttu-id="7f20f-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f20f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f20f-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f20f-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f20f-116">CommonParameters</span></span>
<span data-ttu-id="7f20f-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f20f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f20f-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f20f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f20f-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f20f-119">INPUTS</span></span>

## <span data-ttu-id="7f20f-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f20f-120">OUTPUTS</span></span>

### <span data-ttu-id="7f20f-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7f20f-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7f20f-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f20f-122">NOTES</span></span>

## <span data-ttu-id="7f20f-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f20f-123">RELATED LINKS</span></span>

