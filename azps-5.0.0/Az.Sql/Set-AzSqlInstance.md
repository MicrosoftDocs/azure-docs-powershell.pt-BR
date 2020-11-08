---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: e17c6b226f7ed4fe17842c93d03828d53c0bb22c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115183"
---
# <span data-ttu-id="9516f-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="9516f-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="9516f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9516f-102">SYNOPSIS</span></span>
<span data-ttu-id="9516f-103">Define propriedades para uma instância gerenciada de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9516f-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="9516f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9516f-104">SYNTAX</span></span>

### <span data-ttu-id="9516f-105">SetInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="9516f-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9516f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="9516f-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9516f-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="9516f-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>]
 [-MinimalTlsVersion <String>] [-Force] [-ComputeGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9516f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9516f-108">DESCRIPTION</span></span>
<span data-ttu-id="9516f-109">O cmdlet **set-AzSqlInstance** modifica as propriedades de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="9516f-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="9516f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9516f-110">EXAMPLES</span></span>

### <span data-ttu-id="9516f-111">Exemplo 1: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB,-VCore e-edição</span><span class="sxs-lookup"><span data-stu-id="9516f-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB, -VCore and -Edition</span></span>
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

### <span data-ttu-id="9516f-112">Exemplo 2: alterar a geração de hardware de instância existente usando novo valor para-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9516f-112">Example 2: Change existing instance hardware generation using new value for -ComputeGeneration</span></span>
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

<span data-ttu-id="9516f-113">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="9516f-113">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="9516f-114">Exemplo 3: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="9516f-114">Example 3: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="9516f-115">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="9516f-115">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="9516f-116">OS</span><span class="sxs-lookup"><span data-stu-id="9516f-116">PARAMETERS</span></span>

### <span data-ttu-id="9516f-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="9516f-117">-AdministratorPassword</span></span>
<span data-ttu-id="9516f-118">A nova senha de administrador do SQL para a instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-118">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="9516f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9516f-119">-AsJob</span></span>
<span data-ttu-id="9516f-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9516f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9516f-121">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9516f-121">-AssignIdentity</span></span>
<span data-ttu-id="9516f-122">Gerar e atribuir uma identidade do Azure Active Directory para esta instância para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="9516f-122">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9516f-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9516f-123">-ComputeGeneration</span></span>
<span data-ttu-id="9516f-124">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="9516f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9516f-125">-DefaultProfile</span></span>
<span data-ttu-id="9516f-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9516f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9516f-127">-Edição</span><span class="sxs-lookup"><span data-stu-id="9516f-127">-Edition</span></span>
<span data-ttu-id="9516f-128">A edição a ser atribuída à instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-128">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="9516f-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9516f-129">-Force</span></span>
<span data-ttu-id="9516f-130">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="9516f-130">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9516f-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9516f-131">-InputObject</span></span>
<span data-ttu-id="9516f-132">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="9516f-132">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="9516f-133">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="9516f-133">-InstancePoolName</span></span>
<span data-ttu-id="9516f-134">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="9516f-134">The instance pool name.</span></span>

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

### <span data-ttu-id="9516f-135">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9516f-135">-LicenseType</span></span>
<span data-ttu-id="9516f-136">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="9516f-136">Determines which License Type to use.</span></span> <span data-ttu-id="9516f-137">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="9516f-137">Possible values are:</span></span>
- <span data-ttu-id="9516f-138">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9516f-138">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="9516f-139">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9516f-139">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="9516f-140">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9516f-140">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="9516f-141">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9516f-141">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="9516f-142">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9516f-142">-MinimalTlsVersion</span></span>
<span data-ttu-id="9516f-143">A versão do TLS mínima a ser aplicada para a instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="9516f-143">The minimal TLS version to enforce for Managed instance</span></span> 

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

### <span data-ttu-id="9516f-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="9516f-144">-Name</span></span>
<span data-ttu-id="9516f-145">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-145">Instance name.</span></span>

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

### <span data-ttu-id="9516f-146">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="9516f-146">-ProxyOverride</span></span>
<span data-ttu-id="9516f-147">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-147">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="9516f-148">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="9516f-148">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="9516f-149">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-149">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="9516f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9516f-150">-ResourceGroupName</span></span>
<span data-ttu-id="9516f-151">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9516f-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="9516f-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9516f-152">-ResourceId</span></span>
<span data-ttu-id="9516f-153">A ID do recurso de instância a ser removida</span><span class="sxs-lookup"><span data-stu-id="9516f-153">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="9516f-154">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9516f-154">-StorageSizeInGB</span></span>
<span data-ttu-id="9516f-155">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="9516f-155">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="9516f-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="9516f-156">-Tag</span></span>
<span data-ttu-id="9516f-157">As marcas a serem associadas à instância.</span><span class="sxs-lookup"><span data-stu-id="9516f-157">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="9516f-158">-VCore</span><span class="sxs-lookup"><span data-stu-id="9516f-158">-VCore</span></span>
<span data-ttu-id="9516f-159">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="9516f-159">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="9516f-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9516f-160">-Confirm</span></span>
<span data-ttu-id="9516f-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9516f-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9516f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9516f-162">-WhatIf</span></span>
<span data-ttu-id="9516f-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9516f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9516f-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9516f-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9516f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9516f-165">CommonParameters</span></span>
<span data-ttu-id="9516f-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9516f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9516f-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9516f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9516f-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9516f-168">INPUTS</span></span>

### <span data-ttu-id="9516f-169">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9516f-169">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="9516f-170">System. String</span><span class="sxs-lookup"><span data-stu-id="9516f-170">System.String</span></span>

## <span data-ttu-id="9516f-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9516f-171">OUTPUTS</span></span>

### <span data-ttu-id="9516f-172">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9516f-172">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="9516f-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9516f-173">NOTES</span></span>

## <span data-ttu-id="9516f-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9516f-174">RELATED LINKS</span></span>
