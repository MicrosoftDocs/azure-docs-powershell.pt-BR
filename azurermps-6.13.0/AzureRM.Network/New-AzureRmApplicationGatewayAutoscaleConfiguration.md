---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: f19a2e9f1531f6e009561a9d45ecae07d1bb0a3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433209"
---
# <span data-ttu-id="7b100-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b100-101">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7b100-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b100-102">SYNOPSIS</span></span>
<span data-ttu-id="7b100-103">Cria uma configuração de AutoEscala para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7b100-103">Creates a Autoscale Configuration for the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b100-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b100-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b100-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b100-105">DESCRIPTION</span></span>
<span data-ttu-id="7b100-106">O cmdlet **New-AzureRmApplicationGatewayAutoscaleConfiguration** cria uma configuração de AutoEscala para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="7b100-106">The **New-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet creates Autoscale Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="7b100-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b100-107">EXAMPLES</span></span>

### <span data-ttu-id="7b100-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7b100-108">Example 1</span></span>
```powershell
PS C:\> $autoscaleConfig = New-AzureRmApplicationGatewayAutoscaleConfiguration -MinCapacity 3
PS C:\> $gw = New-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $rgname ..  -AutoscaleConfiguration $autoscaleConfig
```

<span data-ttu-id="7b100-109">O primeiro comando cria uma configuração de dimensionamento automático com capacidade 3 mínima.</span><span class="sxs-lookup"><span data-stu-id="7b100-109">The first command creates an autoscale configuration with minimum capacity 3.</span></span>
<span data-ttu-id="7b100-110">O segundo comando cria um gateway de aplicativo com a configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="7b100-110">The second command creates an application gateway with the autoscale configuration.</span></span>

## <span data-ttu-id="7b100-111">OS</span><span class="sxs-lookup"><span data-stu-id="7b100-111">PARAMETERS</span></span>

### <span data-ttu-id="7b100-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b100-112">-DefaultProfile</span></span>
<span data-ttu-id="7b100-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b100-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b100-114">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="7b100-114">-MinCapacity</span></span>
<span data-ttu-id="7b100-115">Unidades de capacidade mínima que sempre estarão disponíveis [e cobradas] para o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b100-115">Minimum capacity units that will always be available [and charged] for application gateway.</span></span> 

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

### <span data-ttu-id="7b100-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b100-116">-Confirm</span></span>
<span data-ttu-id="7b100-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b100-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b100-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b100-118">-WhatIf</span></span>
<span data-ttu-id="7b100-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b100-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b100-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b100-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b100-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b100-121">CommonParameters</span></span>
<span data-ttu-id="7b100-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b100-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b100-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b100-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b100-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b100-124">INPUTS</span></span>

### <span data-ttu-id="7b100-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7b100-125">None</span></span>

## <span data-ttu-id="7b100-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b100-126">OUTPUTS</span></span>

### <span data-ttu-id="7b100-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b100-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="7b100-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b100-128">NOTES</span></span>

## <span data-ttu-id="7b100-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b100-129">RELATED LINKS</span></span>
