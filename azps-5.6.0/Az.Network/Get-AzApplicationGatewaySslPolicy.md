---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4e15a4296a405a7f0f1e9ac918a5a806603203da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890814"
---
# <span data-ttu-id="abe3c-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="abe3c-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="abe3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="abe3c-103">Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="abe3c-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="abe3c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="abe3c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abe3c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="abe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="abe3c-106">O cmdlet **Get-AzApplicationGatewaySslPolicy** obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="abe3c-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="abe3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abe3c-107">EXAMPLES</span></span>

### <span data-ttu-id="abe3c-108">1:</span><span class="sxs-lookup"><span data-stu-id="abe3c-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="abe3c-109">O primeiro comando obtém o Gateway de Aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="abe3c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="abe3c-110">O segundo comando obtém a política ssl do Gateway de Aplicativo armazenada na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="abe3c-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="abe3c-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="abe3c-111">PARAMETERS</span></span>

### <span data-ttu-id="abe3c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abe3c-112">-ApplicationGateway</span></span>
<span data-ttu-id="abe3c-113">Especifica o gateway de aplicativo da política SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="abe3c-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="abe3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abe3c-114">-DefaultProfile</span></span>
<span data-ttu-id="abe3c-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="abe3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abe3c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abe3c-116">CommonParameters</span></span>
<span data-ttu-id="abe3c-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abe3c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abe3c-118">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abe3c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abe3c-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abe3c-119">INPUTS</span></span>

### <span data-ttu-id="abe3c-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="abe3c-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="abe3c-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="abe3c-121">OUTPUTS</span></span>

### <span data-ttu-id="abe3c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="abe3c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="abe3c-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="abe3c-123">NOTES</span></span>
* <span data-ttu-id="abe3c-124">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="abe3c-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="abe3c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abe3c-125">RELATED LINKS</span></span>

[<span data-ttu-id="abe3c-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="abe3c-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="abe3c-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="abe3c-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


