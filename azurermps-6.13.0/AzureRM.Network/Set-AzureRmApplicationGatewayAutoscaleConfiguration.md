---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 2d7fa9dd9030f1e5878293276a248c2f6718efe5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431939"
---
# <span data-ttu-id="68707-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="68707-101">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="68707-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68707-102">SYNOPSIS</span></span>
<span data-ttu-id="68707-103">Atualiza a configuração de autoescala de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68707-103">Updates Autoscale Configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68707-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68707-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 -MinCapacity <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68707-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68707-105">DESCRIPTION</span></span>
<span data-ttu-id="68707-106">O cmdlet **set-AzureRmApplicationGatewayAutoscaleConfiguration** modifica a configuração de autoescala existente de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68707-106">The **Set-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet modifies the existing autoscale configuration of an Application Gateway.</span></span>

## <span data-ttu-id="68707-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68707-107">EXAMPLES</span></span>

### <span data-ttu-id="68707-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68707-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw -MinCapacity 5
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="68707-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="68707-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="68707-110">O segundo comando atualiza a configuração de autoescala do gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="68707-110">The second command updates the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="68707-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="68707-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="68707-112">OS</span><span class="sxs-lookup"><span data-stu-id="68707-112">PARAMETERS</span></span>

### <span data-ttu-id="68707-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68707-113">-ApplicationGateway</span></span>
<span data-ttu-id="68707-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="68707-114">The applicationGateway</span></span>

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

### <span data-ttu-id="68707-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68707-115">-DefaultProfile</span></span>
<span data-ttu-id="68707-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68707-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68707-117">-MinCapacity</span><span class="sxs-lookup"><span data-stu-id="68707-117">-MinCapacity</span></span>
<span data-ttu-id="68707-118">Capcity mínima para o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="68707-118">Minimum capcity for application gateway.</span></span>

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

### <span data-ttu-id="68707-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68707-119">-Confirm</span></span>
<span data-ttu-id="68707-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68707-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68707-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68707-121">-WhatIf</span></span>
<span data-ttu-id="68707-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68707-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68707-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68707-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68707-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68707-124">CommonParameters</span></span>
<span data-ttu-id="68707-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68707-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68707-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68707-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68707-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68707-127">INPUTS</span></span>

### <span data-ttu-id="68707-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68707-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68707-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68707-129">OUTPUTS</span></span>

### <span data-ttu-id="68707-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="68707-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="68707-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68707-131">NOTES</span></span>

## <span data-ttu-id="68707-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68707-132">RELATED LINKS</span></span>
