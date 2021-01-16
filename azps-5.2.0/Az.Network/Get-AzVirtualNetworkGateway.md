---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262058"
---
# <span data-ttu-id="25d8b-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="25d8b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="25d8b-103">Obtém um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="25d8b-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="25d8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25d8b-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25d8b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="25d8b-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="25d8b-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="25d8b-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="25d8b-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="25d8b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25d8b-108">EXAMPLES</span></span>

### <span data-ttu-id="25d8b-109">Exemplo 1: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="25d8b-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="25d8b-110">Retorna o objeto do gateway de rede virtual com o nome "myGateway1" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="25d8b-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="25d8b-111">Exemplo 2: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="25d8b-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="25d8b-112">Retorna todos os gateways de rede virtual que começam com "mygateway" dentro do grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="25d8b-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="25d8b-113">OS</span><span class="sxs-lookup"><span data-stu-id="25d8b-113">PARAMETERS</span></span>

### <span data-ttu-id="25d8b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25d8b-114">-DefaultProfile</span></span>
<span data-ttu-id="25d8b-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25d8b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25d8b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="25d8b-116">-Name</span></span>
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

### <span data-ttu-id="25d8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d8b-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="25d8b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d8b-118">CommonParameters</span></span>
<span data-ttu-id="25d8b-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d8b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d8b-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25d8b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d8b-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25d8b-121">INPUTS</span></span>

### <span data-ttu-id="25d8b-122">System. String</span><span class="sxs-lookup"><span data-stu-id="25d8b-122">System.String</span></span>

## <span data-ttu-id="25d8b-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25d8b-123">OUTPUTS</span></span>

### <span data-ttu-id="25d8b-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="25d8b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25d8b-125">NOTES</span></span>

## <span data-ttu-id="25d8b-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25d8b-126">RELATED LINKS</span></span>

[<span data-ttu-id="25d8b-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25d8b-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25d8b-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25d8b-130">Redimensionar-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="25d8b-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="25d8b-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
