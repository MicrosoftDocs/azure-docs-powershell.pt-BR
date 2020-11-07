---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: d80e6ddd7fa420b07a0df30c2718d9c4e96123fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773838"
---
# <span data-ttu-id="3e667-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="3e667-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="3e667-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e667-102">SYNOPSIS</span></span>
<span data-ttu-id="3e667-103">Cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e667-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3e667-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e667-104">SYNTAX</span></span>

### <span data-ttu-id="3e667-105">NewByEditionAndComputeGenerationParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e667-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e667-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e667-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e667-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e667-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e667-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="3e667-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e667-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e667-109">DESCRIPTION</span></span>
<span data-ttu-id="3e667-110">O cmdlet **New-AzSqlInstance** cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e667-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="3e667-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e667-111">EXAMPLES</span></span>

### <span data-ttu-id="3e667-112">Exemplo 1: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="3e667-112">Example 1: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4 -DnsZonePartner "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/partnerServerForDnsZone"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="3e667-113">Esse comando cria uma nova instância usando o parâmetro SkuName.</span><span class="sxs-lookup"><span data-stu-id="3e667-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="3e667-114">Exemplo 2: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="3e667-114">Example 2: Create a new instance</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         :
```

<span data-ttu-id="3e667-115">Esse comando cria uma nova instância usando o uso de parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="3e667-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="3e667-116">Exemplo 3: criar uma nova instância em um pool de instâncias usando um objeto de pool de ocorrências</span><span class="sxs-lookup"><span data-stu-id="3e667-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="3e667-117">Esse comando cria uma nova instância em um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="3e667-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="3e667-118">Exemplo 4: criar uma nova instância em um pool de instâncias usando um identificador de recursos de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="3e667-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
```powershell
PS C:\> $instancePool | New-AzSqlInstance -Name managedInstance2 -AdministratorCredential (Get-Credential) -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 1024
DnsZone                  : ad35cna0mw
InstancePoolName         : instancepool0
```

<span data-ttu-id="3e667-119">Esse comando cria uma nova instância em um pool de instâncias usando o identificador de recursos do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="3e667-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="3e667-120">Exemplo 5: criar uma nova instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="3e667-120">Example 5: Create a new instance in an instance pool</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 32 -VCore 2 -ComputeGeneration Gen5 -Edition GeneralPurpose -InstancePoolName instancePool0
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 2
StorageSizeInGB          : 32
DnsZone                  : ad35cna0mw
InstancePoolName         : instancePool0
```

<span data-ttu-id="3e667-121">Esse comando cria uma nova instância em um pool de instâncias com o nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="3e667-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="3e667-122">OS</span><span class="sxs-lookup"><span data-stu-id="3e667-122">PARAMETERS</span></span>

### <span data-ttu-id="3e667-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="3e667-123">-AdministratorCredential</span></span>
<span data-ttu-id="3e667-124">A credencial de autenticação SQL da instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-124">The SQL authentication credential of the instance.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e667-125">-AsJob</span></span>
<span data-ttu-id="3e667-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3e667-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e667-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="3e667-127">-AssignIdentity</span></span>
<span data-ttu-id="3e667-128">Gerar e atribuir uma identidade do Azure Active Directory para esta instância gerenciada para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e667-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="3e667-129">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="3e667-129">-Collation</span></span>
<span data-ttu-id="3e667-130">O agrupamento da instância gerenciada do SQL do Azure a ser usada.</span><span class="sxs-lookup"><span data-stu-id="3e667-130">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="3e667-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3e667-131">-ComputeGeneration</span></span>
<span data-ttu-id="3e667-132">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-132">The compute generation for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e667-133">-DefaultProfile</span></span>
<span data-ttu-id="3e667-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3e667-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e667-135">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="3e667-135">-DnsZonePartner</span></span>
<span data-ttu-id="3e667-136">A ID do recurso do servidor gerenciado por parceiro para herdar a propriedade DnsZone da criação da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="3e667-136">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="3e667-137">-Edição</span><span class="sxs-lookup"><span data-stu-id="3e667-137">-Edition</span></span>
<span data-ttu-id="3e667-138">A edição para a instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-138">The edition for the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-139">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="3e667-139">-InstancePool</span></span>
<span data-ttu-id="3e667-140">O objeto pai do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="3e667-140">The instance pool parent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: NewByInstancePoolParentObjectParameterSet
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-141">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="3e667-141">-InstancePoolName</span></span>
<span data-ttu-id="3e667-142">O pool de instâncias no qual colocar esta instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-142">The instance pool to place this instance in.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-143">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="3e667-143">-InstancePoolResourceId</span></span>
<span data-ttu-id="3e667-144">A ID de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="3e667-144">The instance pool resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByInstancePoolResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-145">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3e667-145">-LicenseType</span></span>
<span data-ttu-id="3e667-146">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="3e667-146">Determines which License Type to use.</span></span> <span data-ttu-id="3e667-147">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="3e667-147">Possible values are:</span></span>
- <span data-ttu-id="3e667-148">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e667-148">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="3e667-149">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e667-149">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="3e667-150">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e667-150">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="3e667-151">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e667-151">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-152">-Local</span><span class="sxs-lookup"><span data-stu-id="3e667-152">-Location</span></span>
<span data-ttu-id="3e667-153">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="3e667-153">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-154">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e667-154">-Name</span></span>
<span data-ttu-id="3e667-155">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-155">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-156">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="3e667-156">-ProxyOverride</span></span>
<span data-ttu-id="3e667-157">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-157">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="3e667-158">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="3e667-158">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="3e667-159">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="3e667-159">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="3e667-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e667-160">-ResourceGroupName</span></span>
<span data-ttu-id="3e667-161">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e667-161">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-162">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3e667-162">-SkuName</span></span>
<span data-ttu-id="3e667-163">O nome da SKU para a instância, por exemplo, ' GP_Gen4 ', ' BC_Gen4 '.</span><span class="sxs-lookup"><span data-stu-id="3e667-163">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: System.String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-164">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="3e667-164">-StorageSizeInGB</span></span>
<span data-ttu-id="3e667-165">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="3e667-165">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-166">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="3e667-166">-SubnetId</span></span>
<span data-ttu-id="3e667-167">A ID de sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="3e667-167">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet, NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-168">-Marca</span><span class="sxs-lookup"><span data-stu-id="3e667-168">-Tag</span></span>
<span data-ttu-id="3e667-169">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="3e667-169">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-170">-TimeZoneID</span><span class="sxs-lookup"><span data-stu-id="3e667-170">-TimezoneId</span></span>
<span data-ttu-id="3e667-171">A ID de fuso horário da instância a ser definida.</span><span class="sxs-lookup"><span data-stu-id="3e667-171">The time zone id for the instance to set.</span></span> <span data-ttu-id="3e667-172">Uma lista de IDs de fuso horário é exposta por meio do modo de exibição do sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="3e667-172">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="3e667-173">-VCore</span><span class="sxs-lookup"><span data-stu-id="3e667-173">-VCore</span></span>
<span data-ttu-id="3e667-174">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="3e667-174">Determines how much VCore to associate with instance</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e667-175">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e667-175">-Confirm</span></span>
<span data-ttu-id="3e667-176">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e667-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e667-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e667-177">-WhatIf</span></span>
<span data-ttu-id="3e667-178">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e667-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e667-179">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e667-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e667-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e667-180">CommonParameters</span></span>
<span data-ttu-id="3e667-181">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e667-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e667-182">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e667-182">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e667-183">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e667-183">INPUTS</span></span>

### <span data-ttu-id="3e667-184">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3e667-184">None</span></span>

## <span data-ttu-id="3e667-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e667-185">OUTPUTS</span></span>

### <span data-ttu-id="3e667-186">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3e667-186">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3e667-187">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e667-187">NOTES</span></span>

## <span data-ttu-id="3e667-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e667-188">RELATED LINKS</span></span>
