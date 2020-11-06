---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ca23e58b173ee67917099f2743dac7dbd3d1bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441317"
---
# <span data-ttu-id="33dab-101">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33dab-101">Get-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="33dab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33dab-102">SYNOPSIS</span></span>
<span data-ttu-id="33dab-103">Obtém um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="33dab-103">Gets a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33dab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33dab-104">SYNTAX</span></span>

```
Get-AzureRmLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33dab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33dab-105">DESCRIPTION</span></span>
<span data-ttu-id="33dab-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="33dab-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="33dab-107">O cmdlet **Get-AzureRmLocalNetworkGateway** retorna o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33dab-107">The **Get-AzureRmLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="33dab-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33dab-108">EXAMPLES</span></span>

### <span data-ttu-id="33dab-109">1: obter um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="33dab-109">1: Get a Local Network Gateway</span></span>
```
Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="33dab-110">Retorna o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="33dab-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="33dab-111">OS</span><span class="sxs-lookup"><span data-stu-id="33dab-111">PARAMETERS</span></span>

### <span data-ttu-id="33dab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33dab-112">-DefaultProfile</span></span>
<span data-ttu-id="33dab-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33dab-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33dab-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="33dab-114">-Name</span></span>
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

### <span data-ttu-id="33dab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33dab-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="33dab-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33dab-116">CommonParameters</span></span>
<span data-ttu-id="33dab-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33dab-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33dab-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33dab-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33dab-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33dab-119">INPUTS</span></span>

### <span data-ttu-id="33dab-120">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33dab-120">None</span></span>
<span data-ttu-id="33dab-121">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="33dab-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33dab-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33dab-122">OUTPUTS</span></span>

### <span data-ttu-id="33dab-123">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="33dab-123">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="33dab-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33dab-124">NOTES</span></span>

## <span data-ttu-id="33dab-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33dab-125">RELATED LINKS</span></span>

