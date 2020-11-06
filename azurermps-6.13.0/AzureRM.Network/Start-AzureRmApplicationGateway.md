---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602790"
---
# <span data-ttu-id="06fa0-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="06fa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="06fa0-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06fa0-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06fa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06fa0-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fa0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="06fa0-106">O cmdlet **Start-AzureRmApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="06fa0-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="06fa0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="06fa0-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="06fa0-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="06fa0-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="06fa0-110">OS</span><span class="sxs-lookup"><span data-stu-id="06fa0-110">PARAMETERS</span></span>

### <span data-ttu-id="06fa0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-111">-ApplicationGateway</span></span>
<span data-ttu-id="06fa0-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="06fa0-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="06fa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fa0-113">-DefaultProfile</span></span>
<span data-ttu-id="06fa0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06fa0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06fa0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fa0-115">CommonParameters</span></span>
<span data-ttu-id="06fa0-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fa0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fa0-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fa0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fa0-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06fa0-118">INPUTS</span></span>

### <span data-ttu-id="06fa0-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="06fa0-120">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="06fa0-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="06fa0-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06fa0-121">OUTPUTS</span></span>

### <span data-ttu-id="06fa0-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="06fa0-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06fa0-123">NOTES</span></span>

## <span data-ttu-id="06fa0-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06fa0-124">RELATED LINKS</span></span>

[<span data-ttu-id="06fa0-125">Parar-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06fa0-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


