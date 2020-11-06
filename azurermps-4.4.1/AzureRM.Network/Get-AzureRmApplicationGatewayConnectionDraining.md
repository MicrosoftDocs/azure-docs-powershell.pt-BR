---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 78c3a151f066d8ff05e92798ebad822943816af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427871"
---
# <span data-ttu-id="7ac76-101">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7ac76-101">Get-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7ac76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ac76-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac76-103">Obtém a conexão que descarrega a configuração de um objeto de configurações HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="7ac76-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ac76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ac76-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ac76-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ac76-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac76-106">O cmdlet **Get-AzureRmApplicationGatewayConnectionDraining** Obtém a configuração de descarga da configuração de um objeto de configurações http back-end.</span><span class="sxs-lookup"><span data-stu-id="7ac76-106">The **Get-AzureRmApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7ac76-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ac76-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac76-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ac76-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="7ac76-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7ac76-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7ac76-110">O segundo comando obtém as configurações HTTP back-end chamadas Settings01 para $AppGw e armazena as configurações na variável $Settings.</span><span class="sxs-lookup"><span data-stu-id="7ac76-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="7ac76-111">O último comando obtém a conexão que descarrega a configuração das configurações HTTP back-end $Settings e a armazena na variável $ConnectionDraining.</span><span class="sxs-lookup"><span data-stu-id="7ac76-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="7ac76-112">OS</span><span class="sxs-lookup"><span data-stu-id="7ac76-112">PARAMETERS</span></span>

### <span data-ttu-id="7ac76-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7ac76-113">-BackendHttpSettings</span></span>
<span data-ttu-id="7ac76-114">As configurações http de back-end</span><span class="sxs-lookup"><span data-stu-id="7ac76-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac76-115">-DefaultProfile</span></span>
<span data-ttu-id="7ac76-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ac76-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac76-117">CommonParameters</span></span>
<span data-ttu-id="7ac76-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac76-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac76-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac76-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac76-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ac76-120">INPUTS</span></span>

### <span data-ttu-id="7ac76-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7ac76-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7ac76-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ac76-122">OUTPUTS</span></span>

### <span data-ttu-id="7ac76-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7ac76-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7ac76-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ac76-124">NOTES</span></span>

## <span data-ttu-id="7ac76-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ac76-125">RELATED LINKS</span></span>

[<span data-ttu-id="7ac76-126">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7ac76-126">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="7ac76-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7ac76-127">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="7ac76-128">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7ac76-128">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7ac76-129">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7ac76-129">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7ac76-130">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7ac76-130">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)