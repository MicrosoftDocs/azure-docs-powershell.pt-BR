---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: cf9e847454fc638afc3c25cc3b5d8f0e78ef2fb0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111564"
---
# <span data-ttu-id="c0956-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0956-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="c0956-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0956-102">SYNOPSIS</span></span>
<span data-ttu-id="c0956-103">Atualiza a Configuração de Escala Automática de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0956-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="c0956-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0956-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0956-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0956-105">DESCRIPTION</span></span>
<span data-ttu-id="c0956-106">O cmdlet **Set-AzApplicationGatewayAutoscaleConfiguration** modifica a configuração de escala automática existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0956-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="c0956-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0956-107">EXAMPLES</span></span>

### <span data-ttu-id="c0956-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0956-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c0956-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="c0956-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="c0956-110">O segundo comando atualiza a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0956-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="c0956-111">O terceiro comando atualiza o gateway do aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="c0956-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c0956-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0956-112">PARAMETERS</span></span>

### <span data-ttu-id="c0956-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0956-113">-ApplicationGateway</span></span>
<span data-ttu-id="c0956-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0956-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c0956-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0956-115">-DefaultProfile</span></span>
<span data-ttu-id="c0956-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0956-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0956-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="c0956-117">-MaxCapacity</span></span>
<span data-ttu-id="c0956-118">Capacidade máxima para gateway de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0956-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="c0956-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="c0956-119">-MinCapacity</span></span>
<span data-ttu-id="c0956-120">Capacidade mínima para gateway de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0956-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="c0956-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c0956-121">-Confirm</span></span>
<span data-ttu-id="c0956-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0956-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0956-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0956-123">-WhatIf</span></span>
<span data-ttu-id="c0956-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c0956-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0956-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0956-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0956-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0956-126">CommonParameters</span></span>
<span data-ttu-id="c0956-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0956-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0956-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0956-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0956-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="c0956-129">INPUTS</span></span>

### <span data-ttu-id="c0956-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0956-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0956-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="c0956-131">OUTPUTS</span></span>

### <span data-ttu-id="c0956-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c0956-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c0956-133">Notas</span><span class="sxs-lookup"><span data-stu-id="c0956-133">NOTES</span></span>

## <span data-ttu-id="c0956-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0956-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0956-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0956-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c0956-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0956-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="c0956-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0956-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)
