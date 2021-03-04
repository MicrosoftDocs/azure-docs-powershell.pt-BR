---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: bfa5cbfdb8ab734a8c6ca8b651808213b9b10f3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886150"
---
# <span data-ttu-id="6bc3c-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bc3c-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="6bc3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc3c-103">Atualiza a Configuração de Escala Automática de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="6bc3c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6bc3c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc3c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6bc3c-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc3c-106">O cmdlet **Set-AzApplicationGatewayAutoscaleConfiguration** modifica a configuração de escala automática existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="6bc3c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc3c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6bc3c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="6bc3c-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="6bc3c-110">O segundo comando atualiza a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="6bc3c-111">O terceiro comando atualiza o gateway de aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="6bc3c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-112">PARAMETERS</span></span>

### <span data-ttu-id="6bc3c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bc3c-113">-ApplicationGateway</span></span>
<span data-ttu-id="6bc3c-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bc3c-114">The applicationGateway</span></span>

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

### <span data-ttu-id="6bc3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc3c-115">-DefaultProfile</span></span>
<span data-ttu-id="6bc3c-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc3c-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="6bc3c-117">-MaxCapacity</span></span>
<span data-ttu-id="6bc3c-118">Capacidade máxima para gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-118">Maximum capacity for application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3c-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="6bc3c-119">-MinCapacity</span></span>
<span data-ttu-id="6bc3c-120">Capacidade mínima para gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-120">Minimum capacity for application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc3c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bc3c-121">-Confirm</span></span>
<span data-ttu-id="6bc3c-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc3c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc3c-123">-WhatIf</span></span>
<span data-ttu-id="6bc3c-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc3c-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc3c-126">CommonParameters</span></span>
<span data-ttu-id="6bc3c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc3c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc3c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc3c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-129">INPUTS</span></span>

### <span data-ttu-id="6bc3c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bc3c-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bc3c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-131">OUTPUTS</span></span>

### <span data-ttu-id="6bc3c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6bc3c-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6bc3c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="6bc3c-133">NOTES</span></span>

## <span data-ttu-id="6bc3c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bc3c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6bc3c-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bc3c-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6bc3c-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bc3c-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="6bc3c-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="6bc3c-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
