---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262061"
---
# <span data-ttu-id="4a65a-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="4a65a-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="4a65a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4a65a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a65a-103">Lista os serviços de ponto de extremidade disponíveis para localização.</span><span class="sxs-lookup"><span data-stu-id="4a65a-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="4a65a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a65a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a65a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4a65a-105">DESCRIPTION</span></span>
<span data-ttu-id="4a65a-106">Get-AzVirtualNetworkAvailableEndpointService lista os serviços de ponto de extremidade disponíveis no local especificado.</span><span class="sxs-lookup"><span data-stu-id="4a65a-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="4a65a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a65a-107">EXAMPLES</span></span>

### <span data-ttu-id="4a65a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a65a-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="4a65a-109">Obtém serviços de ponto de extremidade disponíveis na região oeste.</span><span class="sxs-lookup"><span data-stu-id="4a65a-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="4a65a-110">OS</span><span class="sxs-lookup"><span data-stu-id="4a65a-110">PARAMETERS</span></span>

### <span data-ttu-id="4a65a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a65a-111">-DefaultProfile</span></span>
<span data-ttu-id="4a65a-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a65a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a65a-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4a65a-113">-Location</span></span>
<span data-ttu-id="4a65a-114">O local do qual os serviços de ponto de extremidade são recuperados.</span><span class="sxs-lookup"><span data-stu-id="4a65a-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="4a65a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a65a-115">CommonParameters</span></span>
<span data-ttu-id="4a65a-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a65a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a65a-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a65a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a65a-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4a65a-118">INPUTS</span></span>

### <span data-ttu-id="4a65a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="4a65a-119">System.String</span></span>

## <span data-ttu-id="4a65a-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4a65a-120">OUTPUTS</span></span>

### <span data-ttu-id="4a65a-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="4a65a-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="4a65a-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4a65a-122">NOTES</span></span>

## <span data-ttu-id="4a65a-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a65a-123">RELATED LINKS</span></span>
