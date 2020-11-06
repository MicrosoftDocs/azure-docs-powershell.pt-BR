---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 996a2c17b6283e967eaca8462f4d703aed60d19c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429458"
---
# <span data-ttu-id="34756-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-101">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="34756-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34756-102">SYNOPSIS</span></span>
<span data-ttu-id="34756-103">Remove um pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34756-103">Removes a back-end address pool from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34756-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34756-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34756-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34756-105">DESCRIPTION</span></span>
<span data-ttu-id="34756-106">O cmdlet **Remove-AzureRmApplicationGatewayBackendAddressPool** remove um pool de endereços back-end de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="34756-106">The **Remove-AzureRmApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="34756-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34756-107">EXAMPLES</span></span>

### <span data-ttu-id="34756-108">Exemplo 1: remover um pool de endereços back-end de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="34756-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="34756-109">O primeiro comando obtém o gateway do aplicativo denominado ApplicationGateway01 pertencente ao grupo de recursos chamado ResourceGroup01 e salva-o na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="34756-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="34756-110">O segundo comando Remove o pool de endereços back-end chamado BackEndPool02 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34756-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="34756-111">OS</span><span class="sxs-lookup"><span data-stu-id="34756-111">PARAMETERS</span></span>

### <span data-ttu-id="34756-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34756-112">-ApplicationGateway</span></span>
<span data-ttu-id="34756-113">Especifica o Application Gateway do qual esse cmdlet Remove um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="34756-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="34756-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34756-114">-DefaultProfile</span></span>
<span data-ttu-id="34756-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34756-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34756-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="34756-116">-Name</span></span>
<span data-ttu-id="34756-117">Especifica o nome do pool de endereços back-end que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="34756-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34756-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34756-118">-Confirm</span></span>
<span data-ttu-id="34756-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34756-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34756-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34756-120">-WhatIf</span></span>
<span data-ttu-id="34756-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34756-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34756-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34756-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34756-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34756-123">CommonParameters</span></span>
<span data-ttu-id="34756-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34756-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34756-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34756-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34756-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34756-126">INPUTS</span></span>

### <span data-ttu-id="34756-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34756-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="34756-128">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34756-128">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="34756-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34756-129">OUTPUTS</span></span>

### <span data-ttu-id="34756-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="34756-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34756-131">NOTES</span></span>

## <span data-ttu-id="34756-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34756-132">RELATED LINKS</span></span>

[<span data-ttu-id="34756-133">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-133">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="34756-134">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-134">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="34756-135">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-135">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="34756-136">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="34756-136">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)

