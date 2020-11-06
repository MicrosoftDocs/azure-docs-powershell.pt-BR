---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 4affc8cdfe860dc82fe5cb71c19d4ce73301ed19
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600376"
---
# <span data-ttu-id="04590-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="04590-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="04590-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04590-102">SYNOPSIS</span></span>
<span data-ttu-id="04590-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04590-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="04590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04590-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04590-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04590-105">DESCRIPTION</span></span>
<span data-ttu-id="04590-106">O cmdlet **New-AzApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04590-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="04590-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04590-107">EXAMPLES</span></span>

### <span data-ttu-id="04590-108">1:</span><span class="sxs-lookup"><span data-stu-id="04590-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="04590-109">Esse comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="04590-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="04590-110">OS</span><span class="sxs-lookup"><span data-stu-id="04590-110">PARAMETERS</span></span>

### <span data-ttu-id="04590-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="04590-111">-CipherSuite</span></span>
<span data-ttu-id="04590-112">Pacotes de codificação SSL a serem habilitados na ordem especificada para o gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="04590-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04590-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04590-113">-DefaultProfile</span></span>
<span data-ttu-id="04590-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04590-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04590-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="04590-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="04590-116">Especifica quais protocolos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="04590-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="04590-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="04590-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04590-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="04590-118">TLSv1_0</span></span> 
- <span data-ttu-id="04590-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="04590-119">TLSv1_1</span></span> 
- <span data-ttu-id="04590-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="04590-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04590-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="04590-121">-MinProtocolVersion</span></span>
<span data-ttu-id="04590-122">Versão mínima do protocolo SSL para suporte no Application Gateway</span><span class="sxs-lookup"><span data-stu-id="04590-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="04590-123">-Políticaname</span><span class="sxs-lookup"><span data-stu-id="04590-123">-PolicyName</span></span>
<span data-ttu-id="04590-124">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="04590-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="04590-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="04590-125">-PolicyType</span></span>
<span data-ttu-id="04590-126">Tipo de política SSL</span><span class="sxs-lookup"><span data-stu-id="04590-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="04590-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="04590-127">-Confirm</span></span>
<span data-ttu-id="04590-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04590-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04590-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04590-129">-WhatIf</span></span>
<span data-ttu-id="04590-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04590-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04590-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04590-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04590-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04590-132">CommonParameters</span></span>
<span data-ttu-id="04590-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04590-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04590-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04590-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04590-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04590-135">INPUTS</span></span>

### <span data-ttu-id="04590-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="04590-136">None</span></span>

## <span data-ttu-id="04590-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04590-137">OUTPUTS</span></span>

### <span data-ttu-id="04590-138">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="04590-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="04590-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04590-139">NOTES</span></span>
* <span data-ttu-id="04590-140">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="04590-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="04590-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04590-141">RELATED LINKS</span></span>

[<span data-ttu-id="04590-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="04590-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="04590-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="04590-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


