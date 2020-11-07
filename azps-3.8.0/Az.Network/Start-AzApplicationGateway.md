---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777431"
---
# <span data-ttu-id="d5e60-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="d5e60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5e60-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e60-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5e60-103">Starts an application gateway.</span></span>

## <span data-ttu-id="d5e60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5e60-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5e60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5e60-105">DESCRIPTION</span></span>
<span data-ttu-id="d5e60-106">O cmdlet **Start-AzApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="d5e60-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="d5e60-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5e60-107">EXAMPLES</span></span>

### <span data-ttu-id="d5e60-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="d5e60-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d5e60-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="d5e60-110">OS</span><span class="sxs-lookup"><span data-stu-id="d5e60-110">PARAMETERS</span></span>

### <span data-ttu-id="d5e60-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-111">-ApplicationGateway</span></span>
<span data-ttu-id="d5e60-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="d5e60-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d5e60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e60-113">-DefaultProfile</span></span>
<span data-ttu-id="d5e60-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5e60-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e60-115">CommonParameters</span></span>
<span data-ttu-id="d5e60-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e60-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e60-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5e60-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e60-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5e60-118">INPUTS</span></span>

### <span data-ttu-id="d5e60-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5e60-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5e60-120">OUTPUTS</span></span>

### <span data-ttu-id="d5e60-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5e60-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5e60-122">NOTES</span></span>

## <span data-ttu-id="d5e60-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5e60-123">RELATED LINKS</span></span>

[<span data-ttu-id="d5e60-124">Parar-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5e60-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


