---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 2faa1b245a38a5ef66bb5131f79000218c39d55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432931"
---
# <span data-ttu-id="01779-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01779-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="01779-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01779-102">SYNOPSIS</span></span>
<span data-ttu-id="01779-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01779-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01779-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01779-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01779-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01779-105">DESCRIPTION</span></span>
<span data-ttu-id="01779-106">O cmdlet **Start-AzureRmApplicationGateway** inicia um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="01779-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="01779-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01779-107">EXAMPLES</span></span>

### <span data-ttu-id="01779-108">Example1: iniciar um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="01779-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="01779-109">Esse comando inicia o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01779-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="01779-110">OS</span><span class="sxs-lookup"><span data-stu-id="01779-110">PARAMETERS</span></span>

### <span data-ttu-id="01779-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01779-111">-ApplicationGateway</span></span>
<span data-ttu-id="01779-112">Especifica o gateway do aplicativo em que este cmdlet é iniciado.</span><span class="sxs-lookup"><span data-stu-id="01779-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="01779-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01779-113">-DefaultProfile</span></span>
<span data-ttu-id="01779-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01779-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01779-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01779-115">CommonParameters</span></span>
<span data-ttu-id="01779-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01779-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01779-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01779-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01779-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01779-118">INPUTS</span></span>

### <span data-ttu-id="01779-119">System. String</span><span class="sxs-lookup"><span data-stu-id="01779-119">System.String</span></span>

## <span data-ttu-id="01779-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01779-120">OUTPUTS</span></span>

### <span data-ttu-id="01779-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01779-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01779-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01779-122">NOTES</span></span>

## <span data-ttu-id="01779-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01779-123">RELATED LINKS</span></span>

[<span data-ttu-id="01779-124">Parar-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01779-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


