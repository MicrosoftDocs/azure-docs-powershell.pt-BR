---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124520"
---
# <span data-ttu-id="f3ade-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ade-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f3ade-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3ade-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ade-103">Cria uma configuração de AutoEscala para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f3ade-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="f3ade-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3ade-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3ade-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3ade-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ade-106">O cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** cria uma configuração de AutoEscala para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ade-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="f3ade-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3ade-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ade-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3ade-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="f3ade-109">O primeiro comando cria uma configuração de dimensionamento automático com capacidade 3 mínima.</span><span class="sxs-lookup"><span data-stu-id="f3ade-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="f3ade-110">O segundo comando cria um gateway de aplicativo com a configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="f3ade-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="f3ade-111">OS</span><span class="sxs-lookup"><span data-stu-id="f3ade-111">PARAMETERS</span></span>

### <span data-ttu-id="f3ade-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ade-112">-DefaultProfile</span></span>
<span data-ttu-id="f3ade-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ade-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ade-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="f3ade-114">-MaxCapacity</span></span>
<span data-ttu-id="f3ade-115">Unidades de capacidade máxima que sempre estarão disponíveis [e cobradas] para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3ade-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="f3ade-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="f3ade-116">-MinCapacity</span></span>
<span data-ttu-id="f3ade-117">Unidades de capacidade mínima que sempre estarão disponíveis [e cobradas] para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f3ade-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="f3ade-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f3ade-118">-Confirm</span></span>
<span data-ttu-id="f3ade-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3ade-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ade-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ade-120">-WhatIf</span></span>
<span data-ttu-id="f3ade-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f3ade-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ade-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f3ade-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ade-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ade-123">CommonParameters</span></span>
<span data-ttu-id="f3ade-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ade-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ade-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ade-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ade-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3ade-126">INPUTS</span></span>

### <span data-ttu-id="f3ade-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f3ade-127">None</span></span>

## <span data-ttu-id="f3ade-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3ade-128">OUTPUTS</span></span>

### <span data-ttu-id="f3ade-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ade-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="f3ade-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3ade-130">NOTES</span></span>

## <span data-ttu-id="f3ade-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3ade-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3ade-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ade-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f3ade-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ade-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="f3ade-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3ade-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
