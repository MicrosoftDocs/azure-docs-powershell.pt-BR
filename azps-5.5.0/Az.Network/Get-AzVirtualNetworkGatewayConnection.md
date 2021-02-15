---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 617FB2F9-05EA-4224-B9A9-2F00A7599486
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d3695216cdbda51ae3583218f7d0993894f472eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114703"
---
# <span data-ttu-id="f15fc-101">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f15fc-101">Get-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f15fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f15fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f15fc-103">Obtém uma conexão virtual de gateway de rede</span><span class="sxs-lookup"><span data-stu-id="f15fc-103">Gets a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="f15fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f15fc-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnection [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f15fc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f15fc-105">DESCRIPTION</span></span>
<span data-ttu-id="f15fc-106">A Conexão virtual do Gateway de Rede é o objeto que representa o túnel IPsec (Site para Site ou Vnet-para-Vnet) conectado ao seu Gateway de Rede Virtual no Azure.</span><span class="sxs-lookup"><span data-stu-id="f15fc-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="f15fc-107">O cmdlet **Get-AzVirtualNetworkGatewayConnection** retorna o objeto da sua conexão com base no Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="f15fc-107">The **Get-AzVirtualNetworkGatewayConnection** cmdlet returns the object of your connection based on Name and Resource Group Name.</span></span>
<span data-ttu-id="f15fc-108">Se o cmdlet **Get-AzVirtualNetworkGatewayConnection** for emitido sem especificar o parâmetro -Name, a saída não mostrará detalhes de ConnectionStatus e SharedKey.</span><span class="sxs-lookup"><span data-stu-id="f15fc-108">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show ConnectionStatus and SharedKey details.</span></span>

## <span data-ttu-id="f15fc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f15fc-109">EXAMPLES</span></span>

### <span data-ttu-id="f15fc-110">1: Obter uma conexão virtual de gateway de rede</span><span class="sxs-lookup"><span data-stu-id="f15fc-110">1: Get a Virtual Network Gateway Connection</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="f15fc-111">Retorna o objeto da Conexão virtual do Gateway de Rede com o nome "meuTunnel" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="f15fc-111">Returns the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

### <span data-ttu-id="f15fc-112">2: Obter todas as Conexões virtuais do Gateway de Rede usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="f15fc-112">2: Get all Virtual Network Gateway Connections using filtering</span></span>
```
Get-AzVirtualNetworkGatewayConnection -Name myTunnel* -ResourceGroupName myRG
```

<span data-ttu-id="f15fc-113">Retorna todas as Conexões virtuais do Gateway de Rede que começam com "myTunnel" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="f15fc-113">Returns all Virtual Network Gateway Connections that start with "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="f15fc-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f15fc-114">PARAMETERS</span></span>

### <span data-ttu-id="f15fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f15fc-115">-DefaultProfile</span></span>
<span data-ttu-id="f15fc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f15fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f15fc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f15fc-117">-Name</span></span>
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

### <span data-ttu-id="f15fc-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f15fc-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f15fc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f15fc-119">CommonParameters</span></span>
<span data-ttu-id="f15fc-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f15fc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f15fc-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f15fc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f15fc-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="f15fc-122">INPUTS</span></span>

### <span data-ttu-id="f15fc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f15fc-123">System.String</span></span>

## <span data-ttu-id="f15fc-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="f15fc-124">OUTPUTS</span></span>

### <span data-ttu-id="f15fc-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f15fc-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f15fc-126">Notas</span><span class="sxs-lookup"><span data-stu-id="f15fc-126">NOTES</span></span>

## <span data-ttu-id="f15fc-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f15fc-127">RELATED LINKS</span></span>

[<span data-ttu-id="f15fc-128">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f15fc-128">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f15fc-129">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f15fc-129">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f15fc-130">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f15fc-130">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
