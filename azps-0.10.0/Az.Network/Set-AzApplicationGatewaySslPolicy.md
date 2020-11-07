---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 07958bcab5948280774ff3e056f7c34c9f6b0aac
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776554"
---
# <span data-ttu-id="e8ba6-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba6-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e8ba6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8ba6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ba6-103">Modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e8ba6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8ba6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway>
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8ba6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8ba6-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ba6-106">O cmdlet **set-AzApplicationGatewaySslPolicy** modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="e8ba6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8ba6-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ba6-108">1:</span><span class="sxs-lookup"><span data-stu-id="e8ba6-108">1:</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="e8ba6-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e8ba6-110">Este segundo comando modifica a política SSL para um tipo de política predefinido e nome de política AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="e8ba6-111">OS</span><span class="sxs-lookup"><span data-stu-id="e8ba6-111">PARAMETERS</span></span>

### <span data-ttu-id="e8ba6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8ba6-112">-ApplicationGateway</span></span>
<span data-ttu-id="e8ba6-113">Especifica o gateway de aplicativo da política SSL que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e8ba6-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e8ba6-114">-CipherSuite</span></span>
<span data-ttu-id="e8ba6-115">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e8ba6-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="e8ba6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ba6-116">-DefaultProfile</span></span>
<span data-ttu-id="e8ba6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8ba6-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="e8ba6-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="e8ba6-119">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="e8ba6-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e8ba6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8ba6-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="e8ba6-121">TLSv1_0</span></span> 
- <span data-ttu-id="e8ba6-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="e8ba6-122">TLSv1_1</span></span> 
- <span data-ttu-id="e8ba6-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="e8ba6-123">TLSv1_2</span></span>

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

### <span data-ttu-id="e8ba6-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="e8ba6-124">-MinProtocolVersion</span></span>
<span data-ttu-id="e8ba6-125">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e8ba6-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="e8ba6-126">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="e8ba6-126">-PolicyName</span></span>
<span data-ttu-id="e8ba6-127">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="e8ba6-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="e8ba6-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="e8ba6-128">-PolicyType</span></span>
<span data-ttu-id="e8ba6-129">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="e8ba6-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="e8ba6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e8ba6-130">-Confirm</span></span>
<span data-ttu-id="e8ba6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ba6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ba6-132">-WhatIf</span></span>
<span data-ttu-id="e8ba6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8ba6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ba6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ba6-135">CommonParameters</span></span>
<span data-ttu-id="e8ba6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ba6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ba6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8ba6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ba6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8ba6-138">INPUTS</span></span>

### <span data-ttu-id="e8ba6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ba6-139">System.String</span></span>

## <span data-ttu-id="e8ba6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8ba6-140">OUTPUTS</span></span>

### <span data-ttu-id="e8ba6-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8ba6-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8ba6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8ba6-142">NOTES</span></span>
* <span data-ttu-id="e8ba6-143">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="e8ba6-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e8ba6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8ba6-144">RELATED LINKS</span></span>

[<span data-ttu-id="e8ba6-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba6-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e8ba6-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e8ba6-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)

