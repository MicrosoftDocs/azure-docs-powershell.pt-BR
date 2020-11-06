---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: bccdcb5f94cc90dca04229ca643fd23f29a276e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602630"
---
# <span data-ttu-id="d59c0-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d59c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d59c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d59c0-103">Cria uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d59c0-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d59c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d59c0-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d59c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d59c0-105">DESCRIPTION</span></span>
<span data-ttu-id="d59c0-106">O cmdlet **New-AzureRmApplicationGatewayFrontendPort** cria uma porta de front-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c0-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="d59c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d59c0-107">EXAMPLES</span></span>

### <span data-ttu-id="d59c0-108">Example1: criar uma porta de front-end</span><span class="sxs-lookup"><span data-stu-id="d59c0-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="d59c0-109">Esse comando cria uma porta de front-end chamada FrontEndPort01 na porta 80 e armazena o resultado na variável chamada $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="d59c0-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="d59c0-110">OS</span><span class="sxs-lookup"><span data-stu-id="d59c0-110">PARAMETERS</span></span>

### <span data-ttu-id="d59c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59c0-111">-DefaultProfile</span></span>
<span data-ttu-id="d59c0-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d59c0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d59c0-113">-Name</span></span>
<span data-ttu-id="d59c0-114">Especifica o nome da porta de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d59c0-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c0-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="d59c0-115">-Port</span></span>
<span data-ttu-id="d59c0-116">Especifica o número da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="d59c0-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d59c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59c0-117">CommonParameters</span></span>
<span data-ttu-id="d59c0-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59c0-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d59c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59c0-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d59c0-120">INPUTS</span></span>

### <span data-ttu-id="d59c0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d59c0-121">System.String</span></span>

## <span data-ttu-id="d59c0-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d59c0-122">OUTPUTS</span></span>

### <span data-ttu-id="d59c0-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="d59c0-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d59c0-124">NOTES</span></span>

## <span data-ttu-id="d59c0-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d59c0-125">RELATED LINKS</span></span>

[<span data-ttu-id="d59c0-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d59c0-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d59c0-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="d59c0-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="d59c0-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


