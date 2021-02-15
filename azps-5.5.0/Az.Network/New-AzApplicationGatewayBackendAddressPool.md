---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117429"
---
# <span data-ttu-id="60bff-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="60bff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60bff-102">SYNOPSIS</span></span>
<span data-ttu-id="60bff-103">Cria um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="60bff-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="60bff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60bff-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60bff-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="60bff-105">DESCRIPTION</span></span>
<span data-ttu-id="60bff-106">O cmdlet **New-AzApplicationGatewayBackendAddressPool** cria um pool de endereços back-end para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="60bff-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="60bff-107">Um endereço back-end pode ser especificado como um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou uma ID de configuração IP.</span><span class="sxs-lookup"><span data-stu-id="60bff-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="60bff-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60bff-108">EXAMPLES</span></span>

### <span data-ttu-id="60bff-109">Exemplo 1: Criar um pool de endereços back-end usando o FQDN de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="60bff-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="60bff-110">Esse comando cria um pool de endereços back-end chamado Pool01 usando os FQDNs de servidores back-end e o armazena na variável $Pool back-end.</span><span class="sxs-lookup"><span data-stu-id="60bff-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="60bff-111">Exemplo 2: Criar um pool de endereços back-end usando o endereço IP de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="60bff-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="60bff-112">Esse comando cria um pool de endereços back-end chamado Pool02 usando os endereços IP de servidores back-end e armazena-o na variável $Pool dados.</span><span class="sxs-lookup"><span data-stu-id="60bff-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="60bff-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60bff-113">PARAMETERS</span></span>

### <span data-ttu-id="60bff-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="60bff-114">-BackendFqdns</span></span>
<span data-ttu-id="60bff-115">Especifica uma lista de FQDNs back-end que esse cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="60bff-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="60bff-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="60bff-116">-BackendIPAddresses</span></span>
<span data-ttu-id="60bff-117">Especifica uma lista de endereços IP de back-end que esse cmdlet associa ao pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="60bff-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="60bff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60bff-118">-DefaultProfile</span></span>
<span data-ttu-id="60bff-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="60bff-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60bff-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60bff-120">-Name</span></span>
<span data-ttu-id="60bff-121">Especifica o nome do pool de servidor back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="60bff-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60bff-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="60bff-122">-Confirm</span></span>
<span data-ttu-id="60bff-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60bff-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60bff-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60bff-124">-WhatIf</span></span>
<span data-ttu-id="60bff-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="60bff-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60bff-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60bff-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60bff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60bff-127">CommonParameters</span></span>
<span data-ttu-id="60bff-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60bff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60bff-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60bff-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60bff-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="60bff-130">INPUTS</span></span>

### <span data-ttu-id="60bff-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="60bff-131">None</span></span>

## <span data-ttu-id="60bff-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="60bff-132">OUTPUTS</span></span>

### <span data-ttu-id="60bff-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="60bff-134">Notas</span><span class="sxs-lookup"><span data-stu-id="60bff-134">NOTES</span></span>

## <span data-ttu-id="60bff-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60bff-135">RELATED LINKS</span></span>

[<span data-ttu-id="60bff-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="60bff-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="60bff-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="60bff-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="60bff-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


