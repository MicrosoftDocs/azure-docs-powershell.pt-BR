---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHostGroup.md
ms.openlocfilehash: a87a11b1e894864593d9558b123b19b6bda06e11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597472"
---
# <span data-ttu-id="9f40b-101">Get-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="9f40b-101">Get-AzHostGroup</span></span>

## <span data-ttu-id="9f40b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f40b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f40b-103">Obtenha ou liste os hosts.</span><span class="sxs-lookup"><span data-stu-id="9f40b-103">Get or list hosts.</span></span>

## <span data-ttu-id="9f40b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f40b-104">SYNTAX</span></span>

### <span data-ttu-id="9f40b-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="9f40b-105">DefaultParameter (Default)</span></span>
```
Get-AzHostGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f40b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9f40b-106">ResourceIdParameter</span></span>
```
Get-AzHostGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f40b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f40b-107">DESCRIPTION</span></span>
<span data-ttu-id="9f40b-108">Este cmdlet receberá um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="9f40b-108">This cmdlet will get a host group.</span></span>
<span data-ttu-id="9f40b-109">Esse cmdlet também lista todos os grupos de hosts em um grupo de recursos se um nome de grupo de hosts não for fornecido.</span><span class="sxs-lookup"><span data-stu-id="9f40b-109">This cmdlet also lists all host groups in a resource group if a host group name is not given.</span></span>
<span data-ttu-id="9f40b-110">Esse cmdlet também lista todos os grupos de hosts em uma assinatura, caso nenhum nome de grupo de host nem nome de grupo de recursos seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="9f40b-110">This cmdlet also lists all host groups in a subscription if neither host group name nor resource group name is given.</span></span>

## <span data-ttu-id="9f40b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f40b-111">EXAMPLES</span></span>

### <span data-ttu-id="9f40b-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f40b-112">Example 1</span></span>
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

<span data-ttu-id="9f40b-113">Esse comando retorna um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="9f40b-113">This command returns a host group.</span></span>

### <span data-ttu-id="9f40b-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9f40b-114">Example 2</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
```

<span data-ttu-id="9f40b-115">Esse comando retorna todos os grupos de hosts no grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="9f40b-115">This command returns all host groups in the given resource group.</span></span>

### <span data-ttu-id="9f40b-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="9f40b-116">Example 3</span></span>
```
PS C:\> Get-AzHostGroup

ResourceGroupName                   Name Location           Tags FDCount
-----------------                   ---- --------           ---- -------
myrg01                     myhostgroup01   eastus {[key1, val1]}       1
myrg01                     myhostgroup02   eastus {[key1, val1]}       2
myrg02                     myhostgroup03   eastus {[key1, val1]}       2
```

<span data-ttu-id="9f40b-117">Esse comando retorna todos os grupos de hosts da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9f40b-117">This command returns all host groups in the subscription.</span></span>

## <span data-ttu-id="9f40b-118">OS</span><span class="sxs-lookup"><span data-stu-id="9f40b-118">PARAMETERS</span></span>

### <span data-ttu-id="9f40b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f40b-119">-DefaultProfile</span></span>
<span data-ttu-id="9f40b-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f40b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f40b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f40b-121">-Name</span></span>
<span data-ttu-id="9f40b-122">O nome do grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="9f40b-122">The name of the host group.</span></span>

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

### <span data-ttu-id="9f40b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f40b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f40b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9f40b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f40b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f40b-125">-ResourceId</span></span>
<span data-ttu-id="9f40b-126">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9f40b-126">The ID of the resource.</span></span>

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

### <span data-ttu-id="9f40b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f40b-127">CommonParameters</span></span>
<span data-ttu-id="9f40b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f40b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f40b-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f40b-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f40b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f40b-130">INPUTS</span></span>

### <span data-ttu-id="9f40b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9f40b-131">System.String</span></span>

## <span data-ttu-id="9f40b-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f40b-132">OUTPUTS</span></span>

### <span data-ttu-id="9f40b-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="9f40b-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="9f40b-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f40b-134">NOTES</span></span>

## <span data-ttu-id="9f40b-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f40b-135">RELATED LINKS</span></span>
