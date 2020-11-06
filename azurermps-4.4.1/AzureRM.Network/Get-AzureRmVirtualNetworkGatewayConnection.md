---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3d58e2f9fbd62826084df329cd7047a293ef0291
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431096"
---
# <span data-ttu-id="8b136-101">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8b136-101">Get-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8b136-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b136-102">SYNOPSIS</span></span>
<span data-ttu-id="8b136-103">Obtém uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="8b136-103">Gets a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b136-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b136-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b136-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b136-105">DESCRIPTION</span></span>
<span data-ttu-id="8b136-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="8b136-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="8b136-107">O cmdlet **Get-AzureRmVirtualNetworkGatewayConnection** retorna o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b136-107">The **Get-AzureRmVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="8b136-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b136-108">EXAMPLES</span></span>

### <span data-ttu-id="8b136-109">1: obter uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="8b136-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="8b136-110">Retorna o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="8b136-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="8b136-111">OS</span><span class="sxs-lookup"><span data-stu-id="8b136-111">PARAMETERS</span></span>

### <span data-ttu-id="8b136-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b136-112">-Name</span></span>
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

### <span data-ttu-id="8b136-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b136-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8b136-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b136-114">-DefaultProfile</span></span>
<span data-ttu-id="8b136-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b136-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b136-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b136-116">CommonParameters</span></span>
<span data-ttu-id="8b136-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b136-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b136-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b136-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b136-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b136-119">INPUTS</span></span>

## <span data-ttu-id="8b136-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b136-120">OUTPUTS</span></span>

### <span data-ttu-id="8b136-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8b136-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="8b136-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b136-122">NOTES</span></span>

## <span data-ttu-id="8b136-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b136-123">RELATED LINKS</span></span>

