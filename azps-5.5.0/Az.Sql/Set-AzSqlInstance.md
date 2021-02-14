---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: f16e6f2dcbcf3ebd16926784ca84eef02740df7b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115708"
---
# <span data-ttu-id="b7ee8-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b7ee8-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="b7ee8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ee8-103">Define propriedades para uma Instância Gerenciada do Banco de Dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="b7ee8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7ee8-104">SYNTAX</span></span>

### <span data-ttu-id="b7ee8-105">SetInstanceFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7ee8-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ee8-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b7ee8-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>]
 [-MaintenanceConfigurationId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ee8-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ee8-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-MaintenanceConfigurationId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ee8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ee8-109">O cmdlet **Set-AzSqlInstance** modifica as propriedades de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="b7ee8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7ee8-110">EXAMPLES</span></span>

### <span data-ttu-id="b7ee8-111">Exemplo 1: Definir instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore e -Edition</span><span class="sxs-lookup"><span data-stu-id="b7ee8-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="b7ee8-112">Exemplo 2: alterar a geração de hardware de instância existente usando um novo valor para -ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b7ee8-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="b7ee8-113">Esse comando define a instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore</span><span class="sxs-lookup"><span data-stu-id="b7ee8-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="b7ee8-114">Exemplo 3: Definir instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore para uma instância dentro de um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="b7ee8-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="b7ee8-115">Esse comando define a instância existente usando novos valores para -AdministratorPassword, -LicenseType, -StorageSizeInGB e -VCore para uma instância dentro de um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="b7ee8-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="b7ee8-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7ee8-116">PARAMETERS</span></span>

### <span data-ttu-id="b7ee8-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="b7ee8-117">-AdministratorPassword</span></span>
<span data-ttu-id="b7ee8-118">A nova senha de administrador sql para a instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="b7ee8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7ee8-119">-AsJob</span></span>
<span data-ttu-id="b7ee8-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b7ee8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7ee8-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b7ee8-121">-AssignIdentity</span></span>
<span data-ttu-id="b7ee8-122">Gere e atribua uma Identidade do Azure Active Directory para essa instância para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="b7ee8-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b7ee8-123">-ComputeGeneration</span></span>
<span data-ttu-id="b7ee8-124">A geração de cálculo para a instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="b7ee8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ee8-125">-DefaultProfile</span></span>
<span data-ttu-id="b7ee8-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ee8-127">-Edição</span><span class="sxs-lookup"><span data-stu-id="b7ee8-127">-Edition</span></span>
<span data-ttu-id="b7ee8-128">A edição a ser atribuir à instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="b7ee8-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="b7ee8-129">-Force</span></span>
<span data-ttu-id="b7ee8-130">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="b7ee8-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b7ee8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ee8-131">-InputObject</span></span>
<span data-ttu-id="b7ee8-132">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="b7ee8-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="b7ee8-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="b7ee8-133">-InstancePoolName</span></span>
<span data-ttu-id="b7ee8-134">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-134">The instance pool name.</span></span>

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

### <span data-ttu-id="b7ee8-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b7ee8-135">-LicenseType</span></span>
<span data-ttu-id="b7ee8-136">Determina qual Tipo de Licença usar.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-136">Determines which License Type to use.</span></span> <span data-ttu-id="b7ee8-137">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="b7ee8-137">Possible values are:</span></span>
- <span data-ttu-id="b7ee8-138">Preço BasePrice – O preço com desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças do SQL Server existentes é aplicado.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="b7ee8-139">O preço do serviço instância gerenciada será descontado para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="b7ee8-140">LicenseInclt - O preço de desconto do Azure Hybrid Benefit (AHB) para proprietários de licenças existentes do SQL Server não é aplicado.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="b7ee8-141">O preço do serviço instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="b7ee8-142">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b7ee8-142">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="b7ee8-143">A ID de configuração de manutenção da Instância Gerenciada do Sql Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-143">The Maintenance configuration id for the Sql Azure Managed Instance.</span></span>

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

### <span data-ttu-id="b7ee8-144">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b7ee8-144">-MinimalTlsVersion</span></span>
<span data-ttu-id="b7ee8-145">A versão TLS mínima a ser impor para a instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="b7ee8-145">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="b7ee8-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7ee8-146">-Name</span></span>
<span data-ttu-id="b7ee8-147">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-147">Instance name.</span></span>

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

### <span data-ttu-id="b7ee8-148">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="b7ee8-148">-ProxyOverride</span></span>
<span data-ttu-id="b7ee8-149">O tipo de conexão usado para se conectar à instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-149">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="b7ee8-150">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="b7ee8-150">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="b7ee8-151">Se o ponto de extremidade de dados públicos está habilitado ou não para a instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-151">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="b7ee8-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ee8-152">-ResourceGroupName</span></span>
<span data-ttu-id="b7ee8-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7ee8-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ee8-154">-ResourceId</span></span>
<span data-ttu-id="b7ee8-155">A ID do recurso de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="b7ee8-155">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="b7ee8-156">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="b7ee8-156">-StorageSizeInGB</span></span>
<span data-ttu-id="b7ee8-157">Determina quanto tamanho de armazenamento deve ser associado à instância</span><span class="sxs-lookup"><span data-stu-id="b7ee8-157">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="b7ee8-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7ee8-158">-Tag</span></span>
<span data-ttu-id="b7ee8-159">As marcas a associar à instância.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-159">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="b7ee8-160">-VCore</span><span class="sxs-lookup"><span data-stu-id="b7ee8-160">-VCore</span></span>
<span data-ttu-id="b7ee8-161">Determina quanto vCore associar à instância</span><span class="sxs-lookup"><span data-stu-id="b7ee8-161">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="b7ee8-162">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b7ee8-162">-Confirm</span></span>
<span data-ttu-id="b7ee8-163">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ee8-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ee8-164">-WhatIf</span></span>
<span data-ttu-id="b7ee8-165">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ee8-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ee8-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ee8-167">CommonParameters</span></span>
<span data-ttu-id="b7ee8-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ee8-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ee8-169">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ee8-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ee8-170">Entradas</span><span class="sxs-lookup"><span data-stu-id="b7ee8-170">INPUTS</span></span>

### <span data-ttu-id="b7ee8-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b7ee8-171">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="b7ee8-172">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ee8-172">System.String</span></span>

## <span data-ttu-id="b7ee8-173">Saídas</span><span class="sxs-lookup"><span data-stu-id="b7ee8-173">OUTPUTS</span></span>

### <span data-ttu-id="b7ee8-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b7ee8-174">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="b7ee8-175">Notas</span><span class="sxs-lookup"><span data-stu-id="b7ee8-175">NOTES</span></span>

## <span data-ttu-id="b7ee8-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7ee8-176">RELATED LINKS</span></span>
