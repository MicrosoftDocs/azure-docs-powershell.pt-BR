---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: e0d15be05bf5678eb645a2a26dc2459e6790210a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258100"
---
# <span data-ttu-id="606e2-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="606e2-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="606e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="606e2-102">SYNOPSIS</span></span>
<span data-ttu-id="606e2-103">Obtenha ou liste os hosts.</span><span class="sxs-lookup"><span data-stu-id="606e2-103">Get or list hosts.</span></span>

## <span data-ttu-id="606e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="606e2-104">SYNTAX</span></span>

### <span data-ttu-id="606e2-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="606e2-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="606e2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="606e2-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="606e2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="606e2-107">DESCRIPTION</span></span>
<span data-ttu-id="606e2-108">Este cmdlet receberá um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="606e2-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="606e2-109">Esse cmdlet também lista todos os grupos de hosts em um grupo de recursos se um nome de grupo de hosts não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="606e2-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="606e2-110">Esse cmdlet também lista todos os grupos de hosts em uma assinatura, caso nenhum nome de grupo de host nem nome de grupo de recursos seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="606e2-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="606e2-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="606e2-111">EXAMPLES</span></span>

### <span data-ttu-id="606e2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="606e2-112">Example 1</span></span>
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

<span data-ttu-id="606e2-113">Esse comando retorna um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="606e2-113">This command returns a host group.</span></span>

### <span data-ttu-id="606e2-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="606e2-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="606e2-115">Esse comando retorna todos os grupos de hosts no grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="606e2-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="606e2-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="606e2-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="606e2-117">Esse comando retorna todos os grupos de hosts da assinatura.</span><span class="sxs-lookup"><span data-stu-id="606e2-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="606e2-118">OS</span><span class="sxs-lookup"><span data-stu-id="606e2-118">PARAMETERS</span></span>

### <span data-ttu-id="606e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="606e2-119">-DefaultProfile</span></span>
<span data-ttu-id="606e2-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="606e2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="606e2-121">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="606e2-121">-InstanceView</span></span>
<span data-ttu-id="606e2-122">Expanda o objeto retornado para relacionar também os modos de exibição de instância do host.</span><span class="sxs-lookup"><span data-stu-id="606e2-122">Expand the returned object to also list the host's instance views.</span></span> 

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

### <span data-ttu-id="606e2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="606e2-123">-Name</span></span>
<span data-ttu-id="606e2-124">O nome do grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="606e2-124">The name of the host group.</span></span>

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

### <span data-ttu-id="606e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="606e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="606e2-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="606e2-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="606e2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="606e2-127">-ResourceId</span></span>
<span data-ttu-id="606e2-128">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="606e2-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="606e2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606e2-129">CommonParameters</span></span>
<span data-ttu-id="606e2-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606e2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606e2-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="606e2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606e2-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="606e2-132">INPUTS</span></span>

### <span data-ttu-id="606e2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="606e2-133">System.String</span></span>

## <span data-ttu-id="606e2-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="606e2-134">OUTPUTS</span></span>

### <span data-ttu-id="606e2-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="606e2-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="606e2-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="606e2-136">NOTES</span></span>

## <span data-ttu-id="606e2-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="606e2-137">RELATED LINKS</span></span>
