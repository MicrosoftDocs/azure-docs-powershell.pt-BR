---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602788"
---
# <span data-ttu-id="49006-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="49006-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49006-102">SYNOPSIS</span></span>
<span data-ttu-id="49006-103">Interrompe um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="49006-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49006-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49006-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49006-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49006-105">DESCRIPTION</span></span>
<span data-ttu-id="49006-106">O cmdlet **Stop-AzureRmApplicationGateway** interrompe um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49006-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="49006-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49006-107">EXAMPLES</span></span>

### <span data-ttu-id="49006-108">Exemplo 1: parar um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="49006-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="49006-109">Esse comando interrompe o aplicativo gateway armazenado na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="49006-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="49006-110">OS</span><span class="sxs-lookup"><span data-stu-id="49006-110">PARAMETERS</span></span>

### <span data-ttu-id="49006-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-111">-ApplicationGateway</span></span>
<span data-ttu-id="49006-112">Especifica o gateway do aplicativo em que este cmdlet é interrompido.</span><span class="sxs-lookup"><span data-stu-id="49006-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="49006-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49006-113">-AsJob</span></span>
<span data-ttu-id="49006-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="49006-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49006-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49006-115">-DefaultProfile</span></span>
<span data-ttu-id="49006-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49006-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49006-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49006-117">CommonParameters</span></span>
<span data-ttu-id="49006-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49006-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49006-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49006-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49006-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49006-120">INPUTS</span></span>

### <span data-ttu-id="49006-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="49006-122">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49006-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="49006-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49006-123">OUTPUTS</span></span>

### <span data-ttu-id="49006-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="49006-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49006-125">NOTES</span></span>

## <span data-ttu-id="49006-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49006-126">RELATED LINKS</span></span>

[<span data-ttu-id="49006-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="49006-128">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="49006-129">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="49006-130">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="49006-131">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="49006-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


