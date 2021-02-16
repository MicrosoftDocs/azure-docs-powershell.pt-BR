---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118345"
---
# <span data-ttu-id="919fc-101">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-101">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="919fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="919fc-102">SYNOPSIS</span></span>
<span data-ttu-id="919fc-103">Cria uma configuração de link particular para um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="919fc-103">Creates a private link configuration for an application gateway</span></span>

## <span data-ttu-id="919fc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="919fc-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="919fc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="919fc-105">DESCRIPTION</span></span>
<span data-ttu-id="919fc-106">O cmdlet **New-AzApplicationGatewayPrivateLinkConfiguration** cria uma Configuração do PrivateLink para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="919fc-106">The **New-AzApplicationGatewayPrivateLinkConfiguration** cmdlet creates an PrivateLink Configuration for an Azure application gateway.</span></span>
<span data-ttu-id="919fc-107">A configuração de link particular deve estar associada a uma configuração de ip frontend para habilitar a funcionalidade do link privado.</span><span class="sxs-lookup"><span data-stu-id="919fc-107">The private link configuration must be associated to a frontend ip configuration to enable the private link functionality.</span></span>
<span data-ttu-id="919fc-108">Uma configuração de link particular pode ser associada a apenas uma configuração de ip frontend no gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="919fc-108">One private link configuration can atmost be associated to only one frontend ip configuration on application gateway.</span></span>

## <span data-ttu-id="919fc-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="919fc-109">EXAMPLES</span></span>

### <span data-ttu-id="919fc-110">Exemplo 1: Criar uma Configuração de Link Particular com uma única Configuração ip</span><span class="sxs-lookup"><span data-stu-id="919fc-110">Example 1: Create an Private Link Configuration with single Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

<span data-ttu-id="919fc-111">Esse comando cria uma configuração do PrivateLink chamada "privateLinkConfig01" e armazena o resultado na variável chamada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="919fc-111">This command creates an PrivateLink configuration named 'privateLinkConfig01' and stores the result in the variable named $PrivateLinkConfiguration.</span></span>

### <span data-ttu-id="919fc-112">Exemplo 2: Criar uma Configuração de Link Particular com várias Configurações de Ip</span><span class="sxs-lookup"><span data-stu-id="919fc-112">Example 2: Create an Private Link Configuration with multiple Ip Configurations</span></span>
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

<span data-ttu-id="919fc-113">Esse comando cria uma configuração do PrivateLink chamada "privateLinkConfig01" com duas ipConfigurações e armazena o resultado na variável chamada $PrivateLinkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="919fc-113">This command creates an PrivateLink configuration named 'privateLinkConfig01' with two ipConfigurations and stores the result in the variable named $PrivateLinkConfiguration.</span></span> 

## <span data-ttu-id="919fc-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="919fc-114">PARAMETERS</span></span>

### <span data-ttu-id="919fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919fc-115">-DefaultProfile</span></span>
<span data-ttu-id="919fc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="919fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919fc-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-117">-IpConfiguration</span></span>
<span data-ttu-id="919fc-118">A lista de ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="919fc-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="919fc-119">-Name</span></span>
<span data-ttu-id="919fc-120">O nome da configuração do privateLink</span><span class="sxs-lookup"><span data-stu-id="919fc-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="919fc-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="919fc-121">-Confirm</span></span>
<span data-ttu-id="919fc-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919fc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="919fc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919fc-123">-WhatIf</span></span>
<span data-ttu-id="919fc-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="919fc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919fc-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="919fc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="919fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919fc-126">CommonParameters</span></span>
<span data-ttu-id="919fc-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919fc-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="919fc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919fc-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="919fc-129">INPUTS</span></span>

### <span data-ttu-id="919fc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="919fc-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="919fc-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="919fc-131">OUTPUTS</span></span>

### <span data-ttu-id="919fc-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="919fc-133">Notas</span><span class="sxs-lookup"><span data-stu-id="919fc-133">NOTES</span></span>

## <span data-ttu-id="919fc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="919fc-134">RELATED LINKS</span></span>

[<span data-ttu-id="919fc-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-135">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="919fc-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="919fc-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-137">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="919fc-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="919fc-138">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
