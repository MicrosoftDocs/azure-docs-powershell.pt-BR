---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 0bc3d62ad690ab8bed961045ce46448af8700bd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889212"
---
# <span data-ttu-id="d59c6-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="d59c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d59c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d59c6-103">Adiciona uma configuração de link privado a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d59c6-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="d59c6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d59c6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d59c6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d59c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d59c6-106">O cmdlet **Add-AzApplicationGatewayPrivateLinkConfiguration** adiciona uma configuração de link privado a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d59c6-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="d59c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d59c6-107">EXAMPLES</span></span>

### <span data-ttu-id="d59c6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d59c6-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="d59c6-109">O primeiro comando cria um privateLinkIpConfiguration e o armazena na variável $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d59c6-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="d59c6-110">O segundo comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d59c6-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d59c6-111">O terceiro comando adiciona a configuração de link privado chamada privateLinkConfig01, para o gateway no $AppGw</span><span class="sxs-lookup"><span data-stu-id="d59c6-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="d59c6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d59c6-112">PARAMETERS</span></span>

### <span data-ttu-id="d59c6-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d59c6-113">-ApplicationGateway</span></span>
<span data-ttu-id="d59c6-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d59c6-114">The applicationGateway</span></span>

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

### <span data-ttu-id="d59c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d59c6-115">-DefaultProfile</span></span>
<span data-ttu-id="d59c6-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d59c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d59c6-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-117">-IpConfiguration</span></span>
<span data-ttu-id="d59c6-118">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="d59c6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d59c6-119">-Name</span></span>
<span data-ttu-id="d59c6-120">O nome da configuração privateLink</span><span class="sxs-lookup"><span data-stu-id="d59c6-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="d59c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d59c6-121">CommonParameters</span></span>
<span data-ttu-id="d59c6-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d59c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d59c6-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d59c6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d59c6-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d59c6-124">INPUTS</span></span>

### <span data-ttu-id="d59c6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d59c6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="d59c6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="d59c6-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="d59c6-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d59c6-127">OUTPUTS</span></span>

### <span data-ttu-id="d59c6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d59c6-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d59c6-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="d59c6-129">NOTES</span></span>

## <span data-ttu-id="d59c6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d59c6-130">RELATED LINKS</span></span>

[<span data-ttu-id="d59c6-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d59c6-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d59c6-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="d59c6-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="d59c6-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)