---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: c5c7cdffc8b329fdff426f48f60869ca6821f32d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401344"
---
# <span data-ttu-id="b9534-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b9534-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="b9534-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9534-102">SYNOPSIS</span></span>
<span data-ttu-id="b9534-103">Liste todos os clusters de Kusto em um grupo de recursos ou receba um cluster Kusto específico.</span><span class="sxs-lookup"><span data-stu-id="b9534-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="b9534-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9534-104">SYNTAX</span></span>

### <span data-ttu-id="b9534-105">ByClusterOrResourceGroupOrSubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9534-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9534-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9534-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9534-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9534-107">DESCRIPTION</span></span>
<span data-ttu-id="b9534-108">Liste todos os clusters de Kusto em um grupo de recursos ou receba um cluster Kusto específico.</span><span class="sxs-lookup"><span data-stu-id="b9534-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="b9534-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9534-109">EXAMPLES</span></span>

### <span data-ttu-id="b9534-110">Exemplo 1 - Listar todos os clusters de Kusto em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b9534-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="b9534-111">Tipo : Microsoft.Kusto/ID de clusters: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/myku Grupo de Recursos 1: nome do testrg: mykustocluster1 Local: Capacidade central dos EUA: 3 SKU : D13_v2 ProvisioningState: Estado bem-sucedido: Marca de execução : {} Uri : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri: `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="b9534-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster1.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster1.centralus.kusto.windows.net`</span></span>

<span data-ttu-id="b9534-112">Tipo : Microsoft.Kusto/ID de clusters: /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/myku Grupo de Recursos do Tocluster2: nome do teste: mykustocluster2 Local: Capacidade central dos EUA: 5 SKU : D13_v2 ProvisioningState: Estado bem-sucedido: Running Tag : {} Uri : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri: `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span><span class="sxs-lookup"><span data-stu-id="b9534-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : `https://mykustocluster2.centralus.kusto.windows.net` DataIngestionUri  : `https://ingest-mykustocluster2.centralus.kusto.windows.net`</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="b9534-113">O comando acima lista todos os clusters de Kusto no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="b9534-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="b9534-114">Exemplo 2 - Obter um cluster Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="b9534-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="b9534-115">O comando acima retorna o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="b9534-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="b9534-116">Exemplo 3 - Obter um cluster Kusto específico por id de recurso</span><span class="sxs-lookup"><span data-stu-id="b9534-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="b9534-117">O comando acima retorna o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="b9534-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="b9534-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9534-118">PARAMETERS</span></span>

### <span data-ttu-id="b9534-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9534-119">-DefaultProfile</span></span>
<span data-ttu-id="b9534-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9534-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9534-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9534-121">-Name</span></span>
<span data-ttu-id="b9534-122">Nome de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="b9534-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9534-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9534-124">Nome do grupo de recursos no qual o usuário deseja recuperar o cluster.</span><span class="sxs-lookup"><span data-stu-id="b9534-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9534-125">-ResourceId</span></span>
<span data-ttu-id="b9534-126">Kusto cluster ResourceID.</span><span class="sxs-lookup"><span data-stu-id="b9534-126">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9534-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9534-127">CommonParameters</span></span>
<span data-ttu-id="b9534-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9534-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9534-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9534-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9534-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9534-130">INPUTS</span></span>

### <span data-ttu-id="b9534-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b9534-131">System.String</span></span>

## <span data-ttu-id="b9534-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9534-132">OUTPUTS</span></span>

### <span data-ttu-id="b9534-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="b9534-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="b9534-134">Notas</span><span class="sxs-lookup"><span data-stu-id="b9534-134">NOTES</span></span>

## <span data-ttu-id="b9534-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9534-135">RELATED LINKS</span></span>
