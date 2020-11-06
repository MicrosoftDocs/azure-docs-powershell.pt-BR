---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: b57d228ca6b31f84797baa7b2b41073edfa6c3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428188"
---
# <span data-ttu-id="d99ce-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d99ce-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d99ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d99ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d99ce-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="d99ce-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d99ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d99ce-104">SYNTAX</span></span>

### <span data-ttu-id="d99ce-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="d99ce-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d99ce-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="d99ce-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d99ce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d99ce-107">DESCRIPTION</span></span>
<span data-ttu-id="d99ce-108">O cmdlet **Get-AzureRmLoadBalancer** Obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d99ce-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="d99ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d99ce-109">EXAMPLES</span></span>

### <span data-ttu-id="d99ce-110">Exemplo 1: obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="d99ce-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d99ce-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d99ce-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="d99ce-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d99ce-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="d99ce-113">OS</span><span class="sxs-lookup"><span data-stu-id="d99ce-113">PARAMETERS</span></span>

### <span data-ttu-id="d99ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d99ce-114">-DefaultProfile</span></span>
<span data-ttu-id="d99ce-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d99ce-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d99ce-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d99ce-116">-ExpandResource</span></span>
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

### <span data-ttu-id="d99ce-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d99ce-117">-Name</span></span>
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

### <span data-ttu-id="d99ce-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d99ce-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d99ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d99ce-119">CommonParameters</span></span>
<span data-ttu-id="d99ce-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d99ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d99ce-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d99ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d99ce-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d99ce-122">INPUTS</span></span>

### <span data-ttu-id="d99ce-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d99ce-123">None</span></span>
<span data-ttu-id="d99ce-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d99ce-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d99ce-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d99ce-125">OUTPUTS</span></span>

### <span data-ttu-id="d99ce-126">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d99ce-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d99ce-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d99ce-127">NOTES</span></span>

## <span data-ttu-id="d99ce-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d99ce-128">RELATED LINKS</span></span>

[<span data-ttu-id="d99ce-129">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d99ce-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d99ce-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d99ce-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="d99ce-131">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d99ce-131">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


