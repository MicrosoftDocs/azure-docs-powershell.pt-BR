---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775543"
---
# <span data-ttu-id="305b8-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="305b8-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="305b8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="305b8-102">SYNOPSIS</span></span>
<span data-ttu-id="305b8-103">Obtém um balanceador de carga.</span><span class="sxs-lookup"><span data-stu-id="305b8-103">Gets a load balancer.</span></span>

## <span data-ttu-id="305b8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="305b8-104">SYNTAX</span></span>

### <span data-ttu-id="305b8-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="305b8-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="305b8-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="305b8-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="305b8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="305b8-107">DESCRIPTION</span></span>
<span data-ttu-id="305b8-108">O cmdlet **Get-AzLoadBalancer** Obtém um ou mais balanceadores de carga do Azure contidos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="305b8-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="305b8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="305b8-109">EXAMPLES</span></span>

### <span data-ttu-id="305b8-110">Exemplo 1: obter um balanceador de carga</span><span class="sxs-lookup"><span data-stu-id="305b8-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="305b8-111">Esse comando obtém o balanceador de carga chamado MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="305b8-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="305b8-112">Um balanceador de carga deve existir antes que você possa executar este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="305b8-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="305b8-113">OS</span><span class="sxs-lookup"><span data-stu-id="305b8-113">PARAMETERS</span></span>

### <span data-ttu-id="305b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305b8-114">-DefaultProfile</span></span>
<span data-ttu-id="305b8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="305b8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="305b8-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="305b8-116">-ExpandResource</span></span>
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

### <span data-ttu-id="305b8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="305b8-117">-Name</span></span>
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

### <span data-ttu-id="305b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="305b8-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="305b8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305b8-119">CommonParameters</span></span>
<span data-ttu-id="305b8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305b8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305b8-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305b8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305b8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="305b8-122">INPUTS</span></span>

## <span data-ttu-id="305b8-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="305b8-123">OUTPUTS</span></span>

### <span data-ttu-id="305b8-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="305b8-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="305b8-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="305b8-125">NOTES</span></span>

## <span data-ttu-id="305b8-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="305b8-126">RELATED LINKS</span></span>

[<span data-ttu-id="305b8-127">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="305b8-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="305b8-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="305b8-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="305b8-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="305b8-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


