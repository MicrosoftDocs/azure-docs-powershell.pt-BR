---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: e82ff9f04782842fc44a8da95b3e2656c2b86024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428170"
---
# <span data-ttu-id="50928-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="50928-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="50928-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="50928-102">SYNOPSIS</span></span>
<span data-ttu-id="50928-103">Lista os serviços de ponto de extremidade disponíveis para localização.</span><span class="sxs-lookup"><span data-stu-id="50928-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50928-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="50928-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50928-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="50928-105">DESCRIPTION</span></span>
<span data-ttu-id="50928-106">Get-AzureRmVirtualNetworkAvailableEndpointService lista os serviços de ponto de extremidade disponíveis no local especificado.</span><span class="sxs-lookup"><span data-stu-id="50928-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="50928-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50928-107">EXAMPLES</span></span>

### <span data-ttu-id="50928-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50928-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="50928-109">Obtém serviços de ponto de extremidade disponíveis na região oeste.</span><span class="sxs-lookup"><span data-stu-id="50928-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="50928-110">OS</span><span class="sxs-lookup"><span data-stu-id="50928-110">PARAMETERS</span></span>

### <span data-ttu-id="50928-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50928-111">-DefaultProfile</span></span>
<span data-ttu-id="50928-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="50928-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50928-113">-Local</span><span class="sxs-lookup"><span data-stu-id="50928-113">-Location</span></span>
<span data-ttu-id="50928-114">O local do qual os serviços de ponto de extremidade são recuperados.</span><span class="sxs-lookup"><span data-stu-id="50928-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="50928-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50928-115">CommonParameters</span></span>
<span data-ttu-id="50928-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50928-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50928-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50928-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50928-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="50928-118">INPUTS</span></span>

### <span data-ttu-id="50928-119">System. String</span><span class="sxs-lookup"><span data-stu-id="50928-119">System.String</span></span>

## <span data-ttu-id="50928-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="50928-120">OUTPUTS</span></span>

### <span data-ttu-id="50928-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50928-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="50928-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="50928-122">NOTES</span></span>

## <span data-ttu-id="50928-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50928-123">RELATED LINKS</span></span>

