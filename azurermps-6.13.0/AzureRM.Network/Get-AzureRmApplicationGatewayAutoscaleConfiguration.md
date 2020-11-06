---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f9be647a4c6cb9d5198edcc766a20b3588e7626b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428077"
---
# <span data-ttu-id="1d335-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d335-101">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="1d335-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1d335-102">SYNOPSIS</span></span>
<span data-ttu-id="1d335-103">Obtém a configuração de autoescala do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1d335-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d335-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d335-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d335-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1d335-105">DESCRIPTION</span></span>
<span data-ttu-id="1d335-106">O cmdlet **Get-AzureRmApplicationGatewayAutoscaleConfiguration** Obtém a configuração de autoescala do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1d335-106">The **Get-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="1d335-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1d335-107">EXAMPLES</span></span>

### <span data-ttu-id="1d335-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1d335-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="1d335-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="1d335-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="1d335-110">O segundo comando extrai a configuração de autoescala do gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="1d335-110">The second command extracts out the autoscale configuration from the applicationg gateway.</span></span>

## <span data-ttu-id="1d335-111">OS</span><span class="sxs-lookup"><span data-stu-id="1d335-111">PARAMETERS</span></span>

### <span data-ttu-id="1d335-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d335-112">-ApplicationGateway</span></span>
<span data-ttu-id="1d335-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d335-113">The applicationGateway</span></span>

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

### <span data-ttu-id="1d335-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d335-114">-DefaultProfile</span></span>
<span data-ttu-id="1d335-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1d335-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d335-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d335-116">CommonParameters</span></span>
<span data-ttu-id="1d335-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d335-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d335-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d335-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d335-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1d335-119">INPUTS</span></span>

### <span data-ttu-id="1d335-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1d335-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1d335-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1d335-121">OUTPUTS</span></span>

### <span data-ttu-id="1d335-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d335-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="1d335-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1d335-123">NOTES</span></span>

## <span data-ttu-id="1d335-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1d335-124">RELATED LINKS</span></span>
