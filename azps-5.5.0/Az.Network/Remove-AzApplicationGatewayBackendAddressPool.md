---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F34C5D18-C505-4815-9DDB-C563E205515C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1ce5989516286d366e6363cbeeee8ebddc93edfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118297"
---
# <span data-ttu-id="18358-101">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-101">Remove-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="18358-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18358-102">SYNOPSIS</span></span>
<span data-ttu-id="18358-103">Remove um pool de endereços back-end de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18358-103">Removes a back-end address pool from an application gateway.</span></span>

## <span data-ttu-id="18358-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18358-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendAddressPool -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18358-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="18358-105">DESCRIPTION</span></span>
<span data-ttu-id="18358-106">O cmdlet **Remove-AzApplicationGatewayBackendAddressPool** remove um pool de endereços back-end de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="18358-106">The **Remove-AzApplicationGatewayBackendAddressPool** cmdlet removes a back-end address pool from an Azure application gateway.</span></span>

## <span data-ttu-id="18358-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18358-107">EXAMPLES</span></span>

### <span data-ttu-id="18358-108">Exemplo 1: Remover um pool de endereços back-end de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="18358-108">Example 1: Remove a back-end address pool from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "BackEndPool02"
```

<span data-ttu-id="18358-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 pertencente ao grupo de recursos chamado ResourceGroup01 e o salva na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="18358-109">The first command gets the application gateway named ApplicationGateway01 belonging to the resource group named ResourceGroup01 and saves it in the $AppGw variable.</span></span>
<span data-ttu-id="18358-110">O segundo comando remove o pool de endereços back-end chamado BackEndPool02 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18358-110">The second command removes the back-end address pool named BackEndPool02 from the application gateway.</span></span>

## <span data-ttu-id="18358-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18358-111">PARAMETERS</span></span>

### <span data-ttu-id="18358-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18358-112">-ApplicationGateway</span></span>
<span data-ttu-id="18358-113">Especifica o gateway do aplicativo do qual este cmdlet remove um pool de endereços back-end.</span><span class="sxs-lookup"><span data-stu-id="18358-113">Specifies the application gateway from which this cmdlet removes a back-end address pool.</span></span>

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

### <span data-ttu-id="18358-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18358-114">-DefaultProfile</span></span>
<span data-ttu-id="18358-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="18358-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18358-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="18358-116">-Name</span></span>
<span data-ttu-id="18358-117">Especifica o nome do pool de endereços back-end que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="18358-117">Specifies the name of the back-end address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="18358-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="18358-118">-Confirm</span></span>
<span data-ttu-id="18358-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18358-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18358-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18358-120">-WhatIf</span></span>
<span data-ttu-id="18358-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="18358-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18358-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18358-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18358-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18358-123">CommonParameters</span></span>
<span data-ttu-id="18358-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18358-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18358-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18358-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18358-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="18358-126">INPUTS</span></span>

### <span data-ttu-id="18358-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="18358-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="18358-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="18358-128">OUTPUTS</span></span>

### <span data-ttu-id="18358-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="18358-130">Notas</span><span class="sxs-lookup"><span data-stu-id="18358-130">NOTES</span></span>

## <span data-ttu-id="18358-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18358-131">RELATED LINKS</span></span>

[<span data-ttu-id="18358-132">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-132">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18358-133">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-133">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18358-134">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-134">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="18358-135">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="18358-135">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


