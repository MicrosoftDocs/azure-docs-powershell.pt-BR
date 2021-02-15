---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: ef809acdf8b78eb0d1203a901b3b44028c79733e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116144"
---
# <span data-ttu-id="d7949-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d7949-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="d7949-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7949-102">SYNOPSIS</span></span>
<span data-ttu-id="d7949-103">Cria uma Instância Gerenciada do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7949-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d7949-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7949-104">SYNTAX</span></span>

### <span data-ttu-id="d7949-105">NewByEditionAndComputeGenerationParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7949-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-InstancePoolName <String>] [-MinimalTlsVersion <String>]
 [-BackupStorageRedundancy <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7949-106">NewByInstancePoolParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7949-106">NewByInstancePoolParentObjectParameterSet</span></span>
```
New-AzSqlInstance [-InstancePool] <AzureSqlInstancePoolModel> [-Name] <String>
 -AdministratorCredential <PSCredential> [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>]
 [-PublicDataEndpointEnabled] [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>]
 [-AssignIdentity] [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7949-107">NewByInstancePoolResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7949-107">NewByInstancePoolResourceIdParameterSet</span></span>
```
New-AzSqlInstance [-InstancePoolResourceId] <String> [-Name] <String> -AdministratorCredential <PSCredential>
 [-StorageSizeInGB <Int32>] -VCore <Int32> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-DnsZonePartner <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7949-108">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="d7949-108">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> [-LicenseType <String>] [-StorageSizeInGB <Int32>] -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-DnsZonePartner <String>]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-BackupStorageRedundancy <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7949-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7949-109">DESCRIPTION</span></span>
<span data-ttu-id="d7949-110">O **cmdlet New-AzSqlInstance** cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7949-110">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="d7949-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7949-111">EXAMPLES</span></span>

### <span data-ttu-id="d7949-112">Exemplo 1: Criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="d7949-112">Example 1: Create a new instance</span></span>
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

<span data-ttu-id="d7949-113">Esse comando cria uma nova instância usando o parâmetro SkuName.</span><span class="sxs-lookup"><span data-stu-id="d7949-113">This command creates a new instance by using the SkuName parameter.</span></span>

### <span data-ttu-id="d7949-114">Exemplo 2: Criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="d7949-114">Example 2: Create a new instance</span></span>
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

<span data-ttu-id="d7949-115">Esse comando cria uma nova instância usando os parâmetros Edition e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="d7949-115">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="d7949-116">Exemplo 3: Criar uma nova instância em um pool de instâncias usando um objeto de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="d7949-116">Example 3: Create a new instance in an instance pool using an instance pool object</span></span>
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

<span data-ttu-id="d7949-117">Esse comando cria uma nova instância em um pool de instâncias usando um objeto de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="d7949-117">This command creates a new instance in an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="d7949-118">Exemplo 4: Criar uma nova instância em um pool de instâncias usando um identificador de recurso de pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="d7949-118">Example 4: Create a new instance in an instance pool using an instance pool resource identifier</span></span>
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

<span data-ttu-id="d7949-119">Esse comando cria uma nova instância em um pool de instâncias usando o identificador de recurso do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="d7949-119">This command creates a new instance in an instance pool using the instance pool's resource identifier.</span></span>

### <span data-ttu-id="d7949-120">Exemplo 5: Criar uma nova instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="d7949-120">Example 5: Create a new instance in an instance pool</span></span>
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

<span data-ttu-id="d7949-121">Esse comando cria uma nova instância em um pool de instâncias com nome instancePool0</span><span class="sxs-lookup"><span data-stu-id="d7949-121">This command creates a new instance in an instance pool with name instancePool0</span></span>

## <span data-ttu-id="d7949-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7949-122">PARAMETERS</span></span>

### <span data-ttu-id="d7949-123">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="d7949-123">-AdministratorCredential</span></span>
<span data-ttu-id="d7949-124">A credencial de autenticação SQL da instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-124">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="d7949-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7949-125">-AsJob</span></span>
<span data-ttu-id="d7949-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7949-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7949-127">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d7949-127">-AssignIdentity</span></span>
<span data-ttu-id="d7949-128">Gere e atribua uma Identidade do Azure Active Directory para esta instância gerenciada para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7949-128">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d7949-129">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d7949-129">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d7949-130">A redundância de armazenamento de backup usada para armazenar backups da Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="d7949-130">The Backup storage redundancy used to store backups for the Sql Azure Managed Instance.</span></span> <span data-ttu-id="d7949-131">As opções são: Local, Zona e Geo</span><span class="sxs-lookup"><span data-stu-id="d7949-131">Options are: Local, Zone and Geo</span></span>

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

### <span data-ttu-id="d7949-132">-Colagem</span><span class="sxs-lookup"><span data-stu-id="d7949-132">-Collation</span></span>
<span data-ttu-id="d7949-133">A colagem da Instância Gerenciada do SQL do Azure a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d7949-133">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="d7949-134">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d7949-134">-ComputeGeneration</span></span>
<span data-ttu-id="d7949-135">A geração de cálculo para a instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-135">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="d7949-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7949-136">-DefaultProfile</span></span>
<span data-ttu-id="d7949-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7949-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7949-138">-DnsZonePartner</span><span class="sxs-lookup"><span data-stu-id="d7949-138">-DnsZonePartner</span></span>
<span data-ttu-id="d7949-139">A ID do recurso do servidor gerenciado parceiro para herdar a propriedade DnsZone da criação de instâncias gerenciadas</span><span class="sxs-lookup"><span data-stu-id="d7949-139">The resource id of the partner Managed Server to inherit DnsZone property from for Managed instance creation</span></span>

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

### <span data-ttu-id="d7949-140">-Edição</span><span class="sxs-lookup"><span data-stu-id="d7949-140">-Edition</span></span>
<span data-ttu-id="d7949-141">A edição da instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-141">The edition for the instance.</span></span>

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

### <span data-ttu-id="d7949-142">-Forçar</span><span class="sxs-lookup"><span data-stu-id="d7949-142">-Force</span></span>
<span data-ttu-id="d7949-143">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="d7949-143">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d7949-144">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="d7949-144">-InstancePool</span></span>
<span data-ttu-id="d7949-145">O objeto pai do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="d7949-145">The instance pool parent object.</span></span>

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

### <span data-ttu-id="d7949-146">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="d7949-146">-InstancePoolName</span></span>
<span data-ttu-id="d7949-147">O pool de instâncias para colocar essa instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-147">The instance pool to place this instance in.</span></span>

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

### <span data-ttu-id="d7949-148">-InstancePoolResourceId</span><span class="sxs-lookup"><span data-stu-id="d7949-148">-InstancePoolResourceId</span></span>
<span data-ttu-id="d7949-149">A ID do recurso de pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="d7949-149">The instance pool resource id.</span></span>

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

### <span data-ttu-id="d7949-150">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d7949-150">-LicenseType</span></span>
<span data-ttu-id="d7949-151">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="d7949-151">Determines which License Type to use.</span></span> <span data-ttu-id="d7949-152">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="d7949-152">Possible values are:</span></span>
- <span data-ttu-id="d7949-153">Preço BasePrice – O preço com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças do SQL Server existentes é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d7949-153">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="d7949-154">O preço do serviço instância gerenciada será descontado para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7949-154">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="d7949-155">LicenseInclt - O preço de desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças existentes do SQL Server não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="d7949-155">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="d7949-156">O preço do serviço instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d7949-156">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="d7949-157">-Local</span><span class="sxs-lookup"><span data-stu-id="d7949-157">-Location</span></span>
<span data-ttu-id="d7949-158">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="d7949-158">The location in which to create the instance</span></span>

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

### <span data-ttu-id="d7949-159">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d7949-159">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="d7949-160">A ID de configuração de manutenção da Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="d7949-160">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="d7949-161">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d7949-161">-MinimalTlsVersion</span></span>
<span data-ttu-id="d7949-162">A versão TLS mínima a ser impor para a instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="d7949-162">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="d7949-163">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7949-163">-Name</span></span>
<span data-ttu-id="d7949-164">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-164">Instance name.</span></span>

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

### <span data-ttu-id="d7949-165">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="d7949-165">-ProxyOverride</span></span>
<span data-ttu-id="d7949-166">O tipo de conexão usado para se conectar à instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-166">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="d7949-167">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="d7949-167">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="d7949-168">Se o ponto de extremidade de dados públicos está habilitado ou não para a instância.</span><span class="sxs-lookup"><span data-stu-id="d7949-168">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="d7949-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7949-169">-ResourceGroupName</span></span>
<span data-ttu-id="d7949-170">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7949-170">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7949-171">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7949-171">-SkuName</span></span>
<span data-ttu-id="d7949-172">O nome da SKU para a instância, por exemplo, "GP_Gen4", "BC_Gen4".</span><span class="sxs-lookup"><span data-stu-id="d7949-172">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="d7949-173">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d7949-173">-StorageSizeInGB</span></span>
<span data-ttu-id="d7949-174">Determina quanto tamanho de armazenamento deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="d7949-174">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="d7949-175">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="d7949-175">-SubnetId</span></span>
<span data-ttu-id="d7949-176">A ID da Sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="d7949-176">The Subnet Id to use for instance creation</span></span>

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

### <span data-ttu-id="d7949-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7949-177">-Tag</span></span>
<span data-ttu-id="d7949-178">As marcas a associar à instância</span><span class="sxs-lookup"><span data-stu-id="d7949-178">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="d7949-179">-TimezoneId</span><span class="sxs-lookup"><span data-stu-id="d7949-179">-TimezoneId</span></span>
<span data-ttu-id="d7949-180">A ID de fuso horário da instância a ser definida.</span><span class="sxs-lookup"><span data-stu-id="d7949-180">The time zone id for the instance to set.</span></span> <span data-ttu-id="d7949-181">Uma lista de IDs de fuso horário é exposta por meio do sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="d7949-181">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="d7949-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="d7949-182">-VCore</span></span>
<span data-ttu-id="d7949-183">Determina quanto vCore associar à instância</span><span class="sxs-lookup"><span data-stu-id="d7949-183">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="d7949-184">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d7949-184">-Confirm</span></span>
<span data-ttu-id="d7949-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7949-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7949-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7949-186">-WhatIf</span></span>
<span data-ttu-id="d7949-187">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d7949-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7949-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7949-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7949-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7949-189">CommonParameters</span></span>
<span data-ttu-id="d7949-190">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7949-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7949-191">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7949-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7949-192">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7949-192">INPUTS</span></span>

### <span data-ttu-id="d7949-193">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d7949-193">None</span></span>

## <span data-ttu-id="d7949-194">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7949-194">OUTPUTS</span></span>

### <span data-ttu-id="d7949-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d7949-195">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d7949-196">Notas</span><span class="sxs-lookup"><span data-stu-id="d7949-196">NOTES</span></span>

## <span data-ttu-id="d7949-197">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7949-197">RELATED LINKS</span></span>
