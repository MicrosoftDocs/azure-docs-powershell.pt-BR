---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a810d85a96bd0686ca4ac98b7feb0dd4f905bd9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440608"
---
# <span data-ttu-id="65b64-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="65b64-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="65b64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65b64-102">SYNOPSIS</span></span>
<span data-ttu-id="65b64-103">Cria uma configuração de pool de endereços back-end para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="65b64-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65b64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65b64-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65b64-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65b64-105">DESCRIPTION</span></span>
<span data-ttu-id="65b64-106">O cmdlet **New-AzureRmLoadBalancerBackendAddressPoolConfig** cria uma configuração de pool de endereços de back-end para um balanceador de carga do Azure.</span><span class="sxs-lookup"><span data-stu-id="65b64-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="65b64-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65b64-107">EXAMPLES</span></span>

### <span data-ttu-id="65b64-108">Exemplo 1: criar uma configuração de pool de endereços de back-end para um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="65b64-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="65b64-109">Esse comando cria uma configuração de pool de endereços back-end chamada BackendAddressPool02 para um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="65b64-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="65b64-110">OS</span><span class="sxs-lookup"><span data-stu-id="65b64-110">PARAMETERS</span></span>

### <span data-ttu-id="65b64-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="65b64-111">-Name</span></span>
<span data-ttu-id="65b64-112">Especifica o nome da configuração do pool de endereços a ser criada.</span><span class="sxs-lookup"><span data-stu-id="65b64-112">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="65b64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b64-113">-DefaultProfile</span></span>
<span data-ttu-id="65b64-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65b64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65b64-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b64-115">CommonParameters</span></span>
<span data-ttu-id="65b64-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b64-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b64-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65b64-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b64-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65b64-118">INPUTS</span></span>

## <span data-ttu-id="65b64-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65b64-119">OUTPUTS</span></span>

### <span data-ttu-id="65b64-120">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="65b64-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="65b64-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65b64-121">NOTES</span></span>

## <span data-ttu-id="65b64-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65b64-122">RELATED LINKS</span></span>

[<span data-ttu-id="65b64-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="65b64-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="65b64-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="65b64-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="65b64-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="65b64-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


