---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 884ff52132af34dad7c4498653233f0b122555ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440352"
---
# <span data-ttu-id="073ca-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="073ca-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="073ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="073ca-102">SYNOPSIS</span></span>
<span data-ttu-id="073ca-103">Remove uma configuração de IP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="073ca-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="073ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="073ca-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="073ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="073ca-105">DESCRIPTION</span></span>
<span data-ttu-id="073ca-106">O cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** remove uma configuração de IP de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="073ca-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="073ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="073ca-107">EXAMPLES</span></span>

### <span data-ttu-id="073ca-108">Exemplo 1: remover uma configuração de IP de um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="073ca-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="073ca-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="073ca-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="073ca-110">O segundo comando Remove a configuração de IP denominada Subnet02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="073ca-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="073ca-111">OS</span><span class="sxs-lookup"><span data-stu-id="073ca-111">PARAMETERS</span></span>

### <span data-ttu-id="073ca-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="073ca-112">-ApplicationGateway</span></span>
<span data-ttu-id="073ca-113">Especifica o gateway do aplicativo do qual remover uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="073ca-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="073ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073ca-114">-DefaultProfile</span></span>
<span data-ttu-id="073ca-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="073ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="073ca-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="073ca-116">-Name</span></span>
<span data-ttu-id="073ca-117">Especifica o nome da configuração de IP a ser removida.</span><span class="sxs-lookup"><span data-stu-id="073ca-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="073ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073ca-118">CommonParameters</span></span>
<span data-ttu-id="073ca-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="073ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073ca-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="073ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073ca-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="073ca-121">INPUTS</span></span>

### <span data-ttu-id="073ca-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="073ca-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="073ca-123">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="073ca-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="073ca-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="073ca-124">OUTPUTS</span></span>

### <span data-ttu-id="073ca-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="073ca-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="073ca-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="073ca-126">NOTES</span></span>

## <span data-ttu-id="073ca-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="073ca-127">RELATED LINKS</span></span>

[<span data-ttu-id="073ca-128">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="073ca-128">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="073ca-129">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="073ca-129">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="073ca-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="073ca-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="073ca-131">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="073ca-131">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


