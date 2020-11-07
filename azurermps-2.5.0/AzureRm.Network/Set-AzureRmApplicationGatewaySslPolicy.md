---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 1e0d5de8013bbb6fd5104c3af5bdb555b0317e75
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785155"
---
# <span data-ttu-id="0533c-101">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0533c-101">Set-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="0533c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0533c-102">SYNOPSIS</span></span>
<span data-ttu-id="0533c-103">Modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0533c-103">Modifies the SSL policy of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0533c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0533c-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0533c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0533c-105">DESCRIPTION</span></span>
<span data-ttu-id="0533c-106">O cmdlet **set-AzureRmApplicationGatewaySslPolicy** modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0533c-106">The **Set-AzureRmApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="0533c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0533c-107">EXAMPLES</span></span>

### <span data-ttu-id="0533c-108">1:</span><span class="sxs-lookup"><span data-stu-id="0533c-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="0533c-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0533c-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="0533c-110">Este segundo comando modifica a política SSL para um tipo de política predefinido e nome de política AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="0533c-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="0533c-111">OS</span><span class="sxs-lookup"><span data-stu-id="0533c-111">PARAMETERS</span></span>

### <span data-ttu-id="0533c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0533c-112">-ApplicationGateway</span></span>
<span data-ttu-id="0533c-113">Especifica o gateway de aplicativo da política SSL que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0533c-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="0533c-114">-CipherSuite</span></span>
<span data-ttu-id="0533c-115">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="0533c-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0533c-116">-DefaultProfile</span></span>
<span data-ttu-id="0533c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0533c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="0533c-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="0533c-119">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="0533c-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="0533c-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0533c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0533c-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="0533c-121">TLSv1_0</span></span> 
- <span data-ttu-id="0533c-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="0533c-122">TLSv1_1</span></span> 
- <span data-ttu-id="0533c-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="0533c-123">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="0533c-124">-MinProtocolVersion</span></span>
<span data-ttu-id="0533c-125">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="0533c-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-126">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="0533c-126">-PolicyName</span></span>
<span data-ttu-id="0533c-127">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="0533c-127">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="0533c-128">-PolicyType</span></span>
<span data-ttu-id="0533c-129">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="0533c-129">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0533c-130">-Confirm</span></span>
<span data-ttu-id="0533c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0533c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0533c-132">-WhatIf</span></span>
<span data-ttu-id="0533c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0533c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0533c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0533c-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0533c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0533c-135">CommonParameters</span></span>
<span data-ttu-id="0533c-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0533c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0533c-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0533c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0533c-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0533c-138">INPUTS</span></span>

### <span data-ttu-id="0533c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0533c-139">System.String</span></span>

## <span data-ttu-id="0533c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0533c-140">OUTPUTS</span></span>

### <span data-ttu-id="0533c-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0533c-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0533c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0533c-142">NOTES</span></span>
* <span data-ttu-id="0533c-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="0533c-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0533c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0533c-144">RELATED LINKS</span></span>

[<span data-ttu-id="0533c-145">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0533c-145">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="0533c-146">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="0533c-146">New-AzureRmApplicationGatewaySslPolicy</span></span>](./New-AzureRmApplicationGatewaySslPolicy.md)


