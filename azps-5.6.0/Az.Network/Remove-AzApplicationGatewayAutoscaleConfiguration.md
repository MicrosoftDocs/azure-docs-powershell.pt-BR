---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e6321125958b872d15f60bbe433819c4c6f1d7ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901453"
---
# <span data-ttu-id="3b822-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b822-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="3b822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b822-102">SYNOPSIS</span></span>
<span data-ttu-id="3b822-103">Remove a Configuração de Escala Automática de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b822-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="3b822-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3b822-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b822-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3b822-105">DESCRIPTION</span></span>
<span data-ttu-id="3b822-106">O cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** remove a Configuração de Escala Automática de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="3b822-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="3b822-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b822-107">EXAMPLES</span></span>

### <span data-ttu-id="3b822-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b822-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="3b822-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="3b822-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="3b822-110">O segundo comando remove a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b822-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="3b822-111">O terceiro comando atualiza o gateway de aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="3b822-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="3b822-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3b822-112">PARAMETERS</span></span>

### <span data-ttu-id="3b822-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b822-113">-ApplicationGateway</span></span>
<span data-ttu-id="3b822-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b822-114">The applicationGateway</span></span>

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

### <span data-ttu-id="3b822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b822-115">-DefaultProfile</span></span>
<span data-ttu-id="3b822-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b822-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b822-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3b822-117">-Force</span></span>
<span data-ttu-id="3b822-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="3b822-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3b822-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b822-119">-Confirm</span></span>
<span data-ttu-id="3b822-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b822-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b822-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b822-121">-WhatIf</span></span>
<span data-ttu-id="3b822-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b822-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b822-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b822-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b822-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b822-124">CommonParameters</span></span>
<span data-ttu-id="3b822-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b822-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b822-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b822-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b822-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b822-127">INPUTS</span></span>

### <span data-ttu-id="3b822-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b822-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b822-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3b822-129">OUTPUTS</span></span>

### <span data-ttu-id="3b822-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b822-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b822-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="3b822-131">NOTES</span></span>

## <span data-ttu-id="3b822-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b822-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b822-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b822-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="3b822-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b822-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="3b822-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3b822-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
