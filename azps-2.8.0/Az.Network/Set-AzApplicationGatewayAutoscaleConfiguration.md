---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: ad8795016fc10212a885267d23a61ddc7224c906
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772231"
---
# <span data-ttu-id="5f144-101">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f144-101">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="5f144-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f144-102">SYNOPSIS</span></span>
<span data-ttu-id="5f144-103">Atualiza a configuração de autoescala de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f144-103">Updates Autoscale Configuration of an application gateway.</span></span>

## <span data-ttu-id="5f144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f144-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> -MinCapacity <Int32>
 [-MaxCapacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f144-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f144-105">DESCRIPTION</span></span>
<span data-ttu-id="5f144-106">O cmdlet **set-AzApplicationGatewayAutoscaleConfiguration** modifica a configuração de autoescala existente de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f144-106">The **Set-AzApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="5f144-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f144-107">EXAMPLES</span></span>

### <span data-ttu-id="5f144-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5f144-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="5f144-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="5f144-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="5f144-110">O segundo comando atualiza a configuração de autoescala do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f144-110">The second command updates the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="5f144-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="5f144-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="5f144-112">OS</span><span class="sxs-lookup"><span data-stu-id="5f144-112">PARAMETERS</span></span>

### <span data-ttu-id="5f144-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f144-113">-ApplicationGateway</span></span>
<span data-ttu-id="5f144-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f144-114">The applicationGateway</span></span>

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

### <span data-ttu-id="5f144-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f144-115">-DefaultProfile</span></span>
<span data-ttu-id="5f144-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f144-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f144-117">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="5f144-117">-MaxCapacity</span></span>
<span data-ttu-id="5f144-118">Capacidade máxima do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="5f144-118">Maximum capacity for application gateway.</span></span>

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

### <span data-ttu-id="5f144-119">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="5f144-119">-MinCapacity</span></span>
<span data-ttu-id="5f144-120">Capacidade mínima para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5f144-120">Minimum capacity for application gateway.</span></span>

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

### <span data-ttu-id="5f144-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5f144-121">-Confirm</span></span>
<span data-ttu-id="5f144-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f144-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f144-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f144-123">-WhatIf</span></span>
<span data-ttu-id="5f144-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5f144-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f144-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5f144-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f144-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f144-126">CommonParameters</span></span>
<span data-ttu-id="5f144-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f144-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f144-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f144-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f144-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f144-129">INPUTS</span></span>

### <span data-ttu-id="5f144-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f144-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f144-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f144-131">OUTPUTS</span></span>

### <span data-ttu-id="5f144-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f144-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f144-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f144-133">NOTES</span></span>

## <span data-ttu-id="5f144-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f144-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f144-135">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f144-135">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5f144-136">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f144-136">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="5f144-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f144-137">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)