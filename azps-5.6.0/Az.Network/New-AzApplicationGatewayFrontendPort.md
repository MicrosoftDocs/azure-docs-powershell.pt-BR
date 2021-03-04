---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885629"
---
# <span data-ttu-id="24f85-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="24f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f85-102">SYNOPSIS</span></span>
<span data-ttu-id="24f85-103">Cria uma porta front-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="24f85-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="24f85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24f85-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24f85-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24f85-105">DESCRIPTION</span></span>
<span data-ttu-id="24f85-106">O cmdlet **New-AzApplicationGatewayFrontendPort** cria uma porta front-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="24f85-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="24f85-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24f85-107">EXAMPLES</span></span>

### <span data-ttu-id="24f85-108">Exemplo 1: Exemplo1: Criar uma porta front-end</span><span class="sxs-lookup"><span data-stu-id="24f85-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="24f85-109">Este comando cria uma porta front-end chamada FrontEndPort01 na porta 80 e armazena o resultado na variável chamada $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="24f85-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="24f85-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24f85-110">PARAMETERS</span></span>

### <span data-ttu-id="24f85-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f85-111">-DefaultProfile</span></span>
<span data-ttu-id="24f85-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="24f85-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24f85-113">-Name</span><span class="sxs-lookup"><span data-stu-id="24f85-113">-Name</span></span>
<span data-ttu-id="24f85-114">Especifica o nome da porta front-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="24f85-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="24f85-115">-Port</span><span class="sxs-lookup"><span data-stu-id="24f85-115">-Port</span></span>
<span data-ttu-id="24f85-116">Especifica o número da porta front-end.</span><span class="sxs-lookup"><span data-stu-id="24f85-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="24f85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f85-117">CommonParameters</span></span>
<span data-ttu-id="24f85-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24f85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f85-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24f85-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f85-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24f85-120">INPUTS</span></span>

### <span data-ttu-id="24f85-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="24f85-121">None</span></span>

## <span data-ttu-id="24f85-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24f85-122">OUTPUTS</span></span>

### <span data-ttu-id="24f85-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="24f85-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="24f85-124">NOTES</span></span>

## <span data-ttu-id="24f85-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24f85-125">RELATED LINKS</span></span>

[<span data-ttu-id="24f85-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="24f85-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="24f85-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="24f85-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="24f85-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


