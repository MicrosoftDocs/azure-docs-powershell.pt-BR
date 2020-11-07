---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770554"
---
# <span data-ttu-id="349c3-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="349c3-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="349c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="349c3-102">SYNOPSIS</span></span>
<span data-ttu-id="349c3-103">Atualizar um cluster existente do Kusto.</span><span class="sxs-lookup"><span data-stu-id="349c3-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="349c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="349c3-104">SYNTAX</span></span>

### <span data-ttu-id="349c3-105">ByNameAndResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="349c3-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349c3-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="349c3-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349c3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="349c3-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="349c3-108">DESCRIPTION</span></span>
<span data-ttu-id="349c3-109">Atualizar um cluster existente do Kusto.</span><span class="sxs-lookup"><span data-stu-id="349c3-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="349c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="349c3-110">EXAMPLES</span></span>

### <span data-ttu-id="349c3-111">Exemplo 1-atualize um cluster existente por nome</span><span class="sxs-lookup"><span data-stu-id="349c3-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="349c3-112">O comando acima atualiza a camada do cluster Kusto "mykustocluster" encontrada no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="349c3-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="349c3-113">Exemplo 2-atualize um cluster existente por tubulação</span><span class="sxs-lookup"><span data-stu-id="349c3-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="349c3-114">O comando acima Obtém o Kusto cluster "mykustocluster" localizado no grupo de recursos "testrg" usando o `Get-AzKustoCluster` cmdlet e, em seguida, canaliza o resultado para `Update-AzKustoCluster` atualizar o nível do cluster para "padrão".</span><span class="sxs-lookup"><span data-stu-id="349c3-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="349c3-115">OS</span><span class="sxs-lookup"><span data-stu-id="349c3-115">PARAMETERS</span></span>

### <span data-ttu-id="349c3-116">-Capacidade</span><span class="sxs-lookup"><span data-stu-id="349c3-116">-Capacity</span></span>
<span data-ttu-id="349c3-117">O número de instância da VM.</span><span class="sxs-lookup"><span data-stu-id="349c3-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349c3-118">-DefaultProfile</span></span>
<span data-ttu-id="349c3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="349c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349c3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="349c3-120">-InputObject</span></span>
<span data-ttu-id="349c3-121">Objeto de cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="349c3-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="349c3-122">-Name</span></span>
<span data-ttu-id="349c3-123">Nome do cluster a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="349c3-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="349c3-124">-ResourceGroupName</span></span>
<span data-ttu-id="349c3-125">Nome do grupo de recursos sob o qual o cluster existe.</span><span class="sxs-lookup"><span data-stu-id="349c3-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="349c3-126">-ResourceId</span></span>
<span data-ttu-id="349c3-127">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="349c3-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="349c3-128">-SkuName</span></span>
<span data-ttu-id="349c3-129">Nome do SKU usado para criar o cluster</span><span class="sxs-lookup"><span data-stu-id="349c3-129">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-130">-Tier</span><span class="sxs-lookup"><span data-stu-id="349c3-130">-Tier</span></span>
<span data-ttu-id="349c3-131">Nome da camada usada para criar o cluster</span><span class="sxs-lookup"><span data-stu-id="349c3-131">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c3-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="349c3-132">-Confirm</span></span>
<span data-ttu-id="349c3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="349c3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="349c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349c3-134">-WhatIf</span></span>
<span data-ttu-id="349c3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="349c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="349c3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="349c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="349c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349c3-137">CommonParameters</span></span>
<span data-ttu-id="349c3-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="349c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349c3-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349c3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349c3-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="349c3-140">INPUTS</span></span>

### <span data-ttu-id="349c3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="349c3-141">System.String</span></span>

### <span data-ttu-id="349c3-142">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="349c3-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="349c3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="349c3-143">OUTPUTS</span></span>

### <span data-ttu-id="349c3-144">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="349c3-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="349c3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="349c3-145">NOTES</span></span>

## <span data-ttu-id="349c3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="349c3-146">RELATED LINKS</span></span>
