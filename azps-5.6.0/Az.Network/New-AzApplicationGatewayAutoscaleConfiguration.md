---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e849b109ba1f1fd43ca960d56581357729f5c344
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892947"
---
# <span data-ttu-id="4a1c0-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a1c0-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="4a1c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1c0-103">Cria uma Configuração de Escala Automática para o Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="4a1c0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4a1c0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1c0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4a1c0-105">DESCRIPTION</span></span>
<span data-ttu-id="4a1c0-106">O cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** cria a Configuração de Escala Automática para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="4a1c0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-107">EXAMPLES</span></span>

### <span data-ttu-id="4a1c0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4a1c0-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="4a1c0-109">O primeiro comando cria uma configuração de escala automática com capacidade mínima 3.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="4a1c0-110">O segundo comando cria um gateway de aplicativo com a configuração de escala automática.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="4a1c0-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-111">PARAMETERS</span></span>

### <span data-ttu-id="4a1c0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1c0-112">-DefaultProfile</span></span>
<span data-ttu-id="4a1c0-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a1c0-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="4a1c0-114">-MaxCapacity</span></span>
<span data-ttu-id="4a1c0-115">Unidades de capacidade máxima que sempre estarão disponíveis [e cobradas] para gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="4a1c0-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="4a1c0-116">-MinCapacity</span></span>
<span data-ttu-id="4a1c0-117">Unidades de capacidade mínima que sempre estarão disponíveis [e cobradas] para gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="4a1c0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a1c0-118">-Confirm</span></span>
<span data-ttu-id="4a1c0-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1c0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1c0-120">-WhatIf</span></span>
<span data-ttu-id="4a1c0-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a1c0-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1c0-123">CommonParameters</span></span>
<span data-ttu-id="4a1c0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a1c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1c0-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1c0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1c0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-126">INPUTS</span></span>

### <span data-ttu-id="4a1c0-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4a1c0-127">None</span></span>

## <span data-ttu-id="4a1c0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-128">OUTPUTS</span></span>

### <span data-ttu-id="4a1c0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a1c0-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="4a1c0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="4a1c0-130">NOTES</span></span>

## <span data-ttu-id="4a1c0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a1c0-131">RELATED LINKS</span></span>

[<span data-ttu-id="4a1c0-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a1c0-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4a1c0-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a1c0-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="4a1c0-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a1c0-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
