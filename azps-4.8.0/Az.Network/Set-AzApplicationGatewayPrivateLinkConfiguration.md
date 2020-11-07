---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954797"
---
# <span data-ttu-id="8f2a3-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="8f2a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2a3-103">Modifica uma configuração de PrivateLink para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="8f2a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f2a3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f2a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f2a3-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2a3-106">O cmdlet **set-AzApplicationGatewayPrivateLinkConfiguration** modifica uma configuração privateLink para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="8f2a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f2a3-107">EXAMPLES</span></span>

### <span data-ttu-id="8f2a3-108">Exemplo 1: definir uma configuração de PrivateLink</span><span class="sxs-lookup"><span data-stu-id="8f2a3-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="8f2a3-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8f2a3-110">O segundo comando define a configuração privateLink com o nome privateLinkConfig01 para usar a configuração de IP armazenada em $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="8f2a3-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="8f2a3-111">OS</span><span class="sxs-lookup"><span data-stu-id="8f2a3-111">PARAMETERS</span></span>

### <span data-ttu-id="8f2a3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f2a3-112">-ApplicationGateway</span></span>
<span data-ttu-id="8f2a3-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f2a3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="8f2a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2a3-114">-DefaultProfile</span></span>
<span data-ttu-id="8f2a3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f2a3-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-116">-IpConfiguration</span></span>
<span data-ttu-id="8f2a3-117">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="8f2a3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f2a3-118">-Name</span></span>
<span data-ttu-id="8f2a3-119">O nome da configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="8f2a3-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="8f2a3-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f2a3-120">-Confirm</span></span>
<span data-ttu-id="8f2a3-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f2a3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f2a3-122">-WhatIf</span></span>
<span data-ttu-id="8f2a3-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f2a3-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f2a3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2a3-125">CommonParameters</span></span>
<span data-ttu-id="8f2a3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2a3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2a3-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f2a3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2a3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f2a3-128">INPUTS</span></span>

### <span data-ttu-id="8f2a3-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f2a3-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="8f2a3-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="8f2a3-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="8f2a3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f2a3-131">OUTPUTS</span></span>

### <span data-ttu-id="8f2a3-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8f2a3-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8f2a3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f2a3-133">NOTES</span></span>

## <span data-ttu-id="8f2a3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f2a3-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f2a3-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8f2a3-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8f2a3-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="8f2a3-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8f2a3-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)