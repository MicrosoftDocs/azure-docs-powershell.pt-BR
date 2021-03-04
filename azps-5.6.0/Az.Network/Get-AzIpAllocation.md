---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: c08a148d1c58e08daa2fce8cd1e195887a264f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885999"
---
# <span data-ttu-id="52b0b-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="52b0b-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="52b0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="52b0b-103">Obtém um IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="52b0b-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="52b0b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52b0b-104">SYNTAX</span></span>

### <span data-ttu-id="52b0b-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b0b-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52b0b-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b0b-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="52b0b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b0b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b0b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52b0b-108">DESCRIPTION</span></span>
<span data-ttu-id="52b0b-109">O cmdlet **Get-AzIpAllocation** obtém um IpAllocation do Azure</span><span class="sxs-lookup"><span data-stu-id="52b0b-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="52b0b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52b0b-110">EXAMPLES</span></span>

### <span data-ttu-id="52b0b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52b0b-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="52b0b-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="52b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="52b0b-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52b0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b0b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="52b0b-115">-Name</span></span>
<span data-ttu-id="52b0b-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="52b0b-116">The resource name.</span></span>

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

### <span data-ttu-id="52b0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="52b0b-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="52b0b-118">The resource group name.</span></span>

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

### <span data-ttu-id="52b0b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52b0b-119">-ResourceId</span></span>
<span data-ttu-id="52b0b-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="52b0b-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="52b0b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b0b-121">CommonParameters</span></span>
<span data-ttu-id="52b0b-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b0b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b0b-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52b0b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b0b-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52b0b-124">INPUTS</span></span>

### <span data-ttu-id="52b0b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="52b0b-125">System.String</span></span>

## <span data-ttu-id="52b0b-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52b0b-126">OUTPUTS</span></span>

### <span data-ttu-id="52b0b-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="52b0b-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="52b0b-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="52b0b-128">NOTES</span></span>

## <span data-ttu-id="52b0b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52b0b-129">RELATED LINKS</span></span>
