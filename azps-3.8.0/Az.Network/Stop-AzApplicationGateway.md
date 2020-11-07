---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777418"
---
# <span data-ttu-id="daf38-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="daf38-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daf38-102">SYNOPSIS</span></span>
<span data-ttu-id="daf38-103">Interrompe um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="daf38-103">Stops an application gateway</span></span>

## <span data-ttu-id="daf38-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="daf38-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daf38-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="daf38-105">DESCRIPTION</span></span>
<span data-ttu-id="daf38-106">O cmdlet **Stop-AzApplicationGateway** interrompe um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="daf38-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="daf38-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daf38-107">EXAMPLES</span></span>

### <span data-ttu-id="daf38-108">Exemplo 1: parar um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="daf38-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="daf38-109">Esse comando interrompe o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="daf38-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="daf38-110">OS</span><span class="sxs-lookup"><span data-stu-id="daf38-110">PARAMETERS</span></span>

### <span data-ttu-id="daf38-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-111">-ApplicationGateway</span></span>
<span data-ttu-id="daf38-112">Especifica o gateway do aplicativo em que este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="daf38-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="daf38-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daf38-113">-AsJob</span></span>
<span data-ttu-id="daf38-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="daf38-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf38-115">-DefaultProfile</span></span>
<span data-ttu-id="daf38-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daf38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daf38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf38-117">CommonParameters</span></span>
<span data-ttu-id="daf38-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf38-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf38-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf38-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="daf38-120">INPUTS</span></span>

### <span data-ttu-id="daf38-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daf38-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="daf38-122">OUTPUTS</span></span>

### <span data-ttu-id="daf38-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daf38-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="daf38-124">NOTES</span></span>

## <span data-ttu-id="daf38-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daf38-125">RELATED LINKS</span></span>

[<span data-ttu-id="daf38-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="daf38-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="daf38-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="daf38-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="daf38-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daf38-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


