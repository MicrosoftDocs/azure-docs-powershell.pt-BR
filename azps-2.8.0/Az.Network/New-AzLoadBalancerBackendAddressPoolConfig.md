---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f2ee5f5c740ce8ffb1a791405e3713e269a1a54b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771626"
---
# <span data-ttu-id="e13a9-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e13a9-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e13a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e13a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e13a9-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e13a9-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e13a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e13a9-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e13a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e13a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e13a9-106">O cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços de back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="e13a9-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e13a9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e13a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e13a9-108">Exemplo 1: criar uma configuração de pool de endereços de back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="e13a9-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e13a9-109">Esse comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="e13a9-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e13a9-110">OS</span><span class="sxs-lookup"><span data-stu-id="e13a9-110">PARAMETERS</span></span>

### <span data-ttu-id="e13a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13a9-111">-DefaultProfile</span></span>
<span data-ttu-id="e13a9-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e13a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e13a9-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e13a9-113">-Name</span></span>
<span data-ttu-id="e13a9-114">Especifica o nome da configuração do pool de endereços a ser criada.</span><span class="sxs-lookup"><span data-stu-id="e13a9-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="e13a9-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e13a9-115">-Confirm</span></span>
<span data-ttu-id="e13a9-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e13a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13a9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13a9-117">-WhatIf</span></span>
<span data-ttu-id="e13a9-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e13a9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e13a9-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e13a9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e13a9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13a9-120">CommonParameters</span></span>
<span data-ttu-id="e13a9-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13a9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13a9-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13a9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13a9-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e13a9-123">INPUTS</span></span>

### <span data-ttu-id="e13a9-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e13a9-124">None</span></span>

## <span data-ttu-id="e13a9-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e13a9-125">OUTPUTS</span></span>

### <span data-ttu-id="e13a9-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e13a9-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e13a9-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e13a9-127">NOTES</span></span>

## <span data-ttu-id="e13a9-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e13a9-128">RELATED LINKS</span></span>

[<span data-ttu-id="e13a9-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e13a9-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e13a9-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e13a9-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e13a9-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e13a9-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


