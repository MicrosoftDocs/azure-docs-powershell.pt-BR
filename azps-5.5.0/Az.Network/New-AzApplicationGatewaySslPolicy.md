---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: cf2f2ef91fa217b1710eeb100f4e3e6c2ce6fb9d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113487"
---
# <span data-ttu-id="6cbfe-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6cbfe-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6cbfe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="6cbfe-103">Cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="6cbfe-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cbfe-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cbfe-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cbfe-105">DESCRIPTION</span></span>
<span data-ttu-id="6cbfe-106">O **cmdlet New-AzApplicationGatewaySslPolicy** cria uma política SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="6cbfe-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6cbfe-107">EXAMPLES</span></span>

### <span data-ttu-id="6cbfe-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6cbfe-108">Example 1</span></span>
```powershell
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="6cbfe-109">Esse comando cria uma política personalizada.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="6cbfe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cbfe-110">PARAMETERS</span></span>

### <span data-ttu-id="6cbfe-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="6cbfe-111">-CipherSuite</span></span>
<span data-ttu-id="6cbfe-112">Pacote de SSL para serem habilitados na ordem especificada para o gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6cbfe-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="6cbfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cbfe-113">-DefaultProfile</span></span>
<span data-ttu-id="6cbfe-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cbfe-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="6cbfe-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="6cbfe-116">Especifica quais protocolos estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="6cbfe-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6cbfe-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6cbfe-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="6cbfe-118">TLSv1_0</span></span> 
- <span data-ttu-id="6cbfe-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="6cbfe-119">TLSv1_1</span></span> 
- <span data-ttu-id="6cbfe-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="6cbfe-120">TLSv1_2</span></span>

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

### <span data-ttu-id="6cbfe-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="6cbfe-121">-MinProtocolVersion</span></span>
<span data-ttu-id="6cbfe-122">Versão mínima do protocolo SSL a ser suportada no gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="6cbfe-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="6cbfe-123">-Nomeda Política</span><span class="sxs-lookup"><span data-stu-id="6cbfe-123">-PolicyName</span></span>
<span data-ttu-id="6cbfe-124">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="6cbfe-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="6cbfe-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="6cbfe-125">-PolicyType</span></span>
<span data-ttu-id="6cbfe-126">Tipo de Política SSL</span><span class="sxs-lookup"><span data-stu-id="6cbfe-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="6cbfe-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6cbfe-127">-Confirm</span></span>
<span data-ttu-id="6cbfe-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cbfe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cbfe-129">-WhatIf</span></span>
<span data-ttu-id="6cbfe-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cbfe-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cbfe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cbfe-132">CommonParameters</span></span>
<span data-ttu-id="6cbfe-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cbfe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cbfe-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cbfe-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cbfe-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="6cbfe-135">INPUTS</span></span>

### <span data-ttu-id="6cbfe-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6cbfe-136">None</span></span>

## <span data-ttu-id="6cbfe-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="6cbfe-137">OUTPUTS</span></span>

### <span data-ttu-id="6cbfe-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6cbfe-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="6cbfe-139">Notas</span><span class="sxs-lookup"><span data-stu-id="6cbfe-139">NOTES</span></span>
* <span data-ttu-id="6cbfe-140">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="6cbfe-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6cbfe-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cbfe-141">RELATED LINKS</span></span>

[<span data-ttu-id="6cbfe-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6cbfe-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="6cbfe-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="6cbfe-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


