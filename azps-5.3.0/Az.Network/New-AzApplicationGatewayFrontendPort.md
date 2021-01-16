---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272657"
---
# <span data-ttu-id="6e0d9-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6e0d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e0d9-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0d9-103">Cria uma porta de front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="6e0d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e0d9-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e0d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e0d9-105">DESCRIPTION</span></span>
<span data-ttu-id="6e0d9-106">O cmdlet **New-AzApplicationGatewayFrontendPort** cria uma porta de front-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="6e0d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e0d9-107">EXAMPLES</span></span>

### <span data-ttu-id="6e0d9-108">Exemplo 1: example1: criar uma porta de front-end</span><span class="sxs-lookup"><span data-stu-id="6e0d9-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="6e0d9-109">Esse comando cria uma porta de front-end chamada FrontEndPort01 na porta 80 e armazena o resultado na variável chamada $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="6e0d9-110">OS</span><span class="sxs-lookup"><span data-stu-id="6e0d9-110">PARAMETERS</span></span>

### <span data-ttu-id="6e0d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0d9-111">-DefaultProfile</span></span>
<span data-ttu-id="6e0d9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e0d9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e0d9-113">-Name</span></span>
<span data-ttu-id="6e0d9-114">Especifica o nome da porta de front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6e0d9-115">-Porta</span><span class="sxs-lookup"><span data-stu-id="6e0d9-115">-Port</span></span>
<span data-ttu-id="6e0d9-116">Especifica o número da porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="6e0d9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0d9-117">CommonParameters</span></span>
<span data-ttu-id="6e0d9-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0d9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0d9-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e0d9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0d9-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e0d9-120">INPUTS</span></span>

### <span data-ttu-id="6e0d9-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6e0d9-121">None</span></span>

## <span data-ttu-id="6e0d9-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e0d9-122">OUTPUTS</span></span>

### <span data-ttu-id="6e0d9-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6e0d9-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e0d9-124">NOTES</span></span>

## <span data-ttu-id="6e0d9-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e0d9-125">RELATED LINKS</span></span>

[<span data-ttu-id="6e0d9-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6e0d9-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6e0d9-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6e0d9-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6e0d9-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


