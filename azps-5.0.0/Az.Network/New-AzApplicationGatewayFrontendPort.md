---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124510"
---
# <span data-ttu-id="6ff77-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6ff77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ff77-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff77-103">Cria uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6ff77-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="6ff77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ff77-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ff77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ff77-105">DESCRIPTION</span></span>
<span data-ttu-id="6ff77-106">O cmdlet **New-AzApplicationGatewayFrontendPort** cria uma porta de front-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff77-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="6ff77-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ff77-107">EXAMPLES</span></span>

### <span data-ttu-id="6ff77-108">Exemplo 1: example1: criar uma porta de front-end</span><span class="sxs-lookup"><span data-stu-id="6ff77-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="6ff77-109">Esse comando cria uma porta de front-end chamada FrontEndPort01 na porta 80 e armazena o resultado na variável chamada $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="6ff77-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="6ff77-110">OS</span><span class="sxs-lookup"><span data-stu-id="6ff77-110">PARAMETERS</span></span>

### <span data-ttu-id="6ff77-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff77-111">-DefaultProfile</span></span>
<span data-ttu-id="6ff77-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff77-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff77-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ff77-113">-Name</span></span>
<span data-ttu-id="6ff77-114">Especifica o nome da porta de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="6ff77-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6ff77-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="6ff77-115">-Port</span></span>
<span data-ttu-id="6ff77-116">Especifica o número da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="6ff77-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="6ff77-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff77-117">CommonParameters</span></span>
<span data-ttu-id="6ff77-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff77-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff77-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff77-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff77-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ff77-120">INPUTS</span></span>

### <span data-ttu-id="6ff77-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6ff77-121">None</span></span>

## <span data-ttu-id="6ff77-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ff77-122">OUTPUTS</span></span>

### <span data-ttu-id="6ff77-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6ff77-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ff77-124">NOTES</span></span>

## <span data-ttu-id="6ff77-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ff77-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ff77-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6ff77-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6ff77-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6ff77-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6ff77-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


