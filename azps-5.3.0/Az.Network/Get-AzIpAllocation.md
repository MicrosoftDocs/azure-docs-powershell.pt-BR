---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433484"
---
# <span data-ttu-id="2a2b7-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="2a2b7-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="2a2b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2b7-103">Obtém um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="2a2b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a2b7-104">SYNTAX</span></span>

### <span data-ttu-id="2a2b7-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a2b7-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2b7-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a2b7-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a2b7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a2b7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a2b7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a2b7-108">DESCRIPTION</span></span>
<span data-ttu-id="2a2b7-109">O cmdlet **Get-AzIpAllocation** Obtém um IpAllocation do Azure</span><span class="sxs-lookup"><span data-stu-id="2a2b7-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="2a2b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a2b7-110">EXAMPLES</span></span>

### <span data-ttu-id="2a2b7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2a2b7-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="2a2b7-112">OS</span><span class="sxs-lookup"><span data-stu-id="2a2b7-112">PARAMETERS</span></span>

### <span data-ttu-id="2a2b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2b7-113">-DefaultProfile</span></span>
<span data-ttu-id="2a2b7-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2b7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a2b7-115">-Name</span></span>
<span data-ttu-id="2a2b7-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a2b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a2b7-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a2b7-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a2b7-119">-ResourceId</span></span>
<span data-ttu-id="2a2b7-120">ID do IpAllocation</span><span class="sxs-lookup"><span data-stu-id="2a2b7-120">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a2b7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2b7-121">CommonParameters</span></span>
<span data-ttu-id="2a2b7-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a2b7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2b7-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a2b7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2b7-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a2b7-124">INPUTS</span></span>

### <span data-ttu-id="2a2b7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2b7-125">System.String</span></span>

## <span data-ttu-id="2a2b7-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a2b7-126">OUTPUTS</span></span>

### <span data-ttu-id="2a2b7-127">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="2a2b7-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="2a2b7-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a2b7-128">NOTES</span></span>

## <span data-ttu-id="2a2b7-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a2b7-129">RELATED LINKS</span></span>
