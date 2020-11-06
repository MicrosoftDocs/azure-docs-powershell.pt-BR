---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: f5be63987e055a7a7b6053820c22522bae021ad3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432178"
---
# <span data-ttu-id="35451-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="35451-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35451-102">SYNOPSIS</span></span>
<span data-ttu-id="35451-103">Cria um pool de endereços back-end para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35451-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35451-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35451-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35451-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35451-105">DESCRIPTION</span></span>
<span data-ttu-id="35451-106">O cmdlet **New-AzureRmApplicationGatewayBackendAddressPool** cria um pool de endereços back-end para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="35451-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="35451-107">Um endereço de back-end pode ser especificado como um endereço IP, um FQDN (nome de domínio totalmente qualificado) ou uma ID de configuração de IP.</span><span class="sxs-lookup"><span data-stu-id="35451-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="35451-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35451-108">EXAMPLES</span></span>

### <span data-ttu-id="35451-109">Exemplo 1: criar um pool de endereços back-end usando o FQDN de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="35451-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="35451-110">Esse comando cria um pool de endereços back-end chamado Pool01 usando os FQDNs dos servidores back-end e armazena-o na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="35451-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="35451-111">Exemplo 2: criar um pool de endereços back-end usando o endereço IP de um servidor back-end</span><span class="sxs-lookup"><span data-stu-id="35451-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="35451-112">Esse comando cria um pool de endereços back-end chamado Pool02 usando os endereços IP dos servidores back-end e os armazena na variável $Pool.</span><span class="sxs-lookup"><span data-stu-id="35451-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="35451-113">OS</span><span class="sxs-lookup"><span data-stu-id="35451-113">PARAMETERS</span></span>

### <span data-ttu-id="35451-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="35451-114">-BackendFqdns</span></span>
<span data-ttu-id="35451-115">Especifica uma lista de FQDNs back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="35451-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="35451-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="35451-116">-BackendIPAddresses</span></span>
<span data-ttu-id="35451-117">Especifica uma lista de endereços IP back-end que este cmdlet associa ao pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="35451-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="35451-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="35451-118">-Name</span></span>
<span data-ttu-id="35451-119">Especifica o nome do pool de servidores back-end que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="35451-119">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="35451-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35451-120">-Confirm</span></span>
<span data-ttu-id="35451-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35451-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35451-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35451-122">-WhatIf</span></span>
<span data-ttu-id="35451-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35451-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35451-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35451-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35451-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35451-125">-DefaultProfile</span></span>
<span data-ttu-id="35451-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35451-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35451-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35451-127">CommonParameters</span></span>
<span data-ttu-id="35451-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35451-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35451-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35451-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35451-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35451-130">INPUTS</span></span>

### <span data-ttu-id="35451-131">System. String</span><span class="sxs-lookup"><span data-stu-id="35451-131">System.String</span></span>

## <span data-ttu-id="35451-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35451-132">OUTPUTS</span></span>

### <span data-ttu-id="35451-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="35451-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35451-134">NOTES</span></span>

## <span data-ttu-id="35451-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35451-135">RELATED LINKS</span></span>

[<span data-ttu-id="35451-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35451-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35451-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="35451-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="35451-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


