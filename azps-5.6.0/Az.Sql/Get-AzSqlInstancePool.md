---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 524d9ff479355f511b9039e1ea64a8234e37e021
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891567"
---
# <span data-ttu-id="f5433-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="f5433-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="f5433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5433-102">SYNOPSIS</span></span>
<span data-ttu-id="f5433-103">Retorna informações sobre o pool de instâncias SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f5433-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f5433-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5433-104">SYNTAX</span></span>

### <span data-ttu-id="f5433-105">ListBySubOrResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5433-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5433-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5433-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5433-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5433-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5433-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5433-108">DESCRIPTION</span></span>
<span data-ttu-id="f5433-109">O cmdlet **Get-AzSqlInstancePool** retorna informações sobre um ou mais pool de instâncias do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f5433-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="f5433-110">Especifique o nome de um pool de instâncias para ver informações apenas para esse pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f5433-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="f5433-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5433-111">EXAMPLES</span></span>

### <span data-ttu-id="f5433-112">Exemplo 1: Obter todos os pools de instâncias em uma assinatura do cliente</span><span class="sxs-lookup"><span data-stu-id="f5433-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="f5433-113">Este comando obtém informações sobre todos os pools de instâncias dentro da assinatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="f5433-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="f5433-114">Exemplo 2: Obter todos os pools de instâncias em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f5433-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="f5433-115">Este comando obtém informações sobre todos os pools de instâncias no grupo de recursos resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="f5433-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="f5433-116">Exemplo 3: obter informações sobre um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="f5433-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="f5433-117">Este comando obtém informações sobre a instância do pool de instânciasPool0.</span><span class="sxs-lookup"><span data-stu-id="f5433-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="f5433-118">Exemplo 4: obter informações sobre um pool de instâncias usando a id de recurso do pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="f5433-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="f5433-119">Este comando obtém informações sobre o pool de instâncias com seu identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="f5433-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="f5433-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5433-120">PARAMETERS</span></span>

### <span data-ttu-id="f5433-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5433-121">-DefaultProfile</span></span>
<span data-ttu-id="f5433-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5433-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5433-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f5433-123">-Name</span></span>
<span data-ttu-id="f5433-124">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f5433-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5433-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5433-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5433-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f5433-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5433-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5433-127">-ResourceId</span></span>
<span data-ttu-id="f5433-128">O identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="f5433-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5433-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5433-129">CommonParameters</span></span>
<span data-ttu-id="f5433-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5433-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5433-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5433-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5433-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5433-132">INPUTS</span></span>

### <span data-ttu-id="f5433-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f5433-133">None</span></span>

## <span data-ttu-id="f5433-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5433-134">OUTPUTS</span></span>

### <span data-ttu-id="f5433-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="f5433-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="f5433-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5433-136">NOTES</span></span>

## <span data-ttu-id="f5433-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5433-137">RELATED LINKS</span></span>
