---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786064"
---
# <span data-ttu-id="b4b01-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4b01-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="b4b01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4b01-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b01-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b4b01-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4b01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4b01-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4b01-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4b01-105">DESCRIPTION</span></span>
<span data-ttu-id="b4b01-106">O cmdlet **Start-AzureRmApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="b4b01-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="b4b01-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4b01-107">EXAMPLES</span></span>

### <span data-ttu-id="b4b01-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="b4b01-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b4b01-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b4b01-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b4b01-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4b01-110">PARAMETERS</span></span>

### <span data-ttu-id="b4b01-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4b01-111">-ApplicationGateway</span></span>
<span data-ttu-id="b4b01-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="b4b01-112">Specifies the application gateway that this cmdlet starts.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4b01-113">-DefaultProfile</span></span>
<span data-ttu-id="b4b01-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b01-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4b01-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b01-115">CommonParameters</span></span>
<span data-ttu-id="b4b01-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4b01-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b01-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b01-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b01-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4b01-118">INPUTS</span></span>

### <span data-ttu-id="b4b01-119">System. String</span><span class="sxs-lookup"><span data-stu-id="b4b01-119">System.String</span></span>

## <span data-ttu-id="b4b01-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4b01-120">OUTPUTS</span></span>

### <span data-ttu-id="b4b01-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4b01-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4b01-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4b01-122">NOTES</span></span>

## <span data-ttu-id="b4b01-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4b01-123">RELATED LINKS</span></span>

[<span data-ttu-id="b4b01-124">Parar-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4b01-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


