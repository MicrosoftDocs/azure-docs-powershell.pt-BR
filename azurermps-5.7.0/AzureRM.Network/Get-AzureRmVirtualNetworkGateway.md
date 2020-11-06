---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 29d5ad86d9df7bddec8be600d8b7c680c7bcd7fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428169"
---
# <span data-ttu-id="4eea3-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4eea3-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="4eea3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4eea3-102">SYNOPSIS</span></span>
<span data-ttu-id="4eea3-103">Obtém um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4eea3-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eea3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4eea3-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eea3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4eea3-105">DESCRIPTION</span></span>
<span data-ttu-id="4eea3-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="4eea3-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="4eea3-107">O cmdlet **Get-AzureRmVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4eea3-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="4eea3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eea3-108">EXAMPLES</span></span>

### <span data-ttu-id="4eea3-109">1: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4eea3-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="4eea3-110">Retorna o objeto do gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="4eea3-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="4eea3-111">OS</span><span class="sxs-lookup"><span data-stu-id="4eea3-111">PARAMETERS</span></span>

### <span data-ttu-id="4eea3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eea3-112">-DefaultProfile</span></span>
<span data-ttu-id="4eea3-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4eea3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4eea3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="4eea3-114">-Name</span></span>
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

### <span data-ttu-id="4eea3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eea3-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="4eea3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eea3-116">CommonParameters</span></span>
<span data-ttu-id="4eea3-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eea3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eea3-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eea3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eea3-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4eea3-119">INPUTS</span></span>

### <span data-ttu-id="4eea3-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4eea3-120">None</span></span>
<span data-ttu-id="4eea3-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4eea3-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4eea3-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4eea3-122">OUTPUTS</span></span>

### <span data-ttu-id="4eea3-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4eea3-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4eea3-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4eea3-124">NOTES</span></span>

## <span data-ttu-id="4eea3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eea3-125">RELATED LINKS</span></span>

