---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 961580d6354c6916ad811d6f8bccd4119d8b07a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775444"
---
# <span data-ttu-id="533a3-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="533a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="533a3-102">SYNOPSIS</span></span>
<span data-ttu-id="533a3-103">Cria um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="533a3-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="533a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="533a3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="533a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="533a3-105">DESCRIPTION</span></span>
<span data-ttu-id="533a3-106">O cmdlet **New-AzApplicationGatewayBackendAddressPool** cria um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="533a3-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="533a3-107">Um endereço de back-end pode ser especificado como um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou uma ID de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="533a3-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="533a3-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="533a3-108">EXAMPLES</span></span>

### <span data-ttu-id="533a3-109">Exemplo 1: criar um pool de endereços back-end usando o FQDN de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="533a3-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="533a3-110">Esse comando cria um pool de endereços back-end chamado Pool01 usando os FQDNs dos servidores back-end e armazena-o na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="533a3-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="533a3-111">Exemplo 2: criar um pool de endereços back-end usando o endereço IP de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="533a3-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="533a3-112">Esse comando cria um pool de endereços back-end chamado Pool02 usando os endereços IP dos servidores back-end e os armazena na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="533a3-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="533a3-113">OS</span><span class="sxs-lookup"><span data-stu-id="533a3-113">PARAMETERS</span></span>

### <span data-ttu-id="533a3-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="533a3-114">-BackendFqdns</span></span>
<span data-ttu-id="533a3-115">Especifica uma lista de FQDNs back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="533a3-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533a3-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="533a3-116">-BackendIPAddresses</span></span>
<span data-ttu-id="533a3-117">Especifica uma lista de endereços IP back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="533a3-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533a3-118">-DefaultProfile</span></span>
<span data-ttu-id="533a3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="533a3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533a3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="533a3-120">-Name</span></span>
<span data-ttu-id="533a3-121">Especifica o nome do pool de servidores back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="533a3-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="533a3-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="533a3-122">-Confirm</span></span>
<span data-ttu-id="533a3-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="533a3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533a3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="533a3-124">-WhatIf</span></span>
<span data-ttu-id="533a3-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="533a3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="533a3-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="533a3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="533a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533a3-127">CommonParameters</span></span>
<span data-ttu-id="533a3-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="533a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533a3-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="533a3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533a3-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="533a3-130">INPUTS</span></span>

### <span data-ttu-id="533a3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="533a3-131">System.String</span></span>

## <span data-ttu-id="533a3-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="533a3-132">OUTPUTS</span></span>

### <span data-ttu-id="533a3-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="533a3-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="533a3-134">NOTES</span></span>

## <span data-ttu-id="533a3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="533a3-135">RELATED LINKS</span></span>

[<span data-ttu-id="533a3-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="533a3-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="533a3-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="533a3-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="533a3-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

