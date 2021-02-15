---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzIpAllocation.md
ms.openlocfilehash: 89a0276a94ffa2729c5803a017e297ff05e84534
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114160"
---
# <span data-ttu-id="703c3-101">Get-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="703c3-101">Get-AzIpAllocation</span></span>

## <span data-ttu-id="703c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="703c3-102">SYNOPSIS</span></span>
<span data-ttu-id="703c3-103">Obtém uma Localização IpAllocation do Azure.</span><span class="sxs-lookup"><span data-stu-id="703c3-103">Gets a Azure IpAllocation.</span></span>

## <span data-ttu-id="703c3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="703c3-104">SYNTAX</span></span>

### <span data-ttu-id="703c3-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="703c3-105">GetByNameParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="703c3-106">ListParameterSet</span><span class="sxs-lookup"><span data-stu-id="703c3-106">ListParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="703c3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="703c3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzIpAllocation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="703c3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="703c3-108">DESCRIPTION</span></span>
<span data-ttu-id="703c3-109">O **cmdlet Get-AzIpAllocation** obtém um Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="703c3-109">The **Get-AzIpAllocation** cmdlet gets an Azure IpAllocation</span></span>

## <span data-ttu-id="703c3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="703c3-110">EXAMPLES</span></span>

### <span data-ttu-id="703c3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="703c3-111">Example 1</span></span>
```powershell
Get-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="703c3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="703c3-112">PARAMETERS</span></span>

### <span data-ttu-id="703c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="703c3-113">-DefaultProfile</span></span>
<span data-ttu-id="703c3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="703c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="703c3-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="703c3-115">-Name</span></span>
<span data-ttu-id="703c3-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="703c3-116">The resource name.</span></span>

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

### <span data-ttu-id="703c3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="703c3-117">-ResourceGroupName</span></span>
<span data-ttu-id="703c3-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="703c3-118">The resource group name.</span></span>

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

### <span data-ttu-id="703c3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="703c3-119">-ResourceId</span></span>
<span data-ttu-id="703c3-120">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="703c3-120">IpAllocation Id</span></span>

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

### <span data-ttu-id="703c3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="703c3-121">CommonParameters</span></span>
<span data-ttu-id="703c3-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="703c3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="703c3-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="703c3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="703c3-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="703c3-124">INPUTS</span></span>

### <span data-ttu-id="703c3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="703c3-125">System.String</span></span>

## <span data-ttu-id="703c3-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="703c3-126">OUTPUTS</span></span>

### <span data-ttu-id="703c3-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="703c3-127">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="703c3-128">Notas</span><span class="sxs-lookup"><span data-stu-id="703c3-128">NOTES</span></span>

## <span data-ttu-id="703c3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="703c3-129">RELATED LINKS</span></span>
