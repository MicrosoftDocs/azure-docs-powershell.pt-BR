---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114506"
---
# <span data-ttu-id="3c023-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="3c023-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="3c023-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c023-102">SYNOPSIS</span></span>
<span data-ttu-id="3c023-103">Remover recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="3c023-103">Remove cluster resource.</span></span>

## <span data-ttu-id="3c023-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c023-104">SYNTAX</span></span>

### <span data-ttu-id="3c023-105">ByObj (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c023-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c023-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3c023-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c023-107">ById</span><span class="sxs-lookup"><span data-stu-id="3c023-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c023-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3c023-108">DESCRIPTION</span></span>
<span data-ttu-id="3c023-109">Remover cluster também removerá os tipos de nó sob o cluster.</span><span class="sxs-lookup"><span data-stu-id="3c023-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="3c023-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c023-110">EXAMPLES</span></span>

### <span data-ttu-id="3c023-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c023-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="3c023-112">Remover cluster.</span><span class="sxs-lookup"><span data-stu-id="3c023-112">Remove cluster.</span></span>

### <span data-ttu-id="3c023-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c023-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="3c023-114">Remover cluster, com canos.</span><span class="sxs-lookup"><span data-stu-id="3c023-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="3c023-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c023-115">PARAMETERS</span></span>

### <span data-ttu-id="3c023-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c023-116">-AsJob</span></span>
<span data-ttu-id="3c023-117">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o andamento.</span><span class="sxs-lookup"><span data-stu-id="3c023-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3c023-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c023-118">-DefaultProfile</span></span>
<span data-ttu-id="3c023-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c023-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c023-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c023-120">-InputObject</span></span>
<span data-ttu-id="3c023-121">Recurso Cluster Gerenciado</span><span class="sxs-lookup"><span data-stu-id="3c023-121">Managed Cluster resource</span></span>

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

### <span data-ttu-id="3c023-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c023-122">-Name</span></span>
<span data-ttu-id="3c023-123">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3c023-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="3c023-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c023-124">-PassThru</span></span>
<span data-ttu-id="3c023-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="3c023-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3c023-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c023-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c023-127">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c023-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3c023-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c023-128">-ResourceId</span></span>
<span data-ttu-id="3c023-129">ID do recurso Cluster Gerenciado</span><span class="sxs-lookup"><span data-stu-id="3c023-129">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="3c023-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3c023-130">-Confirm</span></span>
<span data-ttu-id="3c023-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c023-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c023-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c023-132">-WhatIf</span></span>
<span data-ttu-id="3c023-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3c023-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c023-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c023-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c023-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c023-135">CommonParameters</span></span>
<span data-ttu-id="3c023-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c023-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c023-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c023-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c023-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="3c023-138">INPUTS</span></span>

### <span data-ttu-id="3c023-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3c023-139">System.String</span></span>

## <span data-ttu-id="3c023-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="3c023-140">OUTPUTS</span></span>

### <span data-ttu-id="3c023-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c023-141">System.Boolean</span></span>

## <span data-ttu-id="3c023-142">Notas</span><span class="sxs-lookup"><span data-stu-id="3c023-142">NOTES</span></span>

## <span data-ttu-id="3c023-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c023-143">RELATED LINKS</span></span>
