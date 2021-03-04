---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 70002f85191cda1259cd3b29aa6ee5c6b76a7b94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886923"
---
# <span data-ttu-id="f54e5-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="f54e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f54e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f54e5-103">Obtém um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f54e5-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="f54e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f54e5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f54e5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f54e5-105">DESCRIPTION</span></span>
<span data-ttu-id="f54e5-106">O Gateway de Rede Virtual é o objeto que representa seu gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="f54e5-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="f54e5-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do gateway no Azure com base em Nome e Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="f54e5-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f54e5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f54e5-108">EXAMPLES</span></span>

### <span data-ttu-id="f54e5-109">Exemplo 1: Obter um Gateway de Rede Virtual</span><span class="sxs-lookup"><span data-stu-id="f54e5-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="f54e5-110">Retorna o objeto do Gateway de Rede Virtual com o nome "myGateway1" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="f54e5-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="f54e5-111">Exemplo 2: Obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="f54e5-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="f54e5-112">Retorna todos os Gateways de Rede Virtual que começam com "myGateway" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="f54e5-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="f54e5-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f54e5-113">PARAMETERS</span></span>

### <span data-ttu-id="f54e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f54e5-114">-DefaultProfile</span></span>
<span data-ttu-id="f54e5-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f54e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f54e5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f54e5-116">-Name</span></span>
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

### <span data-ttu-id="f54e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f54e5-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f54e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f54e5-118">CommonParameters</span></span>
<span data-ttu-id="f54e5-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f54e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f54e5-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f54e5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f54e5-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f54e5-121">INPUTS</span></span>

### <span data-ttu-id="f54e5-122">System.String</span><span class="sxs-lookup"><span data-stu-id="f54e5-122">System.String</span></span>

## <span data-ttu-id="f54e5-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f54e5-123">OUTPUTS</span></span>

### <span data-ttu-id="f54e5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f54e5-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="f54e5-125">NOTES</span></span>

## <span data-ttu-id="f54e5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f54e5-126">RELATED LINKS</span></span>

[<span data-ttu-id="f54e5-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f54e5-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f54e5-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f54e5-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="f54e5-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f54e5-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
