---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 344be8b71bc74f3620ca90dd60b61f9a59026ea0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115064"
---
# <span data-ttu-id="bafe0-101">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="bafe0-101">Set-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="bafe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bafe0-102">SYNOPSIS</span></span>
<span data-ttu-id="bafe0-103">Modifica a política SSL de um perfil SSL de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bafe0-103">Modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="bafe0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bafe0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DisabledSslProtocols <String[]>] [-PolicyType <String>] [-PolicyName <String>] [-CipherSuite <String[]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bafe0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bafe0-105">DESCRIPTION</span></span>
<span data-ttu-id="bafe0-106">O cmdlet **Set-AzApplicationGatewaySslProfilePolicy** modifica a política SSL de um perfil SSL de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bafe0-106">The **Set-AzApplicationGatewaySslProfilePolicy** cmdlet modifies the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="bafe0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bafe0-107">EXAMPLES</span></span>

### <span data-ttu-id="bafe0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bafe0-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $profile = Set-AzApplicationGatewaySslProfilePolicy -SslProfile $profile -PolicyType Predefined -PolicyName AppGwSslPolicy20170401
```

<span data-ttu-id="bafe0-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="bafe0-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="bafe0-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e armazena as configurações na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="bafe0-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="bafe0-111">O último comando modifica a política ssl do objeto de perfil ssl armazenado em $profile.</span><span class="sxs-lookup"><span data-stu-id="bafe0-111">The last command modifies the ssl policy of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="bafe0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bafe0-112">PARAMETERS</span></span>

### <span data-ttu-id="bafe0-113">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="bafe0-113">-CipherSuite</span></span>
<span data-ttu-id="bafe0-114">Pacote de SSL para serem habilitados na ordem especificada para o gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="bafe0-114">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafe0-115">-DefaultProfile</span></span>
<span data-ttu-id="bafe0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bafe0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-117">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="bafe0-117">-DisabledSslProtocols</span></span>
<span data-ttu-id="bafe0-118">Lista de protocolos SSL a serem desabilitados</span><span class="sxs-lookup"><span data-stu-id="bafe0-118">List of SSL protocols to be disabled</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-119">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="bafe0-119">-MinProtocolVersion</span></span>
<span data-ttu-id="bafe0-120">Versão mínima do protocolo SSL a ser suportada no gateway de aplicativos</span><span class="sxs-lookup"><span data-stu-id="bafe0-120">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="bafe0-121">-Nomeda Política</span><span class="sxs-lookup"><span data-stu-id="bafe0-121">-PolicyName</span></span>
<span data-ttu-id="bafe0-122">Nome da política predefinida SSL</span><span class="sxs-lookup"><span data-stu-id="bafe0-122">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="bafe0-123">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="bafe0-123">-PolicyType</span></span>
<span data-ttu-id="bafe0-124">Tipo de Política SSL</span><span class="sxs-lookup"><span data-stu-id="bafe0-124">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="bafe0-125">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="bafe0-125">-SslProfile</span></span>
<span data-ttu-id="bafe0-126">O perfil SSL do gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="bafe0-126">The application gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bafe0-127">-Confirm</span></span>
<span data-ttu-id="bafe0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bafe0-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bafe0-129">-WhatIf</span></span>
<span data-ttu-id="bafe0-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bafe0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bafe0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bafe0-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafe0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafe0-132">CommonParameters</span></span>
<span data-ttu-id="bafe0-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bafe0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafe0-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bafe0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafe0-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="bafe0-135">INPUTS</span></span>

### <span data-ttu-id="bafe0-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bafe0-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="bafe0-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="bafe0-137">OUTPUTS</span></span>

### <span data-ttu-id="bafe0-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="bafe0-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="bafe0-139">Notas</span><span class="sxs-lookup"><span data-stu-id="bafe0-139">NOTES</span></span>

## <span data-ttu-id="bafe0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bafe0-140">RELATED LINKS</span></span>

[<span data-ttu-id="bafe0-141">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="bafe0-141">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="bafe0-142">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="bafe0-142">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="bafe0-143">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="bafe0-143">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="bafe0-144">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="bafe0-144">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)