---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260720"
---
# <span data-ttu-id="bde96-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bde96-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="bde96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bde96-102">SYNOPSIS</span></span>
<span data-ttu-id="bde96-103">Obtém uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="bde96-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="bde96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bde96-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bde96-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bde96-105">DESCRIPTION</span></span>
<span data-ttu-id="bde96-106">A conexão de gateway de rede virtual é o objeto que representa o túnel IPsec (de site para site ou vnet para vnet) conectado ao gateway de rede virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="bde96-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="bde96-107">O cmdlet **Get-AzVirtualNetworkGatewayConnection** retorna o objeto da sua conexão com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bde96-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="bde96-108">Se o cmdlet **Get-AzVirtualNetworkGatewayConnection** for emitido sem especificar o parâmetro-Name, a saída não mostrará os detalhes ConnectionStatus e SharedKey.</span><span class="sxs-lookup"><span data-stu-id="bde96-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="bde96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bde96-109">EXAMPLES</span></span>

### <span data-ttu-id="bde96-110">1: obter uma conexão de gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="bde96-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="bde96-111">Retorna o objeto da conexão do gateway de rede virtual com o nome "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="bde96-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="bde96-112">2: obter todas as conexões de gateway de rede virtual usando filtragem</span><span class="sxs-lookup"><span data-stu-id="bde96-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="bde96-113">Retorna todas as conexões de gateway de rede virtual que começam com "mytunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="bde96-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="bde96-114">OS</span><span class="sxs-lookup"><span data-stu-id="bde96-114">PARAMETERS</span></span>

### <span data-ttu-id="bde96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde96-115">-DefaultProfile</span></span>
<span data-ttu-id="bde96-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bde96-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bde96-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bde96-117">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bde96-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde96-118">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="bde96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde96-119">CommonParameters</span></span>
<span data-ttu-id="bde96-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bde96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde96-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bde96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde96-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bde96-122">INPUTS</span></span>

### <span data-ttu-id="bde96-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bde96-123">System.String</span></span>

## <span data-ttu-id="bde96-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bde96-124">OUTPUTS</span></span>

### <span data-ttu-id="bde96-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bde96-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="bde96-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bde96-126">NOTES</span></span>

## <span data-ttu-id="bde96-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bde96-127">RELATED LINKS</span></span>

[<span data-ttu-id="bde96-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bde96-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bde96-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bde96-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="bde96-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="bde96-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
