---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118361"
---
# <span data-ttu-id="a5d19-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="a5d19-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="a5d19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a5d19-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d19-103">Obtém todas as opções de SSL disponíveis para a política SSL do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a5d19-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="a5d19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5d19-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5d19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a5d19-105">DESCRIPTION</span></span>
<span data-ttu-id="a5d19-106">O cmdlet **Get-AzApplicationGatewayAvailableSslOption** obtém todas as opções SSL disponíveis para a política SSL</span><span class="sxs-lookup"><span data-stu-id="a5d19-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="a5d19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d19-107">EXAMPLES</span></span>

### <span data-ttu-id="a5d19-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5d19-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="a5d19-109">Esses comandos retornam todas as opções SSL disponíveis para a política SSL.</span><span class="sxs-lookup"><span data-stu-id="a5d19-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="a5d19-110">OS</span><span class="sxs-lookup"><span data-stu-id="a5d19-110">PARAMETERS</span></span>

### <span data-ttu-id="a5d19-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d19-111">-DefaultProfile</span></span>
<span data-ttu-id="a5d19-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d19-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d19-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d19-113">CommonParameters</span></span>
<span data-ttu-id="a5d19-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d19-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d19-115">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5d19-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d19-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a5d19-116">INPUTS</span></span>

### <span data-ttu-id="a5d19-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a5d19-117">None</span></span>

## <span data-ttu-id="a5d19-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a5d19-118">OUTPUTS</span></span>

### <span data-ttu-id="a5d19-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a5d19-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a5d19-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a5d19-120">NOTES</span></span>

## <span data-ttu-id="a5d19-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d19-121">RELATED LINKS</span></span>
