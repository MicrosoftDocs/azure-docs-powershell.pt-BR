---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 823b4ce458e4308965b4c5bea1ad5739708f7aff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440849"
---
# <span data-ttu-id="cab14-101">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cab14-101">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="cab14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cab14-102">SYNOPSIS</span></span>
<span data-ttu-id="cab14-103">Remove uma configuração de IP de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="cab14-103">Removes an IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cab14-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab14-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cab14-105">DESCRIPTION</span></span>
<span data-ttu-id="cab14-106">O cmdlet **Remove-AzureRmApplicationGatewayIPConfiguration** remove uma configuração de IP de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="cab14-106">The **Remove-AzureRmApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="cab14-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cab14-107">EXAMPLES</span></span>

### <span data-ttu-id="cab14-108">Exemplo 1: remover uma configuração de IP de um gateway do aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="cab14-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="cab14-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cab14-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cab14-110">O segundo comando Remove a configuração de IP denominada Subnet02 do gateway do aplicativo armazenado em $AppGw.</span><span class="sxs-lookup"><span data-stu-id="cab14-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="cab14-111">OS</span><span class="sxs-lookup"><span data-stu-id="cab14-111">PARAMETERS</span></span>

### <span data-ttu-id="cab14-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cab14-112">-ApplicationGateway</span></span>
<span data-ttu-id="cab14-113">Especifica o gateway do aplicativo do qual remover uma configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="cab14-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="cab14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab14-114">-DefaultProfile</span></span>
<span data-ttu-id="cab14-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cab14-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab14-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="cab14-116">-Name</span></span>
<span data-ttu-id="cab14-117">Especifica o nome da configuração de IP a ser removida.</span><span class="sxs-lookup"><span data-stu-id="cab14-117">Specifies the name of the IP configuration to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab14-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab14-118">CommonParameters</span></span>
<span data-ttu-id="cab14-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab14-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab14-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab14-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab14-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cab14-121">INPUTS</span></span>

### <span data-ttu-id="cab14-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cab14-122">System.String</span></span>

## <span data-ttu-id="cab14-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cab14-123">OUTPUTS</span></span>

### <span data-ttu-id="cab14-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cab14-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cab14-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cab14-125">NOTES</span></span>

## <span data-ttu-id="cab14-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cab14-126">RELATED LINKS</span></span>

[<span data-ttu-id="cab14-127">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cab14-127">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cab14-128">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cab14-128">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cab14-129">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cab14-129">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="cab14-130">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="cab14-130">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)

