---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 3887f8cdbc4256d39e76fc6b86ff9e9113385519
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93441592"
---
# <span data-ttu-id="6c312-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c312-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6c312-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c312-102">SYNOPSIS</span></span>
<span data-ttu-id="6c312-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c312-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c312-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c312-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c312-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c312-105">DESCRIPTION</span></span>
<span data-ttu-id="6c312-106">O cmdlet **New-AzureRmApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6c312-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="6c312-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c312-107">EXAMPLES</span></span>

### <span data-ttu-id="6c312-108">1:</span><span class="sxs-lookup"><span data-stu-id="6c312-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="6c312-109">Esse comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="6c312-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="6c312-110">OS</span><span class="sxs-lookup"><span data-stu-id="6c312-110">PARAMETERS</span></span>

### <span data-ttu-id="6c312-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="6c312-111">-CipherSuite</span></span>
<span data-ttu-id="6c312-112">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="6c312-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="6c312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c312-113">-DefaultProfile</span></span>
<span data-ttu-id="6c312-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6c312-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c312-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="6c312-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="6c312-116">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="6c312-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="6c312-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6c312-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6c312-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="6c312-118">TLSv1_0</span></span> 
- <span data-ttu-id="6c312-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="6c312-119">TLSv1_1</span></span> 
- <span data-ttu-id="6c312-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="6c312-120">TLSv1_2</span></span>

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

### <span data-ttu-id="6c312-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="6c312-121">-MinProtocolVersion</span></span>
<span data-ttu-id="6c312-122">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="6c312-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="6c312-123">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="6c312-123">-PolicyName</span></span>
<span data-ttu-id="6c312-124">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="6c312-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="6c312-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="6c312-125">-PolicyType</span></span>
<span data-ttu-id="6c312-126">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="6c312-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="6c312-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c312-127">-Confirm</span></span>
<span data-ttu-id="6c312-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c312-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c312-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c312-129">-WhatIf</span></span>
<span data-ttu-id="6c312-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c312-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c312-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c312-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c312-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c312-132">CommonParameters</span></span>
<span data-ttu-id="6c312-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c312-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c312-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c312-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c312-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c312-135">INPUTS</span></span>

### <span data-ttu-id="6c312-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6c312-136">System.String</span></span>

## <span data-ttu-id="6c312-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c312-137">OUTPUTS</span></span>

### <span data-ttu-id="6c312-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c312-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6c312-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c312-139">NOTES</span></span>
* <span data-ttu-id="6c312-140">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="6c312-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6c312-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c312-141">RELATED LINKS</span></span>

[<span data-ttu-id="6c312-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c312-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6c312-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6c312-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


