---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118291"
---
# <span data-ttu-id="ce8f5-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce8f5-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="ce8f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce8f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ce8f5-103">Remove uma configuração IP de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="ce8f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce8f5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce8f5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce8f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ce8f5-106">O cmdlet **Remove-AzApplicationGatewayIPConfiguration** remove uma configuração IP de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="ce8f5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce8f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ce8f5-108">Exemplo 1: Remover uma configuração IP de um gateway de aplicativo do Azure</span><span class="sxs-lookup"><span data-stu-id="ce8f5-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="ce8f5-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $AppGw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ce8f5-110">O segundo comando remove a configuração IP chamada Subnet02 do gateway de aplicativo armazenado no $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ce8f5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce8f5-111">PARAMETERS</span></span>

### <span data-ttu-id="ce8f5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce8f5-112">-ApplicationGateway</span></span>
<span data-ttu-id="ce8f5-113">Especifica o gateway de aplicativo do qual remover uma configuração IP.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="ce8f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce8f5-114">-DefaultProfile</span></span>
<span data-ttu-id="ce8f5-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce8f5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce8f5-116">-Name</span></span>
<span data-ttu-id="ce8f5-117">Especifica o nome da configuração IP a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="ce8f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce8f5-118">CommonParameters</span></span>
<span data-ttu-id="ce8f5-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce8f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce8f5-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce8f5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce8f5-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="ce8f5-121">INPUTS</span></span>

### <span data-ttu-id="ce8f5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce8f5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce8f5-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="ce8f5-123">OUTPUTS</span></span>

### <span data-ttu-id="ce8f5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ce8f5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ce8f5-125">Notas</span><span class="sxs-lookup"><span data-stu-id="ce8f5-125">NOTES</span></span>

## <span data-ttu-id="ce8f5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce8f5-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce8f5-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce8f5-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ce8f5-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce8f5-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ce8f5-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce8f5-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="ce8f5-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce8f5-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


