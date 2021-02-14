---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117325"
---
# <span data-ttu-id="b77cf-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b77cf-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="b77cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b77cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b77cf-103">Salva uma IpAllocation modificada.</span><span class="sxs-lookup"><span data-stu-id="b77cf-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="b77cf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b77cf-104">SYNTAX</span></span>

### <span data-ttu-id="b77cf-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77cf-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77cf-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77cf-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77cf-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b77cf-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77cf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b77cf-108">DESCRIPTION</span></span>
<span data-ttu-id="b77cf-109">O **cmdlet Set-AzIpAllocation** atualiza uma Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b77cf-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="b77cf-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b77cf-110">EXAMPLES</span></span>

### <span data-ttu-id="b77cf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b77cf-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="b77cf-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b77cf-112">PARAMETERS</span></span>

### <span data-ttu-id="b77cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b77cf-113">-AsJob</span></span>
<span data-ttu-id="b77cf-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b77cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b77cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77cf-115">-DefaultProfile</span></span>
<span data-ttu-id="b77cf-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b77cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b77cf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b77cf-117">-InputObject</span></span>
<span data-ttu-id="b77cf-118">A IpAllocation</span><span class="sxs-lookup"><span data-stu-id="b77cf-118">The IpAllocation</span></span>

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

### <span data-ttu-id="b77cf-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="b77cf-119">-IpAllocationTag</span></span>
<span data-ttu-id="b77cf-120">As marcas de alocação da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="b77cf-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="b77cf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b77cf-121">-Name</span></span>
<span data-ttu-id="b77cf-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b77cf-122">The resource name.</span></span>

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

### <span data-ttu-id="b77cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b77cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="b77cf-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b77cf-124">The resource group name.</span></span>

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

### <span data-ttu-id="b77cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b77cf-125">-ResourceId</span></span>
<span data-ttu-id="b77cf-126">IpAllocation Id</span><span class="sxs-lookup"><span data-stu-id="b77cf-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="b77cf-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b77cf-127">-Tag</span></span>
<span data-ttu-id="b77cf-128">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b77cf-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b77cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77cf-129">CommonParameters</span></span>
<span data-ttu-id="b77cf-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77cf-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b77cf-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77cf-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="b77cf-132">INPUTS</span></span>

### <span data-ttu-id="b77cf-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b77cf-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b77cf-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="b77cf-134">OUTPUTS</span></span>

### <span data-ttu-id="b77cf-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="b77cf-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="b77cf-136">Notas</span><span class="sxs-lookup"><span data-stu-id="b77cf-136">NOTES</span></span>

## <span data-ttu-id="b77cf-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b77cf-137">RELATED LINKS</span></span>
