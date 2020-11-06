---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431098"
---
# <span data-ttu-id="057e7-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="057e7-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="057e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="057e7-102">SYNOPSIS</span></span>
<span data-ttu-id="057e7-103">Obtém um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="057e7-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="057e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="057e7-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="057e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="057e7-105">DESCRIPTION</span></span>
<span data-ttu-id="057e7-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="057e7-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="057e7-107">O cmdlet **Get-AzureRmVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="057e7-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="057e7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="057e7-108">EXAMPLES</span></span>

### <span data-ttu-id="057e7-109">1: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="057e7-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="057e7-110">Retorna o objeto do gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="057e7-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="057e7-111">OS</span><span class="sxs-lookup"><span data-stu-id="057e7-111">PARAMETERS</span></span>

### <span data-ttu-id="057e7-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="057e7-112">-Name</span></span>
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

### <span data-ttu-id="057e7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="057e7-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="057e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="057e7-114">-DefaultProfile</span></span>
<span data-ttu-id="057e7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="057e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="057e7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057e7-116">CommonParameters</span></span>
<span data-ttu-id="057e7-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="057e7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057e7-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="057e7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057e7-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="057e7-119">INPUTS</span></span>

## <span data-ttu-id="057e7-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="057e7-120">OUTPUTS</span></span>

### <span data-ttu-id="057e7-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="057e7-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="057e7-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="057e7-122">NOTES</span></span>

## <span data-ttu-id="057e7-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="057e7-123">RELATED LINKS</span></span>

