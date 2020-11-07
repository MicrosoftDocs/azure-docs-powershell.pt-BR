---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 6c28665f35a7422a731aefd4ccf1c4ecabc549d4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785319"
---
# <span data-ttu-id="e59c2-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e59c2-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e59c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e59c2-102">SYNOPSIS</span></span>
<span data-ttu-id="e59c2-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e59c2-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e59c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e59c2-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e59c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e59c2-105">DESCRIPTION</span></span>
<span data-ttu-id="e59c2-106">O cmdlet **New-AzureRmApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e59c2-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="e59c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e59c2-107">EXAMPLES</span></span>

### <span data-ttu-id="e59c2-108">1:</span><span class="sxs-lookup"><span data-stu-id="e59c2-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="e59c2-109">Esse comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="e59c2-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="e59c2-110">OS</span><span class="sxs-lookup"><span data-stu-id="e59c2-110">PARAMETERS</span></span>

### <span data-ttu-id="e59c2-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e59c2-111">-CipherSuite</span></span>
<span data-ttu-id="e59c2-112">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e59c2-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="e59c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59c2-113">-DefaultProfile</span></span>
<span data-ttu-id="e59c2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e59c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e59c2-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="e59c2-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="e59c2-116">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="e59c2-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="e59c2-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e59c2-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e59c2-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="e59c2-118">TLSv1_0</span></span> 
- <span data-ttu-id="e59c2-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="e59c2-119">TLSv1_1</span></span> 
- <span data-ttu-id="e59c2-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="e59c2-120">TLSv1_2</span></span>

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

### <span data-ttu-id="e59c2-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="e59c2-121">-MinProtocolVersion</span></span>
<span data-ttu-id="e59c2-122">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e59c2-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="e59c2-123">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="e59c2-123">-PolicyName</span></span>
<span data-ttu-id="e59c2-124">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="e59c2-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="e59c2-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="e59c2-125">-PolicyType</span></span>
<span data-ttu-id="e59c2-126">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="e59c2-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="e59c2-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e59c2-127">-Confirm</span></span>
<span data-ttu-id="e59c2-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e59c2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59c2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59c2-129">-WhatIf</span></span>
<span data-ttu-id="e59c2-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e59c2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59c2-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e59c2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59c2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59c2-132">CommonParameters</span></span>
<span data-ttu-id="e59c2-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59c2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59c2-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e59c2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59c2-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e59c2-135">INPUTS</span></span>

### <span data-ttu-id="e59c2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e59c2-136">System.String</span></span>

## <span data-ttu-id="e59c2-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e59c2-137">OUTPUTS</span></span>

### <span data-ttu-id="e59c2-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e59c2-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="e59c2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e59c2-139">NOTES</span></span>
* <span data-ttu-id="e59c2-140">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="e59c2-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e59c2-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e59c2-141">RELATED LINKS</span></span>

[<span data-ttu-id="e59c2-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e59c2-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="e59c2-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="e59c2-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


