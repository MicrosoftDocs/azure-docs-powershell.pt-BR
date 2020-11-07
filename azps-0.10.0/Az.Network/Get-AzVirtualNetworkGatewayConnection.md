---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 8658dcf73d6cf1549ac6471e79269883abdf7616
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775469"
---
# <span data-ttu-id="78bd8-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="78bd8-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="78bd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="78bd8-103">Obtém uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="78bd8-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="78bd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78bd8-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78bd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="78bd8-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="78bd8-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="78bd8-107">O cmdlet **Get-AzVirtualNetworkGatewayConnection** retorna o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="78bd8-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="78bd8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78bd8-108">EXAMPLES</span></span>

### <span data-ttu-id="78bd8-109">1: obter uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="78bd8-109">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="78bd8-110">Retorna o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="78bd8-110">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="78bd8-111">OS</span><span class="sxs-lookup"><span data-stu-id="78bd8-111">PARAMETERS</span></span>

### <span data-ttu-id="78bd8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78bd8-112">-DefaultProfile</span></span>
<span data-ttu-id="78bd8-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78bd8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78bd8-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="78bd8-114">-Name</span></span>
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

### <span data-ttu-id="78bd8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78bd8-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="78bd8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78bd8-116">CommonParameters</span></span>
<span data-ttu-id="78bd8-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78bd8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78bd8-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78bd8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78bd8-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78bd8-119">INPUTS</span></span>

## <span data-ttu-id="78bd8-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78bd8-120">OUTPUTS</span></span>

### <span data-ttu-id="78bd8-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="78bd8-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="78bd8-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78bd8-122">NOTES</span></span>

## <span data-ttu-id="78bd8-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78bd8-123">RELATED LINKS</span></span>

