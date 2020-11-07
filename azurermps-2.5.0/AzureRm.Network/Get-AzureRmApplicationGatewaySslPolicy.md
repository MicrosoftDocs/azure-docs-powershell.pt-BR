---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF02FFF8-F00D-4446-968F-F3C9008C39F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 237df37605581adeeb45fdfbb7bae6449128aa7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786471"
---
# <span data-ttu-id="514e1-101">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="514e1-101">Get-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="514e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="514e1-102">SYNOPSIS</span></span>
<span data-ttu-id="514e1-103">Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="514e1-103">Gets the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="514e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="514e1-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="514e1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="514e1-105">DESCRIPTION</span></span>
<span data-ttu-id="514e1-106">O cmdlet **Get-AzureRmApplicationGatewaySslPolicy** Obtém a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="514e1-106">The **Get-AzureRmApplicationGatewaySslPolicy** cmdlet gets the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="514e1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="514e1-107">EXAMPLES</span></span>

### <span data-ttu-id="514e1-108">1:</span><span class="sxs-lookup"><span data-stu-id="514e1-108">1:</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $sslpolicy = Get-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="514e1-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="514e1-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="514e1-110">O segundo comando obtém a política SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="514e1-110">The second command gets the ssl policy from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="514e1-111">OS</span><span class="sxs-lookup"><span data-stu-id="514e1-111">PARAMETERS</span></span>

### <span data-ttu-id="514e1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="514e1-112">-ApplicationGateway</span></span>
<span data-ttu-id="514e1-113">Especifica o gateway de aplicativo da política SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="514e1-113">Specifies the application gateway of the SSL policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="514e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="514e1-114">-DefaultProfile</span></span>
<span data-ttu-id="514e1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="514e1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="514e1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514e1-116">CommonParameters</span></span>
<span data-ttu-id="514e1-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514e1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514e1-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514e1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514e1-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="514e1-119">INPUTS</span></span>

### <span data-ttu-id="514e1-120">System. String</span><span class="sxs-lookup"><span data-stu-id="514e1-120">System.String</span></span>

## <span data-ttu-id="514e1-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="514e1-121">OUTPUTS</span></span>

### <span data-ttu-id="514e1-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="514e1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="514e1-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="514e1-123">NOTES</span></span>
* <span data-ttu-id="514e1-124">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="514e1-124">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="514e1-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="514e1-125">RELATED LINKS</span></span>

[<span data-ttu-id="514e1-126">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="514e1-126">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="514e1-127">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="514e1-127">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


