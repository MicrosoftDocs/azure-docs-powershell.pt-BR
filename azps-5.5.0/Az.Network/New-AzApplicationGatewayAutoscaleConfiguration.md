---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 5bf9106ccfd780fcfcdb7c86b6b86cdee82aba43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118348"
---
# <span data-ttu-id="ed62c-101">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed62c-101">New-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ed62c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed62c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed62c-103">Cria uma Configuração de Escala Automática para o Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed62c-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

## <span data-ttu-id="ed62c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed62c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32> [-MaxCapacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed62c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed62c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed62c-106">O cmdlet **New-AzApplicationGatewayAutoscaleConfiguration** cria a Configuração de Escala Automática para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed62c-106">The **New-AzApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="ed62c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ed62c-107">EXAMPLES</span></span>

### <span data-ttu-id="ed62c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed62c-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="ed62c-109">O primeiro comando cria uma configuração de escala automática com capacidade mínima 3.</span><span class="sxs-lookup"><span data-stu-id="ed62c-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="ed62c-110">O segundo comando cria um gateway de aplicativo com a configuração de escala automática.</span><span class="sxs-lookup"><span data-stu-id="ed62c-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="ed62c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed62c-111">PARAMETERS</span></span>

### <span data-ttu-id="ed62c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed62c-112">-DefaultProfile</span></span>
<span data-ttu-id="ed62c-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed62c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed62c-114">-MaxCapacity</span><span class="sxs-lookup"><span data-stu-id="ed62c-114">-MaxCapacity</span></span>
<span data-ttu-id="ed62c-115">Unidades máximas de capacidade que estarão sempre disponíveis [e cobradas] para o gateway de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ed62c-115">Maximum capacity units that will always be available [and charged] for application gateway.</span></span>

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

### <span data-ttu-id="ed62c-116">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="ed62c-116">-MinCapacity</span></span>
<span data-ttu-id="ed62c-117">Unidades de capacidade mínima que sempre estarão disponíveis [e cobradas] para o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed62c-117">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="ed62c-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ed62c-118">-Confirm</span></span>
<span data-ttu-id="ed62c-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed62c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed62c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed62c-120">-WhatIf</span></span>
<span data-ttu-id="ed62c-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ed62c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed62c-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed62c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed62c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed62c-123">CommonParameters</span></span>
<span data-ttu-id="ed62c-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed62c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed62c-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed62c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed62c-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="ed62c-126">INPUTS</span></span>

### <span data-ttu-id="ed62c-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ed62c-127">None</span></span>

## <span data-ttu-id="ed62c-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ed62c-128">OUTPUTS</span></span>

### <span data-ttu-id="ed62c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed62c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="ed62c-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ed62c-130">NOTES</span></span>

## <span data-ttu-id="ed62c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed62c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ed62c-132">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed62c-132">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Get-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ed62c-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed62c-133">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="ed62c-134">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="ed62c-134">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
