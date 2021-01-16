---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258860"
---
# <span data-ttu-id="31a14-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="31a14-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="31a14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31a14-102">SYNOPSIS</span></span>
<span data-ttu-id="31a14-103">Cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="31a14-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31a14-104">SYNTAX</span></span>

### <span data-ttu-id="31a14-105">NewByEditionAndComputeGenerationParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="31a14-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a14-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31a14-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a14-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="31a14-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a14-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="31a14-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a14-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31a14-109">DESCRIPTION</span></span>
<span data-ttu-id="31a14-110">O cmdlet **New-AzSqlInstance** cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="31a14-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31a14-111">EXAMPLES</span></span>

### <span data-ttu-id="31a14-112">Exemplo 1: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="31a14-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="31a14-113">Esse comando cria uma nova instância usando o parâmetro SkuName.</span><span class="sxs-lookup"><span data-stu-id="31a14-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="31a14-114">Exemplo 2: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="31a14-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="31a14-115">Esse comando cria uma nova instância usando o uso de parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="31a14-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="31a14-116">Exemplo 3: criar uma nova instância em um pool de instâncias usando um objeto de pool de ocorrências</span><span class="sxs-lookup"><span data-stu-id="31a14-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="31a14-117">Esse comando cria uma nova instância em um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="31a14-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="31a14-118">Exemplo 4: criar uma nova instância em um pool de instâncias usando um identificador de recursos de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="31a14-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="31a14-119">Esse comando cria uma nova instância em um pool de instâncias usando o identificador de recursos do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="31a14-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="31a14-120">Exemplo 5: criar uma nova instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="31a14-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="31a14-121">Esse comando cria uma nova instância em um pool de instâncias com o nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="31a14-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="31a14-122">OS</span><span class="sxs-lookup"><span data-stu-id="31a14-122">PARAMETERS</span></span>

### <span data-ttu-id="31a14-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="31a14-123">-AdministratorCredential</span></span>
<span data-ttu-id="31a14-124">A credencial de autenticação SQL da instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="31a14-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31a14-125">-AsJob</span></span>
<span data-ttu-id="31a14-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="31a14-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31a14-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="31a14-127">-AssignIdentity</span></span>
<span data-ttu-id="31a14-128">Gerar e atribuir uma identidade do Azure Active Directory para esta instância gerenciada para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="31a14-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="31a14-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="31a14-130">A redundância do armazenamento de backup usada para armazenar backups para a instância gerenciada do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="31a14-131">Opções são: local, região e geo</span><span class="sxs-lookup"><span data-stu-id="31a14-131">Options are: Local, Zone and Geo</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a14-132">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="31a14-132">-Collation</span></span>
<span data-ttu-id="31a14-133">O agrupamento da instância gerenciada do SQL do Azure a ser usada.</span><span class="sxs-lookup"><span data-stu-id="31a14-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="31a14-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="31a14-134">-ComputeGeneration</span></span>
<span data-ttu-id="31a14-135">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="31a14-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a14-136">-DefaultProfile</span></span>
<span data-ttu-id="31a14-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31a14-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="31a14-138">-DnsZonePartner</span></span>
<span data-ttu-id="31a14-139">A ID do recurso do servidor gerenciado por parceiro para herdar a propriedade DnsZone da criação da instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="31a14-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="31a14-140">-Edição</span><span class="sxs-lookup"><span data-stu-id="31a14-140">-Edition</span></span>
<span data-ttu-id="31a14-141">A edição para a instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="31a14-142">-Force</span><span class="sxs-lookup"><span data-stu-id="31a14-142">-Force</span></span>
<span data-ttu-id="31a14-143">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="31a14-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="31a14-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="31a14-144">-InstancePool</span></span>
<span data-ttu-id="31a14-145">O objeto pai do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="31a14-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="31a14-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="31a14-146">-InstancePoolName</span></span>
<span data-ttu-id="31a14-147">O pool de instâncias no qual colocar esta instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="31a14-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="31a14-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="31a14-149">A ID de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="31a14-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="31a14-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="31a14-150">-LicenseType</span></span>
<span data-ttu-id="31a14-151">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="31a14-151">Determines which License Type to use.</span></span> <span data-ttu-id="31a14-152">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="31a14-152">Possible values are:</span></span>
- <span data-ttu-id="31a14-153">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31a14-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="31a14-154">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31a14-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="31a14-155">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31a14-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="31a14-156">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31a14-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="31a14-157">-Local</span><span class="sxs-lookup"><span data-stu-id="31a14-157">-Location</span></span>
<span data-ttu-id="31a14-158">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="31a14-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="31a14-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="31a14-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="31a14-160">A ID de configuração de manutenção para a instância gerenciada do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="31a14-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="31a14-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="31a14-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="31a14-162">A versão do TLS mínima a ser aplicada para a instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="31a14-162">The minimal TLS version to enforce for Managed instance</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, 1.0, 1.1, 1.2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a14-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="31a14-163">-Name</span></span>
<span data-ttu-id="31a14-164">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-164">Instance name.</span></span>

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

### <span data-ttu-id="31a14-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="31a14-165">-ProxyOverride</span></span>
<span data-ttu-id="31a14-166">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="31a14-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="31a14-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="31a14-168">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="31a14-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="31a14-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a14-169">-ResourceGroupName</span></span>
<span data-ttu-id="31a14-170">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31a14-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="31a14-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="31a14-171">-SkuName</span></span>
<span data-ttu-id="31a14-172">O nome da SKU para a instância, por exemplo, ' GP_Gen4 ', ' BC_Gen4 '.</span><span class="sxs-lookup"><span data-stu-id="31a14-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="31a14-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="31a14-173">-StorageSizeInGB</span></span>
<span data-ttu-id="31a14-174">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="31a14-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="31a14-175">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="31a14-175">-SubnetId</span></span>
<span data-ttu-id="31a14-176">A ID de sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="31a14-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="31a14-177">-Marca</span><span class="sxs-lookup"><span data-stu-id="31a14-177">-Tag</span></span>
<span data-ttu-id="31a14-178">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="31a14-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="31a14-179">-TimeZoneID</span><span class="sxs-lookup"><span data-stu-id="31a14-179">-TimezoneId</span></span>
<span data-ttu-id="31a14-180">A ID de fuso horário da instância a ser definida.</span><span class="sxs-lookup"><span data-stu-id="31a14-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="31a14-181">Uma lista de IDs de fuso horário é exposta por meio do modo de exibição do sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="31a14-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="31a14-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="31a14-182">-VCore</span></span>
<span data-ttu-id="31a14-183">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="31a14-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="31a14-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="31a14-184">-Confirm</span></span>
<span data-ttu-id="31a14-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a14-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a14-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a14-186">-WhatIf</span></span>
<span data-ttu-id="31a14-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="31a14-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a14-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31a14-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a14-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a14-189">CommonParameters</span></span>
<span data-ttu-id="31a14-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a14-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a14-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31a14-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a14-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31a14-192">INPUTS</span></span>

### <span data-ttu-id="31a14-193">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="31a14-193">None</span></span>

## <span data-ttu-id="31a14-194">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31a14-194">OUTPUTS</span></span>

### <span data-ttu-id="31a14-195">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="31a14-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="31a14-196">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31a14-196">NOTES</span></span>

## <span data-ttu-id="31a14-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31a14-197">RELATED LINKS</span></span>
