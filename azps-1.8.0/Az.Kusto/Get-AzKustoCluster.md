---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770572"
---
# <span data-ttu-id="0190a-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0190a-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="0190a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0190a-102">SYNOPSIS</span></span>
<span data-ttu-id="0190a-103">Liste todos os clusters do Kusto em um grupo de recursos ou obtenha um cluster de Kusto específico.</span><span class="sxs-lookup"><span data-stu-id="0190a-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="0190a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0190a-104">SYNTAX</span></span>

### <span data-ttu-id="0190a-105">ByClusterOrResourceGroupOrSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="0190a-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0190a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0190a-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0190a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0190a-107">DESCRIPTION</span></span>
<span data-ttu-id="0190a-108">Liste todos os clusters do Kusto em um grupo de recursos ou obtenha um cluster de Kusto específico.</span><span class="sxs-lookup"><span data-stu-id="0190a-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="0190a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0190a-109">EXAMPLES</span></span>

### <span data-ttu-id="0190a-110">Exemplo 1-listar todos os clusters do Kusto em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0190a-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="0190a-111">Tipo: Microsoft. Kusto/clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 grupo Resource: testrg nome: mykustocluster1 local: capacidade central dos EUA: 3 SKU: D13_v2 ProvisioningState: êxito no estado: executando marca: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="0190a-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="0190a-112">Tipo: Microsoft. Kusto/clusters ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 grupo Resource: testrg nome: mykustocluster2 local: capacidade central dos EUA: 5 SKU: D13_v2 ProvisioningState: êxito no estado: executando marca: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="0190a-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="0190a-113">O comando acima lista todos os clusters do Kusto no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="0190a-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="0190a-114">Exemplo 2-obter um cluster Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="0190a-114">Example 2 - Get a specific Kusto cluster by name</span></span>

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

<span data-ttu-id="0190a-115">O comando acima retorna o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="0190a-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="0190a-116">Exemplo 3-obter um cluster Kusto específico por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="0190a-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

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

<span data-ttu-id="0190a-117">O comando acima retorna o cluster Kusto chamado "mykustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="0190a-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="0190a-118">OS</span><span class="sxs-lookup"><span data-stu-id="0190a-118">PARAMETERS</span></span>

### <span data-ttu-id="0190a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0190a-119">-DefaultProfile</span></span>
<span data-ttu-id="0190a-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0190a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0190a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0190a-121">-Name</span></span>
<span data-ttu-id="0190a-122">Nome de um cluster específico.</span><span class="sxs-lookup"><span data-stu-id="0190a-122">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="0190a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0190a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0190a-124">Nome do grupo de recursos sob o qual o usuário quer recuperar o cluster.</span><span class="sxs-lookup"><span data-stu-id="0190a-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="0190a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0190a-125">-ResourceId</span></span>
<span data-ttu-id="0190a-126">ResourceId do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="0190a-126">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="0190a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0190a-127">CommonParameters</span></span>
<span data-ttu-id="0190a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0190a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0190a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0190a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0190a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0190a-130">INPUTS</span></span>

### <span data-ttu-id="0190a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0190a-131">System.String</span></span>

## <span data-ttu-id="0190a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0190a-132">OUTPUTS</span></span>

### <span data-ttu-id="0190a-133">Microsoft. Azure. Commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0190a-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="0190a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0190a-134">NOTES</span></span>

## <span data-ttu-id="0190a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0190a-135">RELATED LINKS</span></span>
