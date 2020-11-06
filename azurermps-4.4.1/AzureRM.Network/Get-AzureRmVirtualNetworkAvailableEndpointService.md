---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 15f1c71e313cfd684c384446f0ffd2913c69143c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431099"
---
# <span data-ttu-id="f631f-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="f631f-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="f631f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f631f-102">SYNOPSIS</span></span>
<span data-ttu-id="f631f-103">Lista os serviços de ponto de extremidade disponíveis para localização.</span><span class="sxs-lookup"><span data-stu-id="f631f-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f631f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f631f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f631f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f631f-105">DESCRIPTION</span></span>
<span data-ttu-id="f631f-106">Get-AzureRmVirtualNetworkAvailableEndpointService lista os serviços de ponto de extremidade disponíveis no local especificado.</span><span class="sxs-lookup"><span data-stu-id="f631f-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="f631f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f631f-107">EXAMPLES</span></span>

### <span data-ttu-id="f631f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f631f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="f631f-109">Obtém serviços de ponto de extremidade disponíveis na região oeste.</span><span class="sxs-lookup"><span data-stu-id="f631f-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="f631f-110">OS</span><span class="sxs-lookup"><span data-stu-id="f631f-110">PARAMETERS</span></span>

### <span data-ttu-id="f631f-111">-Local</span><span class="sxs-lookup"><span data-stu-id="f631f-111">-Location</span></span>
<span data-ttu-id="f631f-112">O local do qual os serviços de ponto de extremidade são recuperados.</span><span class="sxs-lookup"><span data-stu-id="f631f-112">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="f631f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f631f-113">-DefaultProfile</span></span>
<span data-ttu-id="f631f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f631f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f631f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f631f-115">CommonParameters</span></span>
<span data-ttu-id="f631f-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f631f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f631f-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f631f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f631f-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f631f-118">INPUTS</span></span>

### <span data-ttu-id="f631f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f631f-119">System.String</span></span>

## <span data-ttu-id="f631f-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f631f-120">OUTPUTS</span></span>

### <span data-ttu-id="f631f-121">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f631f-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f631f-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f631f-122">NOTES</span></span>

## <span data-ttu-id="f631f-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f631f-123">RELATED LINKS</span></span>

