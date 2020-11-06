---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 29f9d1b13704f190a94bffaa70b900bc5a3b29e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433072"
---
# <span data-ttu-id="5ee48-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee48-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5ee48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ee48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee48-103">Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ee48-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ee48-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ee48-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee48-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ee48-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee48-106">O cmdlet **Get-AzureRmApplicationGatewaySslPolicy** Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ee48-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="5ee48-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ee48-107">EXAMPLES</span></span>

### <span data-ttu-id="5ee48-108">1:</span><span class="sxs-lookup"><span data-stu-id="5ee48-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="5ee48-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ee48-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ee48-110">O segundo comando obtém a política SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ee48-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="5ee48-111">OS</span><span class="sxs-lookup"><span data-stu-id="5ee48-111">PARAMETERS</span></span>

### <span data-ttu-id="5ee48-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ee48-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ee48-113">Especifica o gateway de aplicativo da política SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5ee48-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5ee48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee48-114">-DefaultProfile</span></span>
<span data-ttu-id="5ee48-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ee48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee48-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee48-116">CommonParameters</span></span>
<span data-ttu-id="5ee48-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee48-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee48-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee48-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee48-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ee48-119">INPUTS</span></span>

### <span data-ttu-id="5ee48-120">System. String</span><span class="sxs-lookup"><span data-stu-id="5ee48-120">System.String</span></span>

## <span data-ttu-id="5ee48-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ee48-121">OUTPUTS</span></span>

### <span data-ttu-id="5ee48-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee48-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="5ee48-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ee48-123">NOTES</span></span>
* <span data-ttu-id="5ee48-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="5ee48-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5ee48-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ee48-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ee48-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee48-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="5ee48-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="5ee48-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


