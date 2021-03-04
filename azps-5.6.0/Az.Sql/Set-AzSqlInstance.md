---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: a6dd059b7fdab3c2670e3b8902def148d88124d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901559"
---
# <span data-ttu-id="2c48a-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c48a-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="2c48a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c48a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c48a-103">Define propriedades para uma instância gerenciada do banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2c48a-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="2c48a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c48a-104">SYNTAX</span></span>

### <span data-ttu-id="2c48a-105">SetInstanceFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2c48a-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c48a-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="2c48a-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c48a-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="2c48a-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c48a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c48a-108">DESCRIPTION</span></span>
<span data-ttu-id="2c48a-109">O cmdlet **Set-AzSqlInstance** modifica propriedades de uma instância gerenciada SQL banco de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c48a-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="2c48a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c48a-110">EXAMPLES</span></span>

### <span data-ttu-id="2c48a-111">Exemplo 1: Definir instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore e -Edition</span><span class="sxs-lookup"><span data-stu-id="2c48a-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition BusinessCritical
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
InstancePoolName         :
```

### <span data-ttu-id="2c48a-112">Exemplo 2: Alterar a geração de hardware de instância existente usando um novo valor para -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2c48a-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -ComputeGeneration Gen5
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
InstancePoolName         :
```

<span data-ttu-id="2c48a-113">Este comando define a instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore</span><span class="sxs-lookup"><span data-stu-id="2c48a-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="2c48a-114">Exemplo 3: Definir instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="2c48a-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 2 -InstancePoolName instancePool0
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
StorageSizeInGB          : 1024
InstancePoolName         : instancePool0
```

<span data-ttu-id="2c48a-115">Este comando define a instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="2c48a-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

### <span data-ttu-id="2c48a-116">Exemplo 4: atualizar a configuração de manutenção para a instância existente</span><span class="sxs-lookup"><span data-stu-id="2c48a-116">Example 4: Update maintenance configuration for existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_WestUS_MI_2"
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

<span data-ttu-id="2c48a-117">Este comando atualiza a instância existente com a configuração de manutenção MI_2</span><span class="sxs-lookup"><span data-stu-id="2c48a-117">This command updates existing instance with maintenance configuration MI_2</span></span>

### <span data-ttu-id="2c48a-118">Exemplo 5: Remover a configuração de manutenção da instância existente</span><span class="sxs-lookup"><span data-stu-id="2c48a-118">Example 5: Remove maintenance configuration from existing instance</span></span>
```powershell
PS C:\> Set-AzSqlInstance -Name "managediInstance1" -ResourceGroupName "Resourcegroup01" -MaintenanceConfigurationId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default"
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
MaintenanceConfigurationId : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/SQL_Default
```

<span data-ttu-id="2c48a-119">Este comando redefine a configuração de manutenção como padrão para a instância existente</span><span class="sxs-lookup"><span data-stu-id="2c48a-119">This command resets maintenance configuration to default for existing instance</span></span>

## <span data-ttu-id="2c48a-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c48a-120">PARAMETERS</span></span>

### <span data-ttu-id="2c48a-121">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="2c48a-121">-AdministratorPassword</span></span>
<span data-ttu-id="2c48a-122">A nova SQL de administrador para a instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-122">The new SQL administrator password for the instance.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c48a-123">-AsJob</span></span>
<span data-ttu-id="2c48a-124">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2c48a-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c48a-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2c48a-125">-AssignIdentity</span></span>
<span data-ttu-id="2c48a-126">Gere e atribua uma Identidade do Azure Active Directory para essa instância para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2c48a-126">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2c48a-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2c48a-127">-ComputeGeneration</span></span>
<span data-ttu-id="2c48a-128">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-128">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="2c48a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c48a-129">-DefaultProfile</span></span>
<span data-ttu-id="2c48a-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c48a-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c48a-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="2c48a-131">-Edition</span></span>
<span data-ttu-id="2c48a-132">A edição a ser atribuído à instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-132">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="2c48a-133">-Force</span><span class="sxs-lookup"><span data-stu-id="2c48a-133">-Force</span></span>
<span data-ttu-id="2c48a-134">Ignorar mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="2c48a-134">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="2c48a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c48a-135">-InputObject</span></span>
<span data-ttu-id="2c48a-136">O objeto AzureSqlManagedInstanceModel a ser removido</span><span class="sxs-lookup"><span data-stu-id="2c48a-136">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-137">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="2c48a-137">-InstancePoolName</span></span>
<span data-ttu-id="2c48a-138">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="2c48a-138">The instance pool name.</span></span>

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

### <span data-ttu-id="2c48a-139">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2c48a-139">-LicenseType</span></span>
<span data-ttu-id="2c48a-140">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="2c48a-140">Determines which License Type to use.</span></span> <span data-ttu-id="2c48a-141">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="2c48a-141">Possible values are:</span></span>
- <span data-ttu-id="2c48a-142">BasePrice - Os preços com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças SQL Server existentes são aplicados.</span><span class="sxs-lookup"><span data-stu-id="2c48a-142">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="2c48a-143">O preço do serviço de Instância Gerenciada será descontado para os proprietários SQL Server licenças existentes.</span><span class="sxs-lookup"><span data-stu-id="2c48a-143">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="2c48a-144">LicenseIncluded - O preço de desconto do Benefício Híbrido do Azure (AHB) para proprietários SQL Server licenças existentes não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="2c48a-144">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="2c48a-145">O preço do serviço de Instância Gerenciada incluirá um novo SQL Server de licença.</span><span class="sxs-lookup"><span data-stu-id="2c48a-145">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="2c48a-146">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2c48a-146">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="2c48a-147">A ID de configuração de manutenção para a Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="2c48a-147">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="2c48a-148">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2c48a-148">-MinimalTlsVersion</span></span>
<span data-ttu-id="2c48a-149">A versão TLS mínima a ser reforçada para instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="2c48a-149">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="2c48a-150">-Name</span><span class="sxs-lookup"><span data-stu-id="2c48a-150">-Name</span></span>
<span data-ttu-id="2c48a-151">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-151">Instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-152">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="2c48a-152">-ProxyOverride</span></span>
<span data-ttu-id="2c48a-153">O tipo de conexão usado para se conectar à instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-153">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="2c48a-154">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="2c48a-154">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="2c48a-155">Se o ponto de extremidade de dados públicos está habilitado ou não para a instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-155">Whether or not the public data endpoint is enabled for the instance.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c48a-156">-ResourceGroupName</span></span>
<span data-ttu-id="2c48a-157">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2c48a-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c48a-158">-ResourceId</span></span>
<span data-ttu-id="2c48a-159">A ID do recurso de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="2c48a-159">The resource id of instance to remove</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c48a-160">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="2c48a-160">-StorageSizeInGB</span></span>
<span data-ttu-id="2c48a-161">Determina quanto tamanho de armazenamento deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="2c48a-161">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="2c48a-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c48a-162">-Tag</span></span>
<span data-ttu-id="2c48a-163">As marcas a associar à instância.</span><span class="sxs-lookup"><span data-stu-id="2c48a-163">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="2c48a-164">-VCore</span><span class="sxs-lookup"><span data-stu-id="2c48a-164">-VCore</span></span>
<span data-ttu-id="2c48a-165">Determina quanto VCore deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="2c48a-165">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="2c48a-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c48a-166">-Confirm</span></span>
<span data-ttu-id="2c48a-167">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c48a-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c48a-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c48a-168">-WhatIf</span></span>
<span data-ttu-id="2c48a-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c48a-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c48a-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c48a-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c48a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c48a-171">CommonParameters</span></span>
<span data-ttu-id="2c48a-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c48a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c48a-173">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c48a-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c48a-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c48a-174">INPUTS</span></span>

### <span data-ttu-id="2c48a-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2c48a-175">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="2c48a-176">System.String</span><span class="sxs-lookup"><span data-stu-id="2c48a-176">System.String</span></span>

## <span data-ttu-id="2c48a-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c48a-177">OUTPUTS</span></span>

### <span data-ttu-id="2c48a-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="2c48a-178">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="2c48a-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c48a-179">NOTES</span></span>

## <span data-ttu-id="2c48a-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c48a-180">RELATED LINKS</span></span>
