---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111562"
---
# <span data-ttu-id="5c27f-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="5c27f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c27f-102">SYNOPSIS</span></span>
<span data-ttu-id="5c27f-103">Modifica uma Configuração do PrivateLink para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c27f-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="5c27f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c27f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c27f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5c27f-105">DESCRIPTION</span></span>
<span data-ttu-id="5c27f-106">O cmdlet **Set-AzApplicationGatewayPrivateLinkConfiguration** modifica uma configuração de privateLink para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5c27f-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="5c27f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c27f-107">EXAMPLES</span></span>

### <span data-ttu-id="5c27f-108">Exemplo 1: Definir uma Configuração de PrivateLink</span><span class="sxs-lookup"><span data-stu-id="5c27f-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="5c27f-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="5c27f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c27f-110">O segundo comando define a configuração privateLink com nome privateLinkConfig01 para usar a configuração de ip armazenada no $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="5c27f-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="5c27f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c27f-111">PARAMETERS</span></span>

### <span data-ttu-id="5c27f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c27f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5c27f-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c27f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5c27f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c27f-114">-DefaultProfile</span></span>
<span data-ttu-id="5c27f-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c27f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c27f-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-116">-IpConfiguration</span></span>
<span data-ttu-id="5c27f-117">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-117">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c27f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c27f-118">-Name</span></span>
<span data-ttu-id="5c27f-119">O nome da configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="5c27f-119">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c27f-120">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5c27f-120">-Confirm</span></span>
<span data-ttu-id="5c27f-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c27f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c27f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c27f-122">-WhatIf</span></span>
<span data-ttu-id="5c27f-123">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5c27f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c27f-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c27f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c27f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c27f-125">CommonParameters</span></span>
<span data-ttu-id="5c27f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c27f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c27f-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c27f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c27f-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="5c27f-128">INPUTS</span></span>

### <span data-ttu-id="5c27f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c27f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="5c27f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="5c27f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="5c27f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="5c27f-131">OUTPUTS</span></span>

### <span data-ttu-id="5c27f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c27f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c27f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="5c27f-133">NOTES</span></span>

## <span data-ttu-id="5c27f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c27f-134">RELATED LINKS</span></span>

[<span data-ttu-id="5c27f-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c27f-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c27f-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="5c27f-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c27f-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)