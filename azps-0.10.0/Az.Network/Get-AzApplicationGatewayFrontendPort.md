---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775588"
---
# <span data-ttu-id="eec26-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="eec26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eec26-102">SYNOPSIS</span></span>
<span data-ttu-id="eec26-103">Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eec26-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="eec26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eec26-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eec26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eec26-105">DESCRIPTION</span></span>
<span data-ttu-id="eec26-106">O cmdlet **Get-AzApplicationGatewayFrontendPort** Obtém a porta de front-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eec26-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="eec26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eec26-107">EXAMPLES</span></span>

### <span data-ttu-id="eec26-108">Exemplo 1: obter uma porta de front-end especificada</span><span class="sxs-lookup"><span data-stu-id="eec26-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="eec26-109">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="eec26-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eec26-110">O segundo comando obtém a porta de front-end chamada FrontEndPort01 da $AppGw e a armazena na variável $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="eec26-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="eec26-111">Exemplo 2: obter uma lista de portas de front-end</span><span class="sxs-lookup"><span data-stu-id="eec26-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="eec26-112">O primeiro comando obtém um gateway do aplicativo denominado ApplicationGateway01 do grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="eec26-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eec26-113">O segundo comando obtém uma lista das portas de front-end do $AppGw e a armazena na variável $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="eec26-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="eec26-114">OS</span><span class="sxs-lookup"><span data-stu-id="eec26-114">PARAMETERS</span></span>

### <span data-ttu-id="eec26-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eec26-115">-ApplicationGateway</span></span>
<span data-ttu-id="eec26-116">Especifica o objeto do gateway do aplicativo que contém a porta de front-end.</span><span class="sxs-lookup"><span data-stu-id="eec26-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="eec26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec26-117">-DefaultProfile</span></span>
<span data-ttu-id="eec26-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eec26-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eec26-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="eec26-119">-Name</span></span>
<span data-ttu-id="eec26-120">Especifica o nome da porta de front-end a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="eec26-120">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eec26-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec26-121">CommonParameters</span></span>
<span data-ttu-id="eec26-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eec26-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec26-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec26-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec26-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eec26-124">INPUTS</span></span>

### <span data-ttu-id="eec26-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eec26-125">System.String</span></span>

## <span data-ttu-id="eec26-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eec26-126">OUTPUTS</span></span>

### <span data-ttu-id="eec26-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="eec26-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eec26-128">NOTES</span></span>

## <span data-ttu-id="eec26-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eec26-129">RELATED LINKS</span></span>

[<span data-ttu-id="eec26-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="eec26-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="eec26-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="eec26-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eec26-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


