---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111681"
---
# <span data-ttu-id="c6a20-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="c6a20-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="c6a20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6a20-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a20-103">Lista os serviços de ponto de extremidade disponíveis para localização.</span><span class="sxs-lookup"><span data-stu-id="c6a20-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="c6a20-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6a20-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a20-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6a20-105">DESCRIPTION</span></span>
<span data-ttu-id="c6a20-106">Get-AzVirtualNetworkAvailableEndpointService lista os serviços de ponto de extremidade disponíveis no local especificado.</span><span class="sxs-lookup"><span data-stu-id="c6a20-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="c6a20-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6a20-107">EXAMPLES</span></span>

### <span data-ttu-id="c6a20-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6a20-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="c6a20-109">Obtém serviços de ponto de extremidade disponíveis na região oeste.</span><span class="sxs-lookup"><span data-stu-id="c6a20-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="c6a20-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6a20-110">PARAMETERS</span></span>

### <span data-ttu-id="c6a20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a20-111">-DefaultProfile</span></span>
<span data-ttu-id="c6a20-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c6a20-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6a20-113">-Local</span><span class="sxs-lookup"><span data-stu-id="c6a20-113">-Location</span></span>
<span data-ttu-id="c6a20-114">O local de onde recuperar os serviços de ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c6a20-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="c6a20-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a20-115">CommonParameters</span></span>
<span data-ttu-id="c6a20-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a20-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a20-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6a20-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a20-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="c6a20-118">INPUTS</span></span>

### <span data-ttu-id="c6a20-119">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a20-119">System.String</span></span>

## <span data-ttu-id="c6a20-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="c6a20-120">OUTPUTS</span></span>

### <span data-ttu-id="c6a20-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="c6a20-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="c6a20-122">Notas</span><span class="sxs-lookup"><span data-stu-id="c6a20-122">NOTES</span></span>

## <span data-ttu-id="c6a20-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6a20-123">RELATED LINKS</span></span>
