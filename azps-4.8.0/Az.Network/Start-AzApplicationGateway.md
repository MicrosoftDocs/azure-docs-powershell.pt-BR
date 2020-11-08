---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110417"
---
# <span data-ttu-id="f7ee2-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="f7ee2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ee2-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-103">Starts an application gateway.</span></span>

## <span data-ttu-id="f7ee2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7ee2-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7ee2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ee2-106">O cmdlet **Start-AzApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="f7ee2-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="f7ee2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7ee2-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ee2-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="f7ee2-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="f7ee2-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7ee2-110">PARAMETERS</span></span>

### <span data-ttu-id="f7ee2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-111">-ApplicationGateway</span></span>
<span data-ttu-id="f7ee2-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7ee2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ee2-113">-DefaultProfile</span></span>
<span data-ttu-id="f7ee2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ee2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ee2-115">CommonParameters</span></span>
<span data-ttu-id="f7ee2-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ee2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ee2-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ee2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ee2-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7ee2-118">INPUTS</span></span>

### <span data-ttu-id="f7ee2-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7ee2-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7ee2-120">OUTPUTS</span></span>

### <span data-ttu-id="f7ee2-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7ee2-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7ee2-122">NOTES</span></span>

## <span data-ttu-id="f7ee2-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7ee2-123">RELATED LINKS</span></span>

[<span data-ttu-id="f7ee2-124">Parar-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7ee2-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


