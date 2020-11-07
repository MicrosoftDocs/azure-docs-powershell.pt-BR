---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775481"
---
# <span data-ttu-id="baccf-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="baccf-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="baccf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="baccf-102">SYNOPSIS</span></span>
<span data-ttu-id="baccf-103">Obtém um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="baccf-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="baccf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="baccf-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baccf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="baccf-105">DESCRIPTION</span></span>
<span data-ttu-id="baccf-106">O gateway de rede virtual é o objeto que representa o gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="baccf-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="baccf-107">O cmdlet **Get-AzVirtualNetworkGateway** retorna o objeto do seu gateway no Azure com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="baccf-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="baccf-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="baccf-108">EXAMPLES</span></span>

### <span data-ttu-id="baccf-109">1: obter um gateway de rede virtual</span><span class="sxs-lookup"><span data-stu-id="baccf-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="baccf-110">Retorna o objeto do gateway de rede virtual com o nome "mygateway" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="baccf-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="baccf-111">OS</span><span class="sxs-lookup"><span data-stu-id="baccf-111">PARAMETERS</span></span>

### <span data-ttu-id="baccf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baccf-112">-DefaultProfile</span></span>
<span data-ttu-id="baccf-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="baccf-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baccf-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="baccf-114">-Name</span></span>
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

### <span data-ttu-id="baccf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baccf-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="baccf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baccf-116">CommonParameters</span></span>
<span data-ttu-id="baccf-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baccf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baccf-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baccf-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baccf-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="baccf-119">INPUTS</span></span>

## <span data-ttu-id="baccf-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="baccf-120">OUTPUTS</span></span>

### <span data-ttu-id="baccf-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="baccf-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="baccf-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="baccf-122">NOTES</span></span>

## <span data-ttu-id="baccf-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="baccf-123">RELATED LINKS</span></span>

