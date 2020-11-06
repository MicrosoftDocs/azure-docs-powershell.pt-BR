---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430156"
---
# <span data-ttu-id="4af0d-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4af0d-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4af0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4af0d-102">SYNOPSIS</span></span>
<span data-ttu-id="4af0d-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4af0d-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4af0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4af0d-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4af0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4af0d-105">DESCRIPTION</span></span>
<span data-ttu-id="4af0d-106">O cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços de back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="4af0d-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4af0d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4af0d-107">EXAMPLES</span></span>

### <span data-ttu-id="4af0d-108">Exemplo 1: criar uma configuração de pool de endereços de back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="4af0d-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="4af0d-109">Esse comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="4af0d-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="4af0d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4af0d-110">PARAMETERS</span></span>

### <span data-ttu-id="4af0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af0d-111">-DefaultProfile</span></span>
<span data-ttu-id="4af0d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4af0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af0d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4af0d-113">-Name</span></span>
<span data-ttu-id="4af0d-114">Especifica o nome da configuração do pool de endereços a ser criada.</span><span class="sxs-lookup"><span data-stu-id="4af0d-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="4af0d-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4af0d-115">-Confirm</span></span>
<span data-ttu-id="4af0d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af0d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af0d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af0d-117">-WhatIf</span></span>
<span data-ttu-id="4af0d-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4af0d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4af0d-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4af0d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4af0d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af0d-120">CommonParameters</span></span>
<span data-ttu-id="4af0d-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af0d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af0d-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4af0d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af0d-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4af0d-123">INPUTS</span></span>

### <span data-ttu-id="4af0d-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4af0d-124">None</span></span>

## <span data-ttu-id="4af0d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4af0d-125">OUTPUTS</span></span>

### <span data-ttu-id="4af0d-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4af0d-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="4af0d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4af0d-127">NOTES</span></span>

## <span data-ttu-id="4af0d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4af0d-128">RELATED LINKS</span></span>

[<span data-ttu-id="4af0d-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4af0d-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4af0d-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4af0d-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4af0d-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4af0d-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


