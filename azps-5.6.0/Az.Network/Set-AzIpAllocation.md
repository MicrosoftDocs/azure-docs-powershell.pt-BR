---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: e03ec2b7f2ceba70ba3037bbcad232dbfa7490de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888453"
---
# <span data-ttu-id="17173-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="17173-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="17173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17173-102">SYNOPSIS</span></span>
<span data-ttu-id="17173-103">Salva um IpAllocation modificado.</span><span class="sxs-lookup"><span data-stu-id="17173-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="17173-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="17173-104">SYNTAX</span></span>

### <span data-ttu-id="17173-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="17173-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17173-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17173-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17173-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17173-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17173-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="17173-108">DESCRIPTION</span></span>
<span data-ttu-id="17173-109">O cmdlet **Set-AzIpAllocation** atualiza um IpAllocation do Azure</span><span class="sxs-lookup"><span data-stu-id="17173-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="17173-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="17173-110">EXAMPLES</span></span>

### <span data-ttu-id="17173-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17173-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="17173-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="17173-112">PARAMETERS</span></span>

### <span data-ttu-id="17173-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17173-113">-AsJob</span></span>
<span data-ttu-id="17173-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="17173-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17173-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17173-115">-DefaultProfile</span></span>
<span data-ttu-id="17173-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17173-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17173-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17173-117">-InputObject</span></span>
<span data-ttu-id="17173-118">The IpAllocation</span><span class="sxs-lookup"><span data-stu-id="17173-118">The IpAllocation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpAllocation
Parameter Sets: SetByInputObjectParameterSet
Aliases: IpAllocation

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17173-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="17173-119">-IpAllocationTag</span></span>
<span data-ttu-id="17173-120">As marcas de alocação da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="17173-120">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17173-121">-Name</span><span class="sxs-lookup"><span data-stu-id="17173-121">-Name</span></span>
<span data-ttu-id="17173-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="17173-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17173-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17173-123">-ResourceGroupName</span></span>
<span data-ttu-id="17173-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17173-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17173-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17173-125">-ResourceId</span></span>
<span data-ttu-id="17173-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="17173-126">IpAllocation Id</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases: IpAllocationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17173-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="17173-127">-Tag</span></span>
<span data-ttu-id="17173-128">Uma hashtable que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="17173-128">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17173-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17173-129">CommonParameters</span></span>
<span data-ttu-id="17173-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17173-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17173-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17173-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17173-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="17173-132">INPUTS</span></span>

### <span data-ttu-id="17173-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="17173-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="17173-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="17173-134">OUTPUTS</span></span>

### <span data-ttu-id="17173-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="17173-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="17173-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="17173-136">NOTES</span></span>

## <span data-ttu-id="17173-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17173-137">RELATED LINKS</span></span>
