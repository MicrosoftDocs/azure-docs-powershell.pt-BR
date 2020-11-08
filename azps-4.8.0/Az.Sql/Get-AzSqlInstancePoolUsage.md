---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113924"
---
# <span data-ttu-id="b06f6-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="b06f6-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="b06f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b06f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b06f6-103">Retorna informações sobre o uso de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b06f6-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="b06f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b06f6-104">SYNTAX</span></span>

### <span data-ttu-id="b06f6-105">InstancePoolUsageDefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b06f6-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06f6-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b06f6-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06f6-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b06f6-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b06f6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b06f6-108">DESCRIPTION</span></span>
<span data-ttu-id="b06f6-109">O cmdlet **Get-AzSqlInstancePoolUsage** retorna informações sobre o uso de um pool de instâncias do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b06f6-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="b06f6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b06f6-110">EXAMPLES</span></span>

### <span data-ttu-id="b06f6-111">Exemplo 1: Obtém o uso de um pool de instâncias do SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b06f6-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="b06f6-112">Obtém o uso do pool de instâncias do SQL do Azure instancepool0.</span><span class="sxs-lookup"><span data-stu-id="b06f6-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="b06f6-113">Exemplo 2: Obtém o uso de um pool de instâncias do SQL do Azure usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="b06f6-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="b06f6-114">Obtém o uso do pool de instâncias do SQL do Azure instancepool0 usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b06f6-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="b06f6-115">Exemplo 3: Obtém o uso de um pool de instâncias do SQL do Azure usando uma ID de recurso do pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="b06f6-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="b06f6-116">Obtém o uso do pool de instâncias do SQL do Azure instancepool0 usando um identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b06f6-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="b06f6-117">Exemplo 3: Obtém o uso de um pool de instâncias do SQL do Azure com um detalhamento dos usos da instância gerenciada dentro do pool.</span><span class="sxs-lookup"><span data-stu-id="b06f6-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="b06f6-118">Obtém o uso do pool de instâncias do SQL do Azure instancepool0 juntamente com os usos das instâncias gerenciadas no instancepool0.</span><span class="sxs-lookup"><span data-stu-id="b06f6-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="b06f6-119">OS</span><span class="sxs-lookup"><span data-stu-id="b06f6-119">PARAMETERS</span></span>

### <span data-ttu-id="b06f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06f6-120">-DefaultProfile</span></span>
<span data-ttu-id="b06f6-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b06f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06f6-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="b06f6-122">-ExpandChildren</span></span>
<span data-ttu-id="b06f6-123">Sinalizador que indica se o uso do pool de instâncias deve ser expandido com o uso de seus filhos.</span><span class="sxs-lookup"><span data-stu-id="b06f6-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="b06f6-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="b06f6-124">-InstancePool</span></span>
<span data-ttu-id="b06f6-125">O objeto de pool de instâncias pai.</span><span class="sxs-lookup"><span data-stu-id="b06f6-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b06f6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b06f6-126">-Name</span></span>
<span data-ttu-id="b06f6-127">O nome do pool de instâncias gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="b06f6-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b06f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="b06f6-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b06f6-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06f6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b06f6-130">-ResourceId</span></span>
<span data-ttu-id="b06f6-131">A ID do recurso pai.</span><span class="sxs-lookup"><span data-stu-id="b06f6-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06f6-132">CommonParameters</span></span>
<span data-ttu-id="b06f6-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06f6-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b06f6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06f6-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b06f6-135">INPUTS</span></span>

### <span data-ttu-id="b06f6-136">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="b06f6-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="b06f6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b06f6-137">System.String</span></span>

## <span data-ttu-id="b06f6-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b06f6-138">OUTPUTS</span></span>

### <span data-ttu-id="b06f6-139">Microsoft. Azure. Commands. Sql. Usages. Models. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="b06f6-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="b06f6-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b06f6-140">NOTES</span></span>

## <span data-ttu-id="b06f6-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b06f6-141">RELATED LINKS</span></span>
