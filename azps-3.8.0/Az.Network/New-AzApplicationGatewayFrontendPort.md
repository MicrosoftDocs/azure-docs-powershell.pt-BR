---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 3770b17a2bee9509f2b69d0e29c146b0b84ced8e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944800"
---
# <span data-ttu-id="f7ed5-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f7ed5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ed5-103">Cria uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f7ed5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7ed5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ed5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ed5-106">O cmdlet **New-AzApplicationGatewayFrontendPort** cria uma porta de front-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="f7ed5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ed5-108">Example1: criar uma porta de front-end</span><span class="sxs-lookup"><span data-stu-id="f7ed5-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f7ed5-109">Esse comando cria uma porta de front-end chamada FrontEndPort01 na porta 80 e armazena o resultado na variável chamada $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="f7ed5-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="f7ed5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ed5-111">-DefaultProfile</span></span>
<span data-ttu-id="f7ed5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7ed5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7ed5-113">-Name</span></span>
<span data-ttu-id="f7ed5-114">Especifica o nome da porta de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ed5-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="f7ed5-115">-Port</span></span>
<span data-ttu-id="f7ed5-116">Especifica o número da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7ed5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ed5-117">CommonParameters</span></span>
<span data-ttu-id="f7ed5-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ed5-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7ed5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ed5-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7ed5-120">INPUTS</span></span>

### <span data-ttu-id="f7ed5-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f7ed5-121">None</span></span>

## <span data-ttu-id="f7ed5-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7ed5-122">OUTPUTS</span></span>

### <span data-ttu-id="f7ed5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f7ed5-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7ed5-124">NOTES</span></span>

## <span data-ttu-id="f7ed5-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7ed5-125">RELATED LINKS</span></span>

[<span data-ttu-id="f7ed5-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7ed5-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7ed5-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7ed5-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7ed5-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


