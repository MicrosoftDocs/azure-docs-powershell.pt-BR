---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114213"
---
# <span data-ttu-id="badf0-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="badf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="badf0-102">SYNOPSIS</span></span>
<span data-ttu-id="badf0-103">Adiciona uma configuração de link particular a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="badf0-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="badf0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="badf0-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="badf0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="badf0-105">DESCRIPTION</span></span>
<span data-ttu-id="badf0-106">O **cmdlet Add-AzApplicationGatewayPrivateLinkConfiguration** adiciona uma configuração de link particular a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="badf0-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="badf0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="badf0-107">EXAMPLES</span></span>

### <span data-ttu-id="badf0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="badf0-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="badf0-109">O primeiro comando cria uma propriedadeLinkIpConfiguration e a armazena na variável $PrivateLinkIpConfiguration privada.</span><span class="sxs-lookup"><span data-stu-id="badf0-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="badf0-110">O segundo comando obtém o gateway de aplicativo chamado ApplicationGateway01 que pertence ao grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="badf0-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="badf0-111">O terceiro comando adiciona a configuração de link particular chamada privateLinkConfig01 para o gateway no $AppGw</span><span class="sxs-lookup"><span data-stu-id="badf0-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="badf0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="badf0-112">PARAMETERS</span></span>

### <span data-ttu-id="badf0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="badf0-113">-ApplicationGateway</span></span>
<span data-ttu-id="badf0-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="badf0-114">The applicationGateway</span></span>

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

### <span data-ttu-id="badf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="badf0-115">-DefaultProfile</span></span>
<span data-ttu-id="badf0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="badf0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="badf0-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-117">-IpConfiguration</span></span>
<span data-ttu-id="badf0-118">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="badf0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="badf0-119">-Name</span></span>
<span data-ttu-id="badf0-120">O nome da configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="badf0-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="badf0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="badf0-121">CommonParameters</span></span>
<span data-ttu-id="badf0-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="badf0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="badf0-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="badf0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="badf0-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="badf0-124">INPUTS</span></span>

### <span data-ttu-id="badf0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="badf0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="badf0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="badf0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="badf0-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="badf0-127">OUTPUTS</span></span>

### <span data-ttu-id="badf0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="badf0-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="badf0-129">Notas</span><span class="sxs-lookup"><span data-stu-id="badf0-129">NOTES</span></span>

## <span data-ttu-id="badf0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="badf0-130">RELATED LINKS</span></span>

[<span data-ttu-id="badf0-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="badf0-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="badf0-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="badf0-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="badf0-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)