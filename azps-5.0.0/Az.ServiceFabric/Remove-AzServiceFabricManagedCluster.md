---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115862"
---
# <span data-ttu-id="8d661-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="8d661-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="8d661-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d661-102">SYNOPSIS</span></span>
<span data-ttu-id="8d661-103">Remover recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="8d661-103">Remove cluster resource.</span></span>

## <span data-ttu-id="8d661-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d661-104">SYNTAX</span></span>

### <span data-ttu-id="8d661-105">ByObj (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d661-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d661-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8d661-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d661-107">ById</span><span class="sxs-lookup"><span data-stu-id="8d661-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d661-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d661-108">DESCRIPTION</span></span>
<span data-ttu-id="8d661-109">Remover cluster isso também removerá os tipos de nó no cluster.</span><span class="sxs-lookup"><span data-stu-id="8d661-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="8d661-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d661-110">EXAMPLES</span></span>

### <span data-ttu-id="8d661-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d661-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="8d661-112">Remover cluster.</span><span class="sxs-lookup"><span data-stu-id="8d661-112">Remove cluster.</span></span>

### <span data-ttu-id="8d661-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8d661-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="8d661-114">Remover cluster, com tubulação.</span><span class="sxs-lookup"><span data-stu-id="8d661-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="8d661-115">OS</span><span class="sxs-lookup"><span data-stu-id="8d661-115">PARAMETERS</span></span>

### <span data-ttu-id="8d661-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d661-116">-AsJob</span></span>
<span data-ttu-id="8d661-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8d661-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8d661-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d661-118">-DefaultProfile</span></span>
<span data-ttu-id="8d661-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d661-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d661-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d661-120">-InputObject</span></span>
<span data-ttu-id="8d661-121">Recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="8d661-121">Managed Cluster resource</span></span>

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

### <span data-ttu-id="8d661-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d661-122">-Name</span></span>
<span data-ttu-id="8d661-123">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="8d661-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8d661-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d661-124">-PassThru</span></span>
<span data-ttu-id="8d661-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="8d661-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8d661-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d661-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d661-127">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d661-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8d661-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d661-128">-ResourceId</span></span>
<span data-ttu-id="8d661-129">ID do recurso de cluster gerenciado</span><span class="sxs-lookup"><span data-stu-id="8d661-129">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="8d661-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d661-130">-Confirm</span></span>
<span data-ttu-id="8d661-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d661-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d661-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d661-132">-WhatIf</span></span>
<span data-ttu-id="8d661-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d661-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d661-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d661-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d661-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d661-135">CommonParameters</span></span>
<span data-ttu-id="8d661-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d661-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d661-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d661-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d661-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d661-138">INPUTS</span></span>

### <span data-ttu-id="8d661-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8d661-139">System.String</span></span>

## <span data-ttu-id="8d661-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d661-140">OUTPUTS</span></span>

### <span data-ttu-id="8d661-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8d661-141">System.Boolean</span></span>

## <span data-ttu-id="8d661-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d661-142">NOTES</span></span>

## <span data-ttu-id="8d661-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d661-143">RELATED LINKS</span></span>
