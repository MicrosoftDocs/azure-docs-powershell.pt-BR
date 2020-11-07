---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: c08d2b1a08e76603af7125d0d4671643133699da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773761"
---
# <span data-ttu-id="ca40c-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ca40c-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="ca40c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca40c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca40c-103">Define propriedades para uma instância gerenciada de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca40c-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="ca40c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca40c-104">SYNTAX</span></span>

### <span data-ttu-id="ca40c-105">SetInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca40c-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca40c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="ca40c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity]
 [-InstancePoolName <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca40c-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="ca40c-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-InstancePoolName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca40c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca40c-108">DESCRIPTION</span></span>
<span data-ttu-id="ca40c-109">O cmdlet **set-AzSqlInstance** modifica as propriedades de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca40c-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="ca40c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca40c-110">EXAMPLES</span></span>

### <span data-ttu-id="ca40c-111">Exemplo 1: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="ca40c-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```powershell
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
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

<span data-ttu-id="ca40c-112">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="ca40c-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

### <span data-ttu-id="ca40c-113">Exemplo 2: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="ca40c-113">Example 2: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>
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

<span data-ttu-id="ca40c-114">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore para uma instância em um pool de instâncias</span><span class="sxs-lookup"><span data-stu-id="ca40c-114">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore for an instance within an instance pool</span></span>

## <span data-ttu-id="ca40c-115">OS</span><span class="sxs-lookup"><span data-stu-id="ca40c-115">PARAMETERS</span></span>

### <span data-ttu-id="ca40c-116">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="ca40c-116">-AdministratorPassword</span></span>
<span data-ttu-id="ca40c-117">A nova senha de administrador do SQL para a instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-117">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="ca40c-118">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="ca40c-118">-AssignIdentity</span></span>
<span data-ttu-id="ca40c-119">Gerar e atribuir uma identidade do Azure Active Directory para esta instância para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca40c-119">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ca40c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca40c-120">-DefaultProfile</span></span>
<span data-ttu-id="ca40c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca40c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca40c-122">-Edição</span><span class="sxs-lookup"><span data-stu-id="ca40c-122">-Edition</span></span>
<span data-ttu-id="ca40c-123">A edição a ser atribuída à instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-123">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="ca40c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ca40c-124">-Force</span></span>
<span data-ttu-id="ca40c-125">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="ca40c-125">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="ca40c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca40c-126">-InputObject</span></span>
<span data-ttu-id="ca40c-127">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="ca40c-127">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="ca40c-128">-InstancePoolName</span><span class="sxs-lookup"><span data-stu-id="ca40c-128">-InstancePoolName</span></span>
<span data-ttu-id="ca40c-129">O nome do pool de instâncias.</span><span class="sxs-lookup"><span data-stu-id="ca40c-129">The instance pool name.</span></span>

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

### <span data-ttu-id="ca40c-130">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ca40c-130">-LicenseType</span></span>
<span data-ttu-id="ca40c-131">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="ca40c-131">Determines which License Type to use.</span></span> <span data-ttu-id="ca40c-132">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="ca40c-132">Possible values are:</span></span>
- <span data-ttu-id="ca40c-133">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca40c-133">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ca40c-134">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca40c-134">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ca40c-135">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca40c-135">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ca40c-136">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ca40c-136">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="ca40c-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca40c-137">-Name</span></span>
<span data-ttu-id="ca40c-138">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-138">Instance name.</span></span>

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

### <span data-ttu-id="ca40c-139">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="ca40c-139">-ProxyOverride</span></span>
<span data-ttu-id="ca40c-140">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-140">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="ca40c-141">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="ca40c-141">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="ca40c-142">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-142">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="ca40c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca40c-143">-ResourceGroupName</span></span>
<span data-ttu-id="ca40c-144">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca40c-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca40c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca40c-145">-ResourceId</span></span>
<span data-ttu-id="ca40c-146">A ID do recurso de instância a ser removida</span><span class="sxs-lookup"><span data-stu-id="ca40c-146">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="ca40c-147">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ca40c-147">-StorageSizeInGB</span></span>
<span data-ttu-id="ca40c-148">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="ca40c-148">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="ca40c-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="ca40c-149">-Tag</span></span>
<span data-ttu-id="ca40c-150">As marcas a serem associadas à instância.</span><span class="sxs-lookup"><span data-stu-id="ca40c-150">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="ca40c-151">-VCore</span><span class="sxs-lookup"><span data-stu-id="ca40c-151">-VCore</span></span>
<span data-ttu-id="ca40c-152">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="ca40c-152">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="ca40c-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca40c-153">-Confirm</span></span>
<span data-ttu-id="ca40c-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca40c-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca40c-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca40c-155">-WhatIf</span></span>
<span data-ttu-id="ca40c-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca40c-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca40c-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca40c-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca40c-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca40c-158">CommonParameters</span></span>
<span data-ttu-id="ca40c-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca40c-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca40c-160">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca40c-160">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca40c-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca40c-161">INPUTS</span></span>

### <span data-ttu-id="ca40c-162">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ca40c-162">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="ca40c-163">System. String</span><span class="sxs-lookup"><span data-stu-id="ca40c-163">System.String</span></span>

## <span data-ttu-id="ca40c-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca40c-164">OUTPUTS</span></span>

### <span data-ttu-id="ca40c-165">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="ca40c-165">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="ca40c-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca40c-166">NOTES</span></span>

## <span data-ttu-id="ca40c-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca40c-167">RELATED LINKS</span></span>
