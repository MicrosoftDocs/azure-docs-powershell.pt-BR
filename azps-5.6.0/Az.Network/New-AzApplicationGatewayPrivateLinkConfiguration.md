---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 7c338f49191071bfa48214e65f79e196a75650eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888096"
---
# <span data-ttu-id="ea024-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ea024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea024-102">SYNOPSIS</span></span>
<span data-ttu-id="ea024-103">Cria uma configuração de link privado para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="ea024-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="ea024-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ea024-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea024-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ea024-105">DESCRIPTION</span></span>
<span data-ttu-id="ea024-106">O cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** cria uma Configuração de PrivateLink para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ea024-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="ea024-107">A configuração de link privado deve estar associada a uma configuração de ip front-end para habilitar a funcionalidade de link privado.</span><span class="sxs-lookup"><span data-stu-id="ea024-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="ea024-108">Uma configuração de link privado pode ser associada apenas a uma configuração de ip front-end no gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea024-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="ea024-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea024-109">EXAMPLES</span></span>

### <span data-ttu-id="ea024-110">Exemplo 1: Criar uma configuração de link privado com configuração ip única</span><span class="sxs-lookup"><span data-stu-id="ea024-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="ea024-111">Este comando cria uma configuração privateLink chamada "privateLinkConfig01" e armazena o resultado na variável chamada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea024-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="ea024-112">Exemplo 2: Criar uma configuração de link privado com várias configurações ip</span><span class="sxs-lookup"><span data-stu-id="ea024-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="ea024-113">Este comando cria uma configuração privateLink chamada 'privateLinkConfig01' com dois ipConfigurations e armazena o resultado na variável denominada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea024-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="ea024-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ea024-114">PARAMETERS</span></span>

### <span data-ttu-id="ea024-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea024-115">-DefaultProfile</span></span>
<span data-ttu-id="ea024-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea024-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea024-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-117">-IpConfiguration</span></span>
<span data-ttu-id="ea024-118">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="ea024-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea024-119">-Name</span></span>
<span data-ttu-id="ea024-120">O nome da configuração privateLink</span><span class="sxs-lookup"><span data-stu-id="ea024-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="ea024-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea024-121">-Confirm</span></span>
<span data-ttu-id="ea024-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea024-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea024-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea024-123">-WhatIf</span></span>
<span data-ttu-id="ea024-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea024-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea024-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea024-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea024-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea024-126">CommonParameters</span></span>
<span data-ttu-id="ea024-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea024-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea024-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea024-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea024-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea024-129">INPUTS</span></span>

### <span data-ttu-id="ea024-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="ea024-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="ea024-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ea024-131">OUTPUTS</span></span>

### <span data-ttu-id="ea024-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="ea024-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="ea024-133">NOTES</span></span>

## <span data-ttu-id="ea024-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea024-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea024-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ea024-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ea024-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="ea024-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea024-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
