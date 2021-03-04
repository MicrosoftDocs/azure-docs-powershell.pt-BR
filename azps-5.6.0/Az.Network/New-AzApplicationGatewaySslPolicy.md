---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: b8b9eadd0beba6413b8b5919087a1c9081735ddf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901457"
---
# <span data-ttu-id="64155-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="64155-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="64155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64155-102">SYNOPSIS</span></span>
<span data-ttu-id="64155-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64155-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="64155-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="64155-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64155-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="64155-105">DESCRIPTION</span></span>
<span data-ttu-id="64155-106">O cmdlet **New-AzApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="64155-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="64155-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64155-107">EXAMPLES</span></span>

### <span data-ttu-id="64155-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64155-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="64155-109">Este comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="64155-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="64155-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="64155-110">PARAMETERS</span></span>

### <span data-ttu-id="64155-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="64155-111">-CipherSuite</span></span>
<span data-ttu-id="64155-112">Pacote de codificação Ssl a ser habilitado na ordem especificada para gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="64155-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="64155-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64155-113">-DefaultProfile</span></span>
<span data-ttu-id="64155-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="64155-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64155-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="64155-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="64155-116">Especifica quais protocolos estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="64155-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="64155-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="64155-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64155-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="64155-118">TLSv1_0</span></span> 
- <span data-ttu-id="64155-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="64155-119">TLSv1_1</span></span> 
- <span data-ttu-id="64155-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="64155-120">TLSv1_2</span></span>

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

### <span data-ttu-id="64155-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="64155-121">-MinProtocolVersion</span></span>
<span data-ttu-id="64155-122">Versão mínima do protocolo Ssl a ser suportada no gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="64155-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="64155-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="64155-123">-PolicyName</span></span>
<span data-ttu-id="64155-124">Nome da política predefinida Ssl</span><span class="sxs-lookup"><span data-stu-id="64155-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="64155-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="64155-125">-PolicyType</span></span>
<span data-ttu-id="64155-126">Tipo de Política Ssl</span><span class="sxs-lookup"><span data-stu-id="64155-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="64155-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64155-127">-Confirm</span></span>
<span data-ttu-id="64155-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64155-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64155-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64155-129">-WhatIf</span></span>
<span data-ttu-id="64155-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64155-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64155-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64155-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64155-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64155-132">CommonParameters</span></span>
<span data-ttu-id="64155-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64155-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64155-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64155-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64155-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64155-135">INPUTS</span></span>

### <span data-ttu-id="64155-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="64155-136">None</span></span>

## <span data-ttu-id="64155-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="64155-137">OUTPUTS</span></span>

### <span data-ttu-id="64155-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="64155-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="64155-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="64155-139">NOTES</span></span>
* <span data-ttu-id="64155-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="64155-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="64155-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64155-141">RELATED LINKS</span></span>

[<span data-ttu-id="64155-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="64155-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="64155-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="64155-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


