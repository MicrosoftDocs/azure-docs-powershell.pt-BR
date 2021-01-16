---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258057"
---
# <span data-ttu-id="8d8bf-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8d8bf-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="8d8bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8bf-103">Define propriedades para uma instância gerenciada de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="8d8bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d8bf-104">SYNTAX</span></span>

### <span data-ttu-id="8d8bf-105">SetInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="8d8bf-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d8bf-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8d8bf-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d8bf-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8bf-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d8bf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d8bf-108">DESCRIPTION</span></span>
<span data-ttu-id="8d8bf-109">O cmdlet **set-AzSqlInstance** modifica as propriedades de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="8d8bf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d8bf-110">EXAMPLES</span></span>

### <span data-ttu-id="8d8bf-111">Exemplo 1: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore e-edição</span><span class="sxs-lookup"><span data-stu-id="8d8bf-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="8d8bf-112">Exemplo 2: alterar a geração de hardware de instância existente usando novo valor para-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8d8bf-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="8d8bf-113">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="8d8bf-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="8d8bf-114">Exemplo 3: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="8d8bf-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="8d8bf-115">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="8d8bf-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="8d8bf-116">OS</span><span class="sxs-lookup"><span data-stu-id="8d8bf-116">PARAMETERS</span></span>

### <span data-ttu-id="8d8bf-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="8d8bf-117">-AdministratorPassword</span></span>
<span data-ttu-id="8d8bf-118">A nova senha de administrador do SQL para a instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="8d8bf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d8bf-119">-AsJob</span></span>
<span data-ttu-id="8d8bf-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8d8bf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d8bf-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8d8bf-121">-AssignIdentity</span></span>
<span data-ttu-id="8d8bf-122">Gerar e atribuir uma identidade do Azure Active Directory para esta instância para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8d8bf-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="8d8bf-123">-ComputeGeneration</span></span>
<span data-ttu-id="8d8bf-124">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="8d8bf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8bf-125">-DefaultProfile</span></span>
<span data-ttu-id="8d8bf-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d8bf-127">-Edição</span><span class="sxs-lookup"><span data-stu-id="8d8bf-127">-Edition</span></span>
<span data-ttu-id="8d8bf-128">A edição a ser atribuída à instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="8d8bf-129">-Force</span><span class="sxs-lookup"><span data-stu-id="8d8bf-129">-Force</span></span>
<span data-ttu-id="8d8bf-130">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="8d8bf-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8d8bf-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d8bf-131">-InputObject</span></span>
<span data-ttu-id="8d8bf-132">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="8d8bf-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="8d8bf-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="8d8bf-133">-InstancePoolName</span></span>
<span data-ttu-id="8d8bf-134">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-134">The instance pool name.</span></span>

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

### <span data-ttu-id="8d8bf-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d8bf-135">-LicenseType</span></span>
<span data-ttu-id="8d8bf-136">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-136">Determines which License Type to use.</span></span> <span data-ttu-id="8d8bf-137">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="8d8bf-137">Possible values are:</span></span>
- <span data-ttu-id="8d8bf-138">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="8d8bf-139">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="8d8bf-140">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="8d8bf-141">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="8d8bf-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8d8bf-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="8d8bf-143">A ID de configuração de manutenção para a instância gerenciada do SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="8d8bf-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="8d8bf-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="8d8bf-145">A versão do TLS mínima a ser aplicada para a instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="8d8bf-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="8d8bf-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d8bf-146">-Name</span></span>
<span data-ttu-id="8d8bf-147">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-147">Instance name.</span></span>

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

### <span data-ttu-id="8d8bf-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="8d8bf-148">-ProxyOverride</span></span>
<span data-ttu-id="8d8bf-149">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="8d8bf-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="8d8bf-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="8d8bf-151">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="8d8bf-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8bf-152">-ResourceGroupName</span></span>
<span data-ttu-id="8d8bf-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="8d8bf-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d8bf-154">-ResourceId</span></span>
<span data-ttu-id="8d8bf-155">A ID do recurso de instância a ser removida</span><span class="sxs-lookup"><span data-stu-id="8d8bf-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="8d8bf-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8d8bf-156">-StorageSizeInGB</span></span>
<span data-ttu-id="8d8bf-157">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="8d8bf-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="8d8bf-158">-Marca</span><span class="sxs-lookup"><span data-stu-id="8d8bf-158">-Tag</span></span>
<span data-ttu-id="8d8bf-159">As marcas a serem associadas à instância.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="8d8bf-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="8d8bf-160">-VCore</span></span>
<span data-ttu-id="8d8bf-161">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="8d8bf-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="8d8bf-162">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d8bf-162">-Confirm</span></span>
<span data-ttu-id="8d8bf-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d8bf-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d8bf-164">-WhatIf</span></span>
<span data-ttu-id="8d8bf-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d8bf-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d8bf-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8bf-167">CommonParameters</span></span>
<span data-ttu-id="8d8bf-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d8bf-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8bf-169">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d8bf-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8bf-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d8bf-170">INPUTS</span></span>

### <span data-ttu-id="8d8bf-171">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8d8bf-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="8d8bf-172">System. String</span><span class="sxs-lookup"><span data-stu-id="8d8bf-172">System.String</span></span>

## <span data-ttu-id="8d8bf-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d8bf-173">OUTPUTS</span></span>

### <span data-ttu-id="8d8bf-174">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8d8bf-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="8d8bf-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d8bf-175">NOTES</span></span>

## <span data-ttu-id="8d8bf-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d8bf-176">RELATED LINKS</span></span>
