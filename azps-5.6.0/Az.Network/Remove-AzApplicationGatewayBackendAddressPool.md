---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 202801e39e62b265b39036793ed4369a5d98bf2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892741"
---
# <span data-ttu-id="7c616-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7c616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c616-102">SYNOPSIS</span></span>
<span data-ttu-id="7c616-103">Remove um pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c616-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="7c616-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c616-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c616-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c616-105">DESCRIPTION</span></span>
<span data-ttu-id="7c616-106">O cmdlet **Remove-AzApplicationGatewayBackendAddressPool** remove um pool de endereços back-end de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c616-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="7c616-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c616-107">EXAMPLES</span></span>

### <span data-ttu-id="7c616-108">Exemplo 1: Remover um pool de endereços back-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7c616-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="7c616-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 pertencente ao grupo de recursos chamado ResourceGroup01 e o salva na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7c616-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="7c616-110">O segundo comando remove o pool de endereços back-end chamado BackEndPool02 do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7c616-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="7c616-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c616-111">PARAMETERS</span></span>

### <span data-ttu-id="7c616-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c616-112">-ApplicationGateway</span></span>
<span data-ttu-id="7c616-113">Especifica o gateway de aplicativo do qual esse cmdlet remove um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="7c616-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="7c616-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c616-114">-DefaultProfile</span></span>
<span data-ttu-id="7c616-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7c616-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c616-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7c616-116">-Name</span></span>
<span data-ttu-id="7c616-117">Especifica o nome do pool de endereços back-end que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="7c616-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7c616-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c616-118">-Confirm</span></span>
<span data-ttu-id="7c616-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c616-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c616-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c616-120">-WhatIf</span></span>
<span data-ttu-id="7c616-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c616-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c616-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c616-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c616-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c616-123">CommonParameters</span></span>
<span data-ttu-id="7c616-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c616-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c616-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c616-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c616-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c616-126">INPUTS</span></span>

### <span data-ttu-id="7c616-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c616-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7c616-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c616-128">OUTPUTS</span></span>

### <span data-ttu-id="7c616-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7c616-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c616-130">NOTES</span></span>

## <span data-ttu-id="7c616-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c616-131">RELATED LINKS</span></span>

[<span data-ttu-id="7c616-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7c616-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7c616-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7c616-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7c616-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


