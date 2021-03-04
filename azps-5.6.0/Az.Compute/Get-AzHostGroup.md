---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: 1b33803ff3a33897d46519952db99ceda1b12c99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890454"
---
# <span data-ttu-id="8f151-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="8f151-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="8f151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f151-102">SYNOPSIS</span></span>
<span data-ttu-id="8f151-103">Obter ou listar hosts.</span><span class="sxs-lookup"><span data-stu-id="8f151-103">Get or list hosts.</span></span>

## <span data-ttu-id="8f151-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8f151-104">SYNTAX</span></span>

### <span data-ttu-id="8f151-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f151-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f151-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8f151-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f151-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8f151-107">DESCRIPTION</span></span>
<span data-ttu-id="8f151-108">Este cmdlet receberá um grupo de host.</span><span class="sxs-lookup"><span data-stu-id="8f151-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="8f151-109">Este cmdlet também lista todos os grupos de host em um grupo de recursos se um nome de grupo de host não for dado.</span><span class="sxs-lookup"><span data-stu-id="8f151-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="8f151-110">Esse cmdlet também lista todos os grupos de host em uma assinatura se nem o nome do grupo de host nem o nome do grupo de recursos for dado.</span><span class="sxs-lookup"><span data-stu-id="8f151-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="8f151-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f151-111">EXAMPLES</span></span>

### <span data-ttu-id="8f151-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8f151-112">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="8f151-113">Este comando retorna um grupo de host.</span><span class="sxs-lookup"><span data-stu-id="8f151-113">This command returns a host group.</span></span>

### <span data-ttu-id="8f151-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8f151-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="8f151-115">Este comando retorna todos os grupos de host no grupo de recursos determinado.</span><span class="sxs-lookup"><span data-stu-id="8f151-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="8f151-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8f151-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="8f151-117">Este comando retorna todos os grupos de host na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8f151-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="8f151-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8f151-118">PARAMETERS</span></span>

### <span data-ttu-id="8f151-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f151-119">-DefaultProfile</span></span>
<span data-ttu-id="8f151-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f151-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f151-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="8f151-121">-InstanceView</span></span>
<span data-ttu-id="8f151-122">Expanda o objeto retornado para também listar os exibições de instância do host.</span><span class="sxs-lookup"><span data-stu-id="8f151-122">Expand the returned object to also list the host's instance views.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f151-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8f151-123">-Name</span></span>
<span data-ttu-id="8f151-124">O nome do grupo host.</span><span class="sxs-lookup"><span data-stu-id="8f151-124">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f151-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f151-125">-ResourceGroupName</span></span>
<span data-ttu-id="8f151-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8f151-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f151-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f151-127">-ResourceId</span></span>
<span data-ttu-id="8f151-128">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8f151-128">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f151-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f151-129">CommonParameters</span></span>
<span data-ttu-id="8f151-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f151-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f151-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f151-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f151-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f151-132">INPUTS</span></span>

### <span data-ttu-id="8f151-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8f151-133">System.String</span></span>

## <span data-ttu-id="8f151-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8f151-134">OUTPUTS</span></span>

### <span data-ttu-id="8f151-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="8f151-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="8f151-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="8f151-136">NOTES</span></span>

## <span data-ttu-id="8f151-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f151-137">RELATED LINKS</span></span>
