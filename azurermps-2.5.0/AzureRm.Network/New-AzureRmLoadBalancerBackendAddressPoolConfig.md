---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785671"
---
# <span data-ttu-id="0af92-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0af92-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="0af92-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0af92-102">SYNOPSIS</span></span>
<span data-ttu-id="0af92-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0af92-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0af92-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0af92-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0af92-105">DESCRIPTION</span></span>
<span data-ttu-id="0af92-106">O cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços de back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="0af92-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0af92-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0af92-107">EXAMPLES</span></span>

### <span data-ttu-id="0af92-108">Exemplo 1: criar uma configuração de pool de endereços de back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="0af92-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="0af92-109">Esse comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="0af92-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="0af92-110">OS</span><span class="sxs-lookup"><span data-stu-id="0af92-110">PARAMETERS</span></span>

### <span data-ttu-id="0af92-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af92-111">-DefaultProfile</span></span>
<span data-ttu-id="0af92-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0af92-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af92-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0af92-113">-Name</span></span>
<span data-ttu-id="0af92-114">Especifica o nome da configuração do pool de endereços a ser criada.</span><span class="sxs-lookup"><span data-stu-id="0af92-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="0af92-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af92-115">CommonParameters</span></span>
<span data-ttu-id="0af92-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0af92-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af92-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af92-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af92-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0af92-118">INPUTS</span></span>

## <span data-ttu-id="0af92-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0af92-119">OUTPUTS</span></span>

### <span data-ttu-id="0af92-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0af92-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="0af92-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0af92-121">NOTES</span></span>

## <span data-ttu-id="0af92-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0af92-122">RELATED LINKS</span></span>

[<span data-ttu-id="0af92-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0af92-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="0af92-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0af92-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="0af92-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0af92-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


