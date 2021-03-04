---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: a9e3f5f8305733329f7ff9e34eadde151d873c6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892339"
---
# <span data-ttu-id="03ab2-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="03ab2-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="03ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="03ab2-103">Remover recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="03ab2-103">Remove cluster resource.</span></span>

## <span data-ttu-id="03ab2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="03ab2-104">SYNTAX</span></span>

### <span data-ttu-id="03ab2-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="03ab2-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ab2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="03ab2-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03ab2-107">ById</span><span class="sxs-lookup"><span data-stu-id="03ab2-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ab2-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="03ab2-108">DESCRIPTION</span></span>
<span data-ttu-id="03ab2-109">Remover cluster também removerá os tipos de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="03ab2-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="03ab2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03ab2-110">EXAMPLES</span></span>

### <span data-ttu-id="03ab2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="03ab2-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="03ab2-112">Remover cluster.</span><span class="sxs-lookup"><span data-stu-id="03ab2-112">Remove cluster.</span></span>

### <span data-ttu-id="03ab2-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="03ab2-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="03ab2-114">Remover cluster, com canalização.</span><span class="sxs-lookup"><span data-stu-id="03ab2-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="03ab2-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="03ab2-115">PARAMETERS</span></span>

### <span data-ttu-id="03ab2-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03ab2-116">-AsJob</span></span>
<span data-ttu-id="03ab2-117">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="03ab2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="03ab2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ab2-118">-DefaultProfile</span></span>
<span data-ttu-id="03ab2-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03ab2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03ab2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03ab2-120">-InputObject</span></span>
<span data-ttu-id="03ab2-121">Recurso cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="03ab2-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="03ab2-122">-Name</span></span>
<span data-ttu-id="03ab2-123">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="03ab2-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03ab2-124">-PassThru</span></span>
<span data-ttu-id="03ab2-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="03ab2-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="03ab2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ab2-126">-ResourceGroupName</span></span>
<span data-ttu-id="03ab2-127">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="03ab2-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03ab2-128">-ResourceId</span></span>
<span data-ttu-id="03ab2-129">ID de recurso de Cluster Gerenciado</span><span class="sxs-lookup"><span data-stu-id="03ab2-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03ab2-130">-Confirm</span></span>
<span data-ttu-id="03ab2-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ab2-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ab2-132">-WhatIf</span></span>
<span data-ttu-id="03ab2-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="03ab2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03ab2-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="03ab2-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03ab2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ab2-135">CommonParameters</span></span>
<span data-ttu-id="03ab2-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ab2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ab2-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03ab2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ab2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03ab2-138">INPUTS</span></span>

### <span data-ttu-id="03ab2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="03ab2-139">System.String</span></span>

## <span data-ttu-id="03ab2-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="03ab2-140">OUTPUTS</span></span>

### <span data-ttu-id="03ab2-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03ab2-141">System.Boolean</span></span>

## <span data-ttu-id="03ab2-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="03ab2-142">NOTES</span></span>

## <span data-ttu-id="03ab2-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03ab2-143">RELATED LINKS</span></span>
