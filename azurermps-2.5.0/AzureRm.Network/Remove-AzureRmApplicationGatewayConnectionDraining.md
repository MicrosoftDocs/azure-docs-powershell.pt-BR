---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
ms.openlocfilehash: 751e27600d81a24005ea0a9200d3efa1d1647597
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786430"
---
# <span data-ttu-id="0490c-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0490c-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="0490c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0490c-102">SYNOPSIS</span></span>
<span data-ttu-id="0490c-103">Remove a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="0490c-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0490c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0490c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0490c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0490c-105">DESCRIPTION</span></span>
<span data-ttu-id="0490c-106">O cmdlet **Remove-AzureRmApplicationGatewayConnectionDraining** remove a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="0490c-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="0490c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0490c-107">EXAMPLES</span></span>

### <span data-ttu-id="0490c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0490c-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="0490c-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0490c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0490c-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="0490c-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="0490c-111">O último comando Remove a conexão que descarrega a configuração das configurações HTTP de back-end armazenadas em $Settings.</span><span class="sxs-lookup"><span data-stu-id="0490c-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="0490c-112">OS</span><span class="sxs-lookup"><span data-stu-id="0490c-112">PARAMETERS</span></span>

### <span data-ttu-id="0490c-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0490c-113">-BackendHttpSettings</span></span>
<span data-ttu-id="0490c-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="0490c-114">The backend http settings</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0490c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0490c-115">-DefaultProfile</span></span>
<span data-ttu-id="0490c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0490c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0490c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0490c-117">CommonParameters</span></span>
<span data-ttu-id="0490c-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0490c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0490c-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0490c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0490c-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0490c-120">INPUTS</span></span>

### <span data-ttu-id="0490c-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0490c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0490c-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0490c-122">OUTPUTS</span></span>

### <span data-ttu-id="0490c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0490c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0490c-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0490c-124">NOTES</span></span>

## <span data-ttu-id="0490c-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0490c-125">RELATED LINKS</span></span>

[<span data-ttu-id="0490c-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0490c-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="0490c-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0490c-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="0490c-128">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0490c-128">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0490c-129">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0490c-129">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="0490c-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="0490c-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

