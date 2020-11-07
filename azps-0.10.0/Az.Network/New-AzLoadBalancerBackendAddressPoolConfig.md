---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775398"
---
# <span data-ttu-id="869c1-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="869c1-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="869c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="869c1-102">SYNOPSIS</span></span>
<span data-ttu-id="869c1-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="869c1-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="869c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="869c1-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="869c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="869c1-105">DESCRIPTION</span></span>
<span data-ttu-id="869c1-106">O cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços de back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="869c1-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="869c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="869c1-107">EXAMPLES</span></span>

### <span data-ttu-id="869c1-108">Exemplo 1: criar uma configuração de pool de endereços de back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="869c1-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="869c1-109">Esse comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="869c1-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="869c1-110">OS</span><span class="sxs-lookup"><span data-stu-id="869c1-110">PARAMETERS</span></span>

### <span data-ttu-id="869c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="869c1-111">-DefaultProfile</span></span>
<span data-ttu-id="869c1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="869c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="869c1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="869c1-113">-Name</span></span>
<span data-ttu-id="869c1-114">Especifica o nome da configuração do pool de endereços a ser criada.</span><span class="sxs-lookup"><span data-stu-id="869c1-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="869c1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="869c1-115">CommonParameters</span></span>
<span data-ttu-id="869c1-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="869c1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="869c1-117">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="869c1-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="869c1-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="869c1-118">INPUTS</span></span>

## <span data-ttu-id="869c1-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="869c1-119">OUTPUTS</span></span>

### <span data-ttu-id="869c1-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="869c1-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="869c1-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="869c1-121">NOTES</span></span>

## <span data-ttu-id="869c1-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="869c1-122">RELATED LINKS</span></span>

[<span data-ttu-id="869c1-123">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="869c1-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="869c1-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="869c1-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="869c1-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="869c1-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


