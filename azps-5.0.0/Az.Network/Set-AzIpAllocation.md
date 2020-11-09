---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpAllocation.md
ms.openlocfilehash: 4d817dcabe73972b3a8f21de5b9b0906d7a95cc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283857"
---
# <span data-ttu-id="99fa9-101">Set-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-101">Set-AzIpAllocation</span></span>

## <span data-ttu-id="99fa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="99fa9-103">Salva uma IpAllocation modificada.</span><span class="sxs-lookup"><span data-stu-id="99fa9-103">Saves a modified IpAllocation.</span></span>

## <span data-ttu-id="99fa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99fa9-104">SYNTAX</span></span>

### <span data-ttu-id="99fa9-105">SetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99fa9-105">SetByNameParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceGroupName] <String> [-Name] <String> [-IpAllocationTag <Hashtable>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99fa9-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99fa9-106">SetByResourceIdParameterSet</span></span>
```
Set-AzIpAllocation [-ResourceId] <String> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99fa9-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99fa9-107">SetByInputObjectParameterSet</span></span>
```
Set-AzIpAllocation [-InputObject] <PSIpAllocation> [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99fa9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99fa9-108">DESCRIPTION</span></span>
<span data-ttu-id="99fa9-109">O cmdlet **set-AzIpAllocation** atualiza um Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-109">The **Set-AzIpAllocation** cmdlet updates an Azure IpAllocation</span></span>

## <span data-ttu-id="99fa9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99fa9-110">EXAMPLES</span></span>

### <span data-ttu-id="99fa9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99fa9-111">Example 1</span></span>
```powershell
Set-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'  -IpAllocationTag @{"VnetId"="vnet1"}  -Tag @{"TestTag"="TestValue"}
```

## <span data-ttu-id="99fa9-112">OS</span><span class="sxs-lookup"><span data-stu-id="99fa9-112">PARAMETERS</span></span>

### <span data-ttu-id="99fa9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99fa9-113">-AsJob</span></span>
<span data-ttu-id="99fa9-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="99fa9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99fa9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fa9-115">-DefaultProfile</span></span>
<span data-ttu-id="99fa9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99fa9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99fa9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99fa9-117">-InputObject</span></span>
<span data-ttu-id="99fa9-118">O IpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-118">The IpAllocation</span></span>

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

### <span data-ttu-id="99fa9-119">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="99fa9-119">-IpAllocationTag</span></span>
<span data-ttu-id="99fa9-120">As marcas de alocação da alocação de IP</span><span class="sxs-lookup"><span data-stu-id="99fa9-120">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="99fa9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="99fa9-121">-Name</span></span>
<span data-ttu-id="99fa9-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="99fa9-122">The resource name.</span></span>

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

### <span data-ttu-id="99fa9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99fa9-123">-ResourceGroupName</span></span>
<span data-ttu-id="99fa9-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99fa9-124">The resource group name.</span></span>

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

### <span data-ttu-id="99fa9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99fa9-125">-ResourceId</span></span>
<span data-ttu-id="99fa9-126">ID do IpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-126">IpAllocation Id</span></span>

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

### <span data-ttu-id="99fa9-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="99fa9-127">-Tag</span></span>
<span data-ttu-id="99fa9-128">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="99fa9-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="99fa9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fa9-129">CommonParameters</span></span>
<span data-ttu-id="99fa9-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99fa9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fa9-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99fa9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fa9-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99fa9-132">INPUTS</span></span>

### <span data-ttu-id="99fa9-133">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-133">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="99fa9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99fa9-134">OUTPUTS</span></span>

### <span data-ttu-id="99fa9-135">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="99fa9-135">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="99fa9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99fa9-136">NOTES</span></span>

## <span data-ttu-id="99fa9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99fa9-137">RELATED LINKS</span></span>
