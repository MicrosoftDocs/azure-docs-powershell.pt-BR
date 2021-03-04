---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: 9f648f0e2ab15919f3caa849041846570d627df5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887661"
---
# <span data-ttu-id="10a53-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10a53-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="10a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a53-102">SYNOPSIS</span></span>
<span data-ttu-id="10a53-103">Cria uma instância gerenciada SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="10a53-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="10a53-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="10a53-104">SYNTAX</span></span>

### <span data-ttu-id="10a53-105">NewByEditionAndComputeGenerationParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="10a53-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a53-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a53-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a53-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10a53-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10a53-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="10a53-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a53-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="10a53-109">DESCRIPTION</span></span>
<span data-ttu-id="10a53-110">O cmdlet **New-AzSqlInstance** cria uma instância gerenciada SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="10a53-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="10a53-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10a53-111">EXAMPLES</span></span>

### <span data-ttu-id="10a53-112">Exemplo 1: Criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="10a53-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="10a53-113">Este comando cria uma nova instância usando o parâmetro SkuName.</span><span class="sxs-lookup"><span data-stu-id="10a53-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="10a53-114">Exemplo 2: Criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="10a53-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="10a53-115">Este comando cria uma nova instância usando os parâmetros Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="10a53-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="10a53-116">Exemplo 3: Criar uma nova instância em um pool de instâncias usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="10a53-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="10a53-117">Esse comando cria uma nova instância em um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="10a53-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="10a53-118">Exemplo 4: Criar uma nova instância em um pool de instâncias usando um identificador de recurso do pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="10a53-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="10a53-119">Este comando cria uma nova instância em um pool de instâncias usando o identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="10a53-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="10a53-120">Exemplo 5: Criar uma nova instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="10a53-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="10a53-121">Este comando cria uma nova instância em um pool de instâncias com name instancePool0</span><span class="sxs-lookup"><span data-stu-id="10a53-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

### <span data-ttu-id="10a53-122">Exemplo 6: Criar uma nova instância com configuração de manutenção</span><span class="sxs-lookup"><span data-stu-id="10a53-122">Example 6: Create a new instance with maintenance configuration</span></span>
```powershell
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName resourcegroup01 -Location "westus" -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -ComputeGeneration Gen5 -Edition GeneralPurpose -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
Location                   : westus
Id                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName          : resourcegroup01
ManagedInstanceName        : managedInstance1
Tags                       :
Identity                   :
Sku                        : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName   : managedInstance1.wusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin         : adminLogin1
AdministratorPassword      :
SubnetId                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType                : LicenseIncluded
VCores                     : 8
StorageSizeInGB            : 256
Collation                  : SQL_Latin1_General_CP1_CI_AS
PublicDataEndpointEnabled  : False
ProxyOverride              :
TimezoneId                 : UTC
DnsZonePartner             :
DnsZone                    : ad35cna0mw
InstancePoolName           :
MinimalTlsVersion          :
BackupStorageRedundancy    : Geo
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2
```

<span data-ttu-id="10a53-123">Este comando cria uma nova instância com configuração de manutenção MI_2</span><span class="sxs-lookup"><span data-stu-id="10a53-123">This command creates a new instance with maintenance configuration MI_2</span></span>

## <span data-ttu-id="10a53-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="10a53-124">PARAMETERS</span></span>

### <span data-ttu-id="10a53-125">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="10a53-125">-AdministratorCredential</span></span>
<span data-ttu-id="10a53-126">A SQL de autenticação da instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-126">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="10a53-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10a53-127">-AsJob</span></span>
<span data-ttu-id="10a53-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="10a53-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10a53-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="10a53-129">-AssignIdentity</span></span>
<span data-ttu-id="10a53-130">Gere e atribua uma Identidade do Active Directory do Azure para esta instância gerenciada para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="10a53-130">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="10a53-131">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="10a53-131">-BackupStorageRedundancy</span></span>
<span data-ttu-id="10a53-132">A redundância de armazenamento de backup usada para armazenar backups para a Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="10a53-132">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="10a53-133">As opções são: Local, Zona e Geo</span><span class="sxs-lookup"><span data-stu-id="10a53-133">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="10a53-134">-Collation</span><span class="sxs-lookup"><span data-stu-id="10a53-134">-Collation</span></span>
<span data-ttu-id="10a53-135">O colamento da instância gerenciada do Azure SQL a ser usada.</span><span class="sxs-lookup"><span data-stu-id="10a53-135">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="10a53-136">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="10a53-136">-ComputeGeneration</span></span>
<span data-ttu-id="10a53-137">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-137">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="10a53-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a53-138">-DefaultProfile</span></span>
<span data-ttu-id="10a53-139">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10a53-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a53-140">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="10a53-140">-DnsZonePartner</span></span>
<span data-ttu-id="10a53-141">A id de recurso do servidor gerenciado parceiro para herdar a propriedade DnsZone da criação de instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="10a53-141">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="10a53-142">-Edition</span><span class="sxs-lookup"><span data-stu-id="10a53-142">-Edition</span></span>
<span data-ttu-id="10a53-143">A edição da instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-143">The edition for the instance.</span></span>

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

### <span data-ttu-id="10a53-144">-Force</span><span class="sxs-lookup"><span data-stu-id="10a53-144">-Force</span></span>
<span data-ttu-id="10a53-145">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="10a53-145">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="10a53-146">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="10a53-146">-InstancePool</span></span>
<span data-ttu-id="10a53-147">O objeto pai do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="10a53-147">The instance pool parent object.</span></span>

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

### <span data-ttu-id="10a53-148">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="10a53-148">-InstancePoolName</span></span>
<span data-ttu-id="10a53-149">O pool de instâncias para colocar essa instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-149">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="10a53-150">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="10a53-150">-InstancePoolResourceId</span></span>
<span data-ttu-id="10a53-151">A ID de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="10a53-151">The instance pool resource id.</span></span>

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

### <span data-ttu-id="10a53-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="10a53-152">-LicenseType</span></span>
<span data-ttu-id="10a53-153">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="10a53-153">Determines which License Type to use.</span></span> <span data-ttu-id="10a53-154">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="10a53-154">Possible values are:</span></span>
- <span data-ttu-id="10a53-155">BasePrice - Os preços com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças SQL Server existentes são aplicados.</span><span class="sxs-lookup"><span data-stu-id="10a53-155">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="10a53-156">O preço do serviço de Instância Gerenciada será descontado para os proprietários SQL Server licenças existentes.</span><span class="sxs-lookup"><span data-stu-id="10a53-156">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="10a53-157">LicenseIncluded - O preço de desconto do Benefício Híbrido do Azure (AHB) para proprietários SQL Server licenças existentes não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="10a53-157">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="10a53-158">O preço do serviço de Instância Gerenciada incluirá um novo SQL Server de licença.</span><span class="sxs-lookup"><span data-stu-id="10a53-158">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="10a53-159">-Location</span><span class="sxs-lookup"><span data-stu-id="10a53-159">-Location</span></span>
<span data-ttu-id="10a53-160">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="10a53-160">The location in which to create the instance</span></span>

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

### <span data-ttu-id="10a53-161">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="10a53-161">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="10a53-162">A ID de configuração de manutenção para a Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="10a53-162">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="10a53-163">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="10a53-163">-MinimalTlsVersion</span></span>
<span data-ttu-id="10a53-164">A versão TLS mínima a ser reforçada para instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="10a53-164">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="10a53-165">-Name</span><span class="sxs-lookup"><span data-stu-id="10a53-165">-Name</span></span>
<span data-ttu-id="10a53-166">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-166">Instance name.</span></span>

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

### <span data-ttu-id="10a53-167">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="10a53-167">-ProxyOverride</span></span>
<span data-ttu-id="10a53-168">O tipo de conexão usado para se conectar à instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-168">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="10a53-169">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="10a53-169">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="10a53-170">Se o ponto de extremidade de dados públicos está habilitado ou não para a instância.</span><span class="sxs-lookup"><span data-stu-id="10a53-170">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="10a53-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a53-171">-ResourceGroupName</span></span>
<span data-ttu-id="10a53-172">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10a53-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="10a53-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="10a53-173">-SkuName</span></span>
<span data-ttu-id="10a53-174">O nome SKU da instância, por exemplo, 'GP_Gen4', 'BC_Gen4'.</span><span class="sxs-lookup"><span data-stu-id="10a53-174">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="10a53-175">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="10a53-175">-StorageSizeInGB</span></span>
<span data-ttu-id="10a53-176">Determina quanto tamanho de armazenamento deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="10a53-176">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="10a53-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="10a53-177">-SubnetId</span></span>
<span data-ttu-id="10a53-178">A ID da Sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="10a53-178">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="10a53-179">-Tag</span><span class="sxs-lookup"><span data-stu-id="10a53-179">-Tag</span></span>
<span data-ttu-id="10a53-180">As marcas a associar à instância</span><span class="sxs-lookup"><span data-stu-id="10a53-180">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="10a53-181">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="10a53-181">-TimezoneId</span></span>
<span data-ttu-id="10a53-182">A ID do fuso horário para a instância a ser definida.</span><span class="sxs-lookup"><span data-stu-id="10a53-182">The time zone id for the instance to set.</span></span> <span data-ttu-id="10a53-183">Uma lista de IDs de fuso horário é exposta por meio do sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="10a53-183">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="10a53-184">-VCore</span><span class="sxs-lookup"><span data-stu-id="10a53-184">-VCore</span></span>
<span data-ttu-id="10a53-185">Determina quanto VCore deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="10a53-185">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="10a53-186">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10a53-186">-Confirm</span></span>
<span data-ttu-id="10a53-187">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10a53-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a53-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a53-188">-WhatIf</span></span>
<span data-ttu-id="10a53-189">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10a53-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a53-190">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10a53-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a53-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a53-191">CommonParameters</span></span>
<span data-ttu-id="10a53-192">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a53-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a53-193">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10a53-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a53-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10a53-194">INPUTS</span></span>

### <span data-ttu-id="10a53-195">Nenhum</span><span class="sxs-lookup"><span data-stu-id="10a53-195">None</span></span>

## <span data-ttu-id="10a53-196">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="10a53-196">OUTPUTS</span></span>

### <span data-ttu-id="10a53-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="10a53-197">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="10a53-198">NOTES</span><span class="sxs-lookup"><span data-stu-id="10a53-198">NOTES</span></span>

## <span data-ttu-id="10a53-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10a53-199">RELATED LINKS</span></span>
