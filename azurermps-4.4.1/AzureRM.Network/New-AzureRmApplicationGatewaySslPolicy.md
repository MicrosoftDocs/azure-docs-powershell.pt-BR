---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: dc6dc0c201ebb8298805064e06af5bb6c63ceda8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429969"
---
# <span data-ttu-id="314d4-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="314d4-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="314d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="314d4-102">SYNOPSIS</span></span>
<span data-ttu-id="314d4-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="314d4-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="314d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="314d4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="314d4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="314d4-105">DESCRIPTION</span></span>
<span data-ttu-id="314d4-106">O cmdlet **New-AzureRmApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="314d4-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="314d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="314d4-107">EXAMPLES</span></span>

### <span data-ttu-id="314d4-108">1:</span><span class="sxs-lookup"><span data-stu-id="314d4-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="314d4-109">Esse comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="314d4-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="314d4-110">OS</span><span class="sxs-lookup"><span data-stu-id="314d4-110">PARAMETERS</span></span>

### <span data-ttu-id="314d4-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="314d4-111">-CipherSuite</span></span>
<span data-ttu-id="314d4-112">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="314d4-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="314d4-113">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="314d4-113">-DisabledSslProtocols</span></span>
<span data-ttu-id="314d4-114">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="314d4-114">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="314d4-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="314d4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="314d4-116">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="314d4-116">TLSv1_0</span></span> 
- <span data-ttu-id="314d4-117">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="314d4-117">TLSv1_1</span></span> 
- <span data-ttu-id="314d4-118">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="314d4-118">TLSv1_2</span></span>

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

### <span data-ttu-id="314d4-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="314d4-119">-MinProtocolVersion</span></span>
<span data-ttu-id="314d4-120">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="314d4-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314d4-121">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="314d4-121">-PolicyName</span></span>
<span data-ttu-id="314d4-122">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="314d4-122">Name of Ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314d4-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="314d4-123">-PolicyType</span></span>
<span data-ttu-id="314d4-124">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="314d4-124">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314d4-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="314d4-125">-Confirm</span></span>
<span data-ttu-id="314d4-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="314d4-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314d4-127">-WhatIf</span></span>
<span data-ttu-id="314d4-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="314d4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314d4-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="314d4-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314d4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314d4-130">-DefaultProfile</span></span>
<span data-ttu-id="314d4-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="314d4-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="314d4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314d4-132">CommonParameters</span></span>
<span data-ttu-id="314d4-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314d4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314d4-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314d4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314d4-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="314d4-135">INPUTS</span></span>

### <span data-ttu-id="314d4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="314d4-136">System.String</span></span>

## <span data-ttu-id="314d4-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="314d4-137">OUTPUTS</span></span>

### <span data-ttu-id="314d4-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="314d4-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="314d4-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="314d4-139">NOTES</span></span>
* <span data-ttu-id="314d4-140">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="314d4-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="314d4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="314d4-141">RELATED LINKS</span></span>

[<span data-ttu-id="314d4-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="314d4-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="314d4-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="314d4-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


