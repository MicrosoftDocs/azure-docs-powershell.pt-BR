---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 25602712a792a1de7b79ce00baf5074ebb8177a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600231"
---
# <span data-ttu-id="0c665-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c665-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="0c665-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c665-102">SYNOPSIS</span></span>
<span data-ttu-id="0c665-103">Remove a configuração de autoescala de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="0c665-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="0c665-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c665-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c665-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c665-105">DESCRIPTION</span></span>
<span data-ttu-id="0c665-106">O cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** remove a configuração de autoescala de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="0c665-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="0c665-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c665-107">EXAMPLES</span></span>

### <span data-ttu-id="0c665-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c665-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="0c665-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="0c665-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="0c665-110">O segundo comando Remove a configuração de autoescala do gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="0c665-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="0c665-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="0c665-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="0c665-112">OS</span><span class="sxs-lookup"><span data-stu-id="0c665-112">PARAMETERS</span></span>

### <span data-ttu-id="0c665-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c665-113">-ApplicationGateway</span></span>
<span data-ttu-id="0c665-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c665-114">The applicationGateway</span></span>

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

### <span data-ttu-id="0c665-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c665-115">-DefaultProfile</span></span>
<span data-ttu-id="0c665-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c665-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c665-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0c665-117">-Force</span></span>
<span data-ttu-id="0c665-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="0c665-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0c665-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0c665-119">-Confirm</span></span>
<span data-ttu-id="0c665-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c665-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c665-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c665-121">-WhatIf</span></span>
<span data-ttu-id="0c665-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c665-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c665-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c665-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c665-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c665-124">CommonParameters</span></span>
<span data-ttu-id="0c665-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c665-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c665-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c665-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c665-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c665-127">INPUTS</span></span>

### <span data-ttu-id="0c665-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c665-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c665-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c665-129">OUTPUTS</span></span>

### <span data-ttu-id="0c665-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c665-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c665-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c665-131">NOTES</span></span>

## <span data-ttu-id="0c665-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c665-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c665-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c665-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0c665-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c665-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="0c665-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c665-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
