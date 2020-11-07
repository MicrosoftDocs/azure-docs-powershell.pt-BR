---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785686"
---
# <span data-ttu-id="5956a-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="5956a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5956a-102">SYNOPSIS</span></span>
<span data-ttu-id="5956a-103">Cria um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5956a-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5956a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5956a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5956a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5956a-105">DESCRIPTION</span></span>
<span data-ttu-id="5956a-106">O cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** cria um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5956a-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="5956a-107">Um endereço de back-end pode ser especificado como um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou uma ID de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="5956a-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="5956a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5956a-108">EXAMPLES</span></span>

### <span data-ttu-id="5956a-109">Exemplo 1: criar um pool de endereços back-end usando o FQDN de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="5956a-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="5956a-110">Esse comando cria um pool de endereços back-end chamado Pool01 usando os FQDNs dos servidores back-end e armazena-o na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="5956a-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="5956a-111">Exemplo 2: criar um pool de endereços back-end usando o endereço IP de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="5956a-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="5956a-112">Esse comando cria um pool de endereços back-end chamado Pool02 usando os endereços IP dos servidores back-end e os armazena na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="5956a-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="5956a-113">OS</span><span class="sxs-lookup"><span data-stu-id="5956a-113">PARAMETERS</span></span>

### <span data-ttu-id="5956a-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="5956a-114">-BackendFqdns</span></span>
<span data-ttu-id="5956a-115">Especifica uma lista de FQDNs back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="5956a-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="5956a-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="5956a-116">-BackendIPAddresses</span></span>
<span data-ttu-id="5956a-117">Especifica uma lista de endereços IP back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="5956a-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="5956a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5956a-118">-DefaultProfile</span></span>
<span data-ttu-id="5956a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5956a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5956a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5956a-120">-Name</span></span>
<span data-ttu-id="5956a-121">Especifica o nome do pool de servidores back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="5956a-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5956a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5956a-122">-Confirm</span></span>
<span data-ttu-id="5956a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5956a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5956a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5956a-124">-WhatIf</span></span>
<span data-ttu-id="5956a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5956a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5956a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5956a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5956a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5956a-127">CommonParameters</span></span>
<span data-ttu-id="5956a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5956a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5956a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5956a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5956a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5956a-130">INPUTS</span></span>

### <span data-ttu-id="5956a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5956a-131">System.String</span></span>

## <span data-ttu-id="5956a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5956a-132">OUTPUTS</span></span>

### <span data-ttu-id="5956a-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="5956a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5956a-134">NOTES</span></span>

## <span data-ttu-id="5956a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5956a-135">RELATED LINKS</span></span>

[<span data-ttu-id="5956a-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5956a-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5956a-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="5956a-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5956a-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


