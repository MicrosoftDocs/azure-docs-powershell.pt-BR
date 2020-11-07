---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775526"
---
# <span data-ttu-id="b87c7-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b87c7-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="b87c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b87c7-102">SYNOPSIS</span></span>
<span data-ttu-id="b87c7-103">Obtém um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="b87c7-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="b87c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b87c7-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b87c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b87c7-105">DESCRIPTION</span></span>
<span data-ttu-id="b87c7-106">O gateway de rede local é o objeto que representa o seu dispositivo VPN local.</span><span class="sxs-lookup"><span data-stu-id="b87c7-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="b87c7-107">O cmdlet **Get-AzLocalNetworkGateway** retorna o objeto que representa o gateway local com base no nome e no nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b87c7-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b87c7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b87c7-108">EXAMPLES</span></span>

### <span data-ttu-id="b87c7-109">1: obter um gateway de rede local</span><span class="sxs-lookup"><span data-stu-id="b87c7-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="b87c7-110">Retorna o objeto do gateway de rede local com o nome "myLocalGW" no grupo de recursos "myRG"</span><span class="sxs-lookup"><span data-stu-id="b87c7-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="b87c7-111">OS</span><span class="sxs-lookup"><span data-stu-id="b87c7-111">PARAMETERS</span></span>

### <span data-ttu-id="b87c7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87c7-112">-DefaultProfile</span></span>
<span data-ttu-id="b87c7-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b87c7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b87c7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b87c7-114">-Name</span></span>
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

### <span data-ttu-id="b87c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b87c7-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b87c7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87c7-116">CommonParameters</span></span>
<span data-ttu-id="b87c7-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b87c7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87c7-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b87c7-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87c7-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b87c7-119">INPUTS</span></span>

## <span data-ttu-id="b87c7-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b87c7-120">OUTPUTS</span></span>

### <span data-ttu-id="b87c7-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b87c7-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b87c7-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b87c7-122">NOTES</span></span>

## <span data-ttu-id="b87c7-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b87c7-123">RELATED LINKS</span></span>

