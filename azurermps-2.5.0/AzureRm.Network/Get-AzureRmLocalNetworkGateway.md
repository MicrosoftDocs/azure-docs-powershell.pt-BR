---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 1a2a8aa8405be5dfc5275a07d253f06f1134e3e7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785911"
---
# <span data-ttu-id="69126-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="69126-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="69126-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69126-102">SYNOPSIS</span></span>
<span data-ttu-id="69126-103">Obtém um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="69126-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69126-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69126-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69126-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69126-105">DESCRIPTION</span></span>
<span data-ttu-id="69126-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="69126-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="69126-107">O cmdlet **Get-AzureRmLocalNetworkGateway** retorna o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69126-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="69126-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69126-108">EXAMPLES</span></span>

### <span data-ttu-id="69126-109">1: obter um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="69126-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="69126-110">Retorna o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="69126-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="69126-111">OS</span><span class="sxs-lookup"><span data-stu-id="69126-111">PARAMETERS</span></span>

### <span data-ttu-id="69126-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69126-112">-DefaultProfile</span></span>
<span data-ttu-id="69126-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69126-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69126-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="69126-114">-Name</span></span>
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

### <span data-ttu-id="69126-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69126-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="69126-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69126-116">CommonParameters</span></span>
<span data-ttu-id="69126-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69126-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69126-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69126-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69126-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69126-119">INPUTS</span></span>

## <span data-ttu-id="69126-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69126-120">OUTPUTS</span></span>

### <span data-ttu-id="69126-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="69126-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="69126-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69126-122">NOTES</span></span>

## <span data-ttu-id="69126-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69126-123">RELATED LINKS</span></span>

