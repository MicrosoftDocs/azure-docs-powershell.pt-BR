---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: e2d80f6c132967e18e5a03a3a4bee4ed470f1719
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111606"
---
# <span data-ttu-id="511e9-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="511e9-101">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="511e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="511e9-102">SYNOPSIS</span></span>
<span data-ttu-id="511e9-103">Remove a Configuração de Escala Automática de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="511e9-103">Removes Autoscale Configuration from an application gateway.</span></span>

## <span data-ttu-id="511e9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="511e9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="511e9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="511e9-105">DESCRIPTION</span></span>
<span data-ttu-id="511e9-106">O cmdlet **Remove-AzApplicationGatewayAutoscaleConfiguration** remove a Configuração de Escala Automática de um Gateway de Aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="511e9-106">The **Remove-AzApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="511e9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="511e9-107">EXAMPLES</span></span>

### <span data-ttu-id="511e9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="511e9-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="511e9-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="511e9-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="511e9-110">O segundo comando remove a configuração de escala automática do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="511e9-110">The second command removes the autoscale configuration from the application gateway.</span></span>
<span data-ttu-id="511e9-111">O terceiro comando atualiza o gateway do aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="511e9-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="511e9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="511e9-112">PARAMETERS</span></span>

### <span data-ttu-id="511e9-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="511e9-113">-ApplicationGateway</span></span>
<span data-ttu-id="511e9-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="511e9-114">The applicationGateway</span></span>

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

### <span data-ttu-id="511e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511e9-115">-DefaultProfile</span></span>
<span data-ttu-id="511e9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="511e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="511e9-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="511e9-117">-Force</span></span>
<span data-ttu-id="511e9-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="511e9-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="511e9-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="511e9-119">-Confirm</span></span>
<span data-ttu-id="511e9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="511e9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="511e9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="511e9-121">-WhatIf</span></span>
<span data-ttu-id="511e9-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="511e9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="511e9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="511e9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="511e9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511e9-124">CommonParameters</span></span>
<span data-ttu-id="511e9-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="511e9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511e9-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="511e9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511e9-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="511e9-127">INPUTS</span></span>

### <span data-ttu-id="511e9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="511e9-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="511e9-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="511e9-129">OUTPUTS</span></span>

### <span data-ttu-id="511e9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="511e9-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="511e9-131">Notas</span><span class="sxs-lookup"><span data-stu-id="511e9-131">NOTES</span></span>

## <span data-ttu-id="511e9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="511e9-132">RELATED LINKS</span></span>

[<span data-ttu-id="511e9-133">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="511e9-133">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="511e9-134">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="511e9-134">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="511e9-135">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="511e9-135">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
