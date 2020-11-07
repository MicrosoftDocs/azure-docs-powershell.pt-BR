---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 98f824ec0d874f8977c6e29f51358856cb5d1ca1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775570"
---
# <span data-ttu-id="53957-101">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="53957-101">Get-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="53957-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53957-102">SYNOPSIS</span></span>
<span data-ttu-id="53957-103">Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53957-103">Gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="53957-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53957-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53957-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53957-105">DESCRIPTION</span></span>
<span data-ttu-id="53957-106">O cmdlet **Get-AzApplicationGatewaySslPolicy** Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53957-106">The **Get-AzApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="53957-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53957-107">EXAMPLES</span></span>

### <span data-ttu-id="53957-108">1:</span><span class="sxs-lookup"><span data-stu-id="53957-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="53957-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="53957-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="53957-110">O segundo comando obtém a política SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="53957-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="53957-111">OS</span><span class="sxs-lookup"><span data-stu-id="53957-111">PARAMETERS</span></span>

### <span data-ttu-id="53957-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53957-112">-ApplicationGateway</span></span>
<span data-ttu-id="53957-113">Especifica o gateway de aplicativo da política SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="53957-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="53957-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53957-114">-DefaultProfile</span></span>
<span data-ttu-id="53957-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53957-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53957-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53957-116">CommonParameters</span></span>
<span data-ttu-id="53957-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53957-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53957-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53957-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53957-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53957-119">INPUTS</span></span>

### <span data-ttu-id="53957-120">System. String</span><span class="sxs-lookup"><span data-stu-id="53957-120">System.String</span></span>

## <span data-ttu-id="53957-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53957-121">OUTPUTS</span></span>

### <span data-ttu-id="53957-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="53957-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="53957-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53957-123">NOTES</span></span>
* <span data-ttu-id="53957-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="53957-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="53957-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53957-125">RELATED LINKS</span></span>

[<span data-ttu-id="53957-126">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="53957-126">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="53957-127">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="53957-127">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


