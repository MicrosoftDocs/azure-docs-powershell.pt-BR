---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771969"
---
# <span data-ttu-id="2bc57-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="2bc57-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bc57-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc57-103">Obtém um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2bc57-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="2bc57-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc57-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bc57-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bc57-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc57-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc57-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="2bc57-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2bc57-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2bc57-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bc57-108">EXAMPLES</span></span>

### <span data-ttu-id="2bc57-109">1: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2bc57-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="2bc57-110">Retorna o objeto do gateway de rede virtual com o nome "myGateway1" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="2bc57-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="2bc57-111">2: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="2bc57-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="2bc57-112">Retorna todos os gateways de rede virtual que começam com "mygateway" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="2bc57-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="2bc57-113">OS</span><span class="sxs-lookup"><span data-stu-id="2bc57-113">PARAMETERS</span></span>

### <span data-ttu-id="2bc57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc57-114">-DefaultProfile</span></span>
<span data-ttu-id="2bc57-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc57-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bc57-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bc57-116">-Name</span></span>
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

### <span data-ttu-id="2bc57-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc57-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2bc57-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc57-118">CommonParameters</span></span>
<span data-ttu-id="2bc57-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc57-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc57-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bc57-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc57-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bc57-121">INPUTS</span></span>

### <span data-ttu-id="2bc57-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc57-122">System.String</span></span>

## <span data-ttu-id="2bc57-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bc57-123">OUTPUTS</span></span>

### <span data-ttu-id="2bc57-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="2bc57-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bc57-125">NOTES</span></span>

## <span data-ttu-id="2bc57-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bc57-126">RELATED LINKS</span></span>

[<span data-ttu-id="2bc57-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2bc57-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2bc57-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2bc57-130">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2bc57-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2bc57-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
