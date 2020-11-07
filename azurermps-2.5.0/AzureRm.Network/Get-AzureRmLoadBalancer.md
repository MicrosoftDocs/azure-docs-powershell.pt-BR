---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 39bbf3a30f4334e35f58109da86b9b07208682af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785711"
---
# <span data-ttu-id="d6711-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6711-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d6711-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6711-102">SYNOPSIS</span></span>
<span data-ttu-id="d6711-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d6711-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6711-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6711-104">SYNTAX</span></span>

### <span data-ttu-id="d6711-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="d6711-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6711-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="d6711-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6711-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6711-107">DESCRIPTION</span></span>
<span data-ttu-id="d6711-108">O cmdlet **Get-AzureRmLoadBalancer** Obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d6711-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="d6711-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6711-109">EXAMPLES</span></span>

### <span data-ttu-id="d6711-110">Exemplo 1: obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d6711-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d6711-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d6711-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="d6711-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6711-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="d6711-113">OS</span><span class="sxs-lookup"><span data-stu-id="d6711-113">PARAMETERS</span></span>

### <span data-ttu-id="d6711-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6711-114">-DefaultProfile</span></span>
<span data-ttu-id="d6711-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6711-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6711-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d6711-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6711-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6711-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6711-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6711-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6711-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6711-119">CommonParameters</span></span>
<span data-ttu-id="d6711-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6711-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6711-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6711-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6711-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6711-122">INPUTS</span></span>

## <span data-ttu-id="d6711-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6711-123">OUTPUTS</span></span>

### <span data-ttu-id="d6711-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6711-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d6711-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6711-125">NOTES</span></span>

## <span data-ttu-id="d6711-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6711-126">RELATED LINKS</span></span>

[<span data-ttu-id="d6711-127">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6711-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d6711-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6711-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="d6711-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d6711-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


