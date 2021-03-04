---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885860"
---
# <span data-ttu-id="1c376-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1c376-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="1c376-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c376-102">SYNOPSIS</span></span>
<span data-ttu-id="1c376-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c376-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="1c376-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1c376-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c376-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1c376-105">DESCRIPTION</span></span>
<span data-ttu-id="1c376-106">O cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="1c376-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1c376-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c376-107">EXAMPLES</span></span>

### <span data-ttu-id="1c376-108">Exemplo 1: Criar uma configuração de pool de endereços back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="1c376-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="1c376-109">Este comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="1c376-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="1c376-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1c376-110">PARAMETERS</span></span>

### <span data-ttu-id="1c376-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c376-111">-DefaultProfile</span></span>
<span data-ttu-id="1c376-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1c376-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c376-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1c376-113">-Name</span></span>
<span data-ttu-id="1c376-114">Especifica o nome da configuração do pool de endereços a ser criado.</span><span class="sxs-lookup"><span data-stu-id="1c376-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="1c376-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c376-115">-Confirm</span></span>
<span data-ttu-id="1c376-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c376-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c376-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c376-117">-WhatIf</span></span>
<span data-ttu-id="1c376-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c376-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c376-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c376-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c376-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c376-120">CommonParameters</span></span>
<span data-ttu-id="1c376-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c376-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c376-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c376-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c376-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c376-123">INPUTS</span></span>

### <span data-ttu-id="1c376-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1c376-124">None</span></span>

## <span data-ttu-id="1c376-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1c376-125">OUTPUTS</span></span>

### <span data-ttu-id="1c376-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1c376-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="1c376-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="1c376-127">NOTES</span></span>

## <span data-ttu-id="1c376-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c376-128">RELATED LINKS</span></span>

[<span data-ttu-id="1c376-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1c376-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1c376-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1c376-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="1c376-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="1c376-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


