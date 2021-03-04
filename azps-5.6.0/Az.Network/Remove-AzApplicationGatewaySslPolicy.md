---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: e5ac68f10a75dff94313fa17830720466e82da5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890376"
---
# <span data-ttu-id="41686-101">Remove-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="41686-101">Remove-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="41686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41686-102">SYNOPSIS</span></span>
<span data-ttu-id="41686-103">Remove uma política SSL de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="41686-103">Removes an SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="41686-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41686-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41686-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41686-105">DESCRIPTION</span></span>
<span data-ttu-id="41686-106">O Remove-AzApplicationGatewaySslPolicy cmdlet remove a política SSL de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="41686-106">The Remove-AzApplicationGatewaySslPolicy cmdlet removes SSL policy from an Azure application gateway.</span></span>

## <span data-ttu-id="41686-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41686-107">EXAMPLES</span></span>

### <span data-ttu-id="41686-108">Exemplo 1: Remover uma política SSL de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="41686-108">Example 1: Remove an SSL policy from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

<span data-ttu-id="41686-109">Este comando remove a política SSL do gateway de aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="41686-109">This command removes the SSL policy from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="41686-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41686-110">PARAMETERS</span></span>

### <span data-ttu-id="41686-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41686-111">-ApplicationGateway</span></span>
<span data-ttu-id="41686-112">Especifica o gateway de aplicativo do qual este cmdlet remove a política SSL.</span><span class="sxs-lookup"><span data-stu-id="41686-112">Specifies the application gateway from which this cmdlet removes SSL policy.</span></span>

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

### <span data-ttu-id="41686-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41686-113">-DefaultProfile</span></span>
<span data-ttu-id="41686-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="41686-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41686-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41686-115">-Force</span></span>
<span data-ttu-id="41686-116">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="41686-116">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41686-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41686-117">-Confirm</span></span>
<span data-ttu-id="41686-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41686-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41686-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41686-119">-WhatIf</span></span>
<span data-ttu-id="41686-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41686-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41686-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41686-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41686-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41686-122">CommonParameters</span></span>
<span data-ttu-id="41686-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41686-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41686-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41686-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41686-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41686-125">INPUTS</span></span>

### <span data-ttu-id="41686-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41686-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41686-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41686-127">OUTPUTS</span></span>

### <span data-ttu-id="41686-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41686-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41686-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="41686-129">NOTES</span></span>
<span data-ttu-id="41686-130">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="41686-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="41686-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41686-131">RELATED LINKS</span></span>

[<span data-ttu-id="41686-132">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="41686-132">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="41686-133">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="41686-133">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="41686-134">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="41686-134">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

