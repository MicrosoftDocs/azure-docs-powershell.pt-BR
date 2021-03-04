---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 30A34CA8-AC07-4327-B7B9-19F001DA996A
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 689e678bf740590f3d5d749124b74a38742395b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889770"
---
# <span data-ttu-id="50071-101">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="50071-101">Set-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="50071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50071-102">SYNOPSIS</span></span>
<span data-ttu-id="50071-103">Modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50071-103">Modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="50071-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="50071-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-DisabledSslProtocols <String[]>]
 [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50071-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="50071-105">DESCRIPTION</span></span>
<span data-ttu-id="50071-106">O cmdlet **Set-AzApplicationGatewaySslPolicy** modifica a política SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50071-106">The **Set-AzApplicationGatewaySslPolicy** cmdlet modifies the SSL policy of an application gateway.</span></span>

## <span data-ttu-id="50071-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="50071-107">EXAMPLES</span></span>

### <span data-ttu-id="50071-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="50071-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslPolicy -ApplicationGateway $getgw -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="50071-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e o armazena na variável $AppGw de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="50071-109">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50071-110">Este segundo comando modifica a política ssl para um tipo de política Predefinido e nome de política AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="50071-110">This second command modifies the ssl policy to a policy type Predefined and policy name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="50071-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="50071-111">PARAMETERS</span></span>

### <span data-ttu-id="50071-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50071-112">-ApplicationGateway</span></span>
<span data-ttu-id="50071-113">Especifica o gateway de aplicativo da política SSL que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="50071-113">Specifies the application gateway of the SSL policy that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="50071-114">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="50071-114">-CipherSuite</span></span>
<span data-ttu-id="50071-115">Pacote de codificação Ssl a ser habilitado na ordem especificada para gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="50071-115">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="50071-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50071-116">-DefaultProfile</span></span>
<span data-ttu-id="50071-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="50071-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50071-118">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="50071-118">-DisabledSslProtocols</span></span>
<span data-ttu-id="50071-119">Especifica quais protocolos estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="50071-119">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="50071-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="50071-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="50071-121">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="50071-121">TLSv1_0</span></span> 
- <span data-ttu-id="50071-122">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="50071-122">TLSv1_1</span></span> 
- <span data-ttu-id="50071-123">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="50071-123">TLSv1_2</span></span>

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

### <span data-ttu-id="50071-124">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="50071-124">-MinProtocolVersion</span></span>
<span data-ttu-id="50071-125">Versão mínima do protocolo Ssl a ser suportada no gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="50071-125">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="50071-126">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="50071-126">-PolicyName</span></span>
<span data-ttu-id="50071-127">Nome da política predefinida Ssl</span><span class="sxs-lookup"><span data-stu-id="50071-127">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="50071-128">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="50071-128">-PolicyType</span></span>
<span data-ttu-id="50071-129">Tipo de Política Ssl</span><span class="sxs-lookup"><span data-stu-id="50071-129">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="50071-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50071-130">-Confirm</span></span>
<span data-ttu-id="50071-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50071-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50071-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50071-132">-WhatIf</span></span>
<span data-ttu-id="50071-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="50071-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50071-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="50071-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50071-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50071-135">CommonParameters</span></span>
<span data-ttu-id="50071-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50071-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50071-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50071-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50071-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50071-138">INPUTS</span></span>

### <span data-ttu-id="50071-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50071-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50071-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="50071-140">OUTPUTS</span></span>

### <span data-ttu-id="50071-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50071-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50071-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="50071-142">NOTES</span></span>
* <span data-ttu-id="50071-143">Palavras-chave: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="50071-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="50071-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="50071-144">RELATED LINKS</span></span>

[<span data-ttu-id="50071-145">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="50071-145">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="50071-146">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="50071-146">New-AzApplicationGatewaySslPolicy</span></span>](./New-AzApplicationGatewaySslPolicy.md)


