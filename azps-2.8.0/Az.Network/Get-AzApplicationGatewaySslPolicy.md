---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 6f93a66739fe1943182726e6998267d1e406f0a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772048"
---
# <span data-ttu-id="b5bae-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bae-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="b5bae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5bae-102">SYNOPSIS</span></span>
<span data-ttu-id="b5bae-103">Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b5bae-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="b5bae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5bae-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5bae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b5bae-105">DESCRIPTION</span></span>
<span data-ttu-id="b5bae-106">O cmdlet **Get-AzApplicationGatewaySslPolicy** Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b5bae-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="b5bae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5bae-107">EXAMPLES</span></span>

### <span data-ttu-id="b5bae-108">1:</span><span class="sxs-lookup"><span data-stu-id="b5bae-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="b5bae-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b5bae-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="b5bae-110">O segundo comando obtém a política SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="b5bae-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="b5bae-111">OS</span><span class="sxs-lookup"><span data-stu-id="b5bae-111">PARAMETERS</span></span>

### <span data-ttu-id="b5bae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5bae-112">-ApplicationGateway</span></span>
<span data-ttu-id="b5bae-113">Especifica o gateway de aplicativo da política SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b5bae-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b5bae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5bae-114">-DefaultProfile</span></span>
<span data-ttu-id="b5bae-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5bae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5bae-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5bae-116">CommonParameters</span></span>
<span data-ttu-id="b5bae-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5bae-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5bae-118">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5bae-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5bae-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b5bae-119">INPUTS</span></span>

### <span data-ttu-id="b5bae-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5bae-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5bae-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b5bae-121">OUTPUTS</span></span>

### <span data-ttu-id="b5bae-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bae-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="b5bae-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b5bae-123">NOTES</span></span>
* <span data-ttu-id="b5bae-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b5bae-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b5bae-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5bae-125">RELATED LINKS</span></span>

[<span data-ttu-id="b5bae-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bae-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="b5bae-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="b5bae-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


