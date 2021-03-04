---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885386"
---
# <span data-ttu-id="c99d4-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c99d4-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="c99d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c99d4-102">SYNOPSIS</span></span>
<span data-ttu-id="c99d4-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c99d4-103">Starts an application gateway.</span></span>

## <span data-ttu-id="c99d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c99d4-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c99d4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c99d4-105">DESCRIPTION</span></span>
<span data-ttu-id="c99d4-106">O cmdlet **Start-AzApplicationGateway** inicia um gateway de aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="c99d4-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="c99d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c99d4-107">EXAMPLES</span></span>

### <span data-ttu-id="c99d4-108">Exemplo1: Iniciar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c99d4-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="c99d4-109">Este comando inicia o gateway de aplicativo armazenado na variável $AppGw de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c99d4-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="c99d4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c99d4-110">PARAMETERS</span></span>

### <span data-ttu-id="c99d4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c99d4-111">-ApplicationGateway</span></span>
<span data-ttu-id="c99d4-112">Especifica o gateway de aplicativo que este cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="c99d4-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c99d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99d4-113">-DefaultProfile</span></span>
<span data-ttu-id="c99d4-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c99d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c99d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99d4-115">CommonParameters</span></span>
<span data-ttu-id="c99d4-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c99d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99d4-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c99d4-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99d4-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c99d4-118">INPUTS</span></span>

### <span data-ttu-id="c99d4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c99d4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c99d4-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c99d4-120">OUTPUTS</span></span>

### <span data-ttu-id="c99d4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c99d4-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c99d4-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="c99d4-122">NOTES</span></span>

## <span data-ttu-id="c99d4-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c99d4-123">RELATED LINKS</span></span>

[<span data-ttu-id="c99d4-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c99d4-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


