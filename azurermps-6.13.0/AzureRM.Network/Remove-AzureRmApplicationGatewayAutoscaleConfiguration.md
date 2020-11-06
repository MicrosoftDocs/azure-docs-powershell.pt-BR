---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 1ca390eb8c99ad991f5a15c6a3959d366ae5f983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428461"
---
# <span data-ttu-id="b28b8-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b28b8-101">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="b28b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b28b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b28b8-103">Remove a configuração de autoescala de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="b28b8-103">Removes Autoscale Configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b28b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b28b8-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b28b8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b28b8-105">DESCRIPTION</span></span>
<span data-ttu-id="b28b8-106">O cmdlet **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** remove a configuração de autoescala de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="b28b8-106">The **Remove-AzureRmApplicationGatewayAutoscaleConfiguration** cmdlet removes Autoscale Configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="b28b8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b28b8-107">EXAMPLES</span></span>

### <span data-ttu-id="b28b8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b28b8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b28b8-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="b28b8-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="b28b8-110">O segundo comando Remove a configuração de autoescala do gateway applicationg.</span><span class="sxs-lookup"><span data-stu-id="b28b8-110">The second command removes the autoscale configuration from the applicationg gateway.</span></span>
<span data-ttu-id="b28b8-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="b28b8-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b28b8-112">OS</span><span class="sxs-lookup"><span data-stu-id="b28b8-112">PARAMETERS</span></span>

### <span data-ttu-id="b28b8-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b8-113">-ApplicationGateway</span></span>
<span data-ttu-id="b28b8-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b8-114">The applicationGateway</span></span>

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

### <span data-ttu-id="b28b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b28b8-115">-DefaultProfile</span></span>
<span data-ttu-id="b28b8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b28b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b28b8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b28b8-117">-Force</span></span>
<span data-ttu-id="b28b8-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b28b8-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b28b8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b28b8-119">-Confirm</span></span>
<span data-ttu-id="b28b8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b28b8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b28b8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b28b8-121">-WhatIf</span></span>
<span data-ttu-id="b28b8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b28b8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b28b8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b28b8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b28b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b28b8-124">CommonParameters</span></span>
<span data-ttu-id="b28b8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b28b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b28b8-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b28b8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b28b8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b28b8-127">INPUTS</span></span>

### <span data-ttu-id="b28b8-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b8-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b28b8-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b28b8-129">OUTPUTS</span></span>

### <span data-ttu-id="b28b8-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b28b8-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b28b8-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b28b8-131">NOTES</span></span>

## <span data-ttu-id="b28b8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b28b8-132">RELATED LINKS</span></span>