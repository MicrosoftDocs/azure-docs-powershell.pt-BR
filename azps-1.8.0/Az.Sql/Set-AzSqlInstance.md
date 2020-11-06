---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstance.md
ms.openlocfilehash: ad98b764eac08c9fb1f6d3dd367d78ca1b5d45d9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598772"
---
# <span data-ttu-id="d74ee-101">Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="d74ee-101">Set-AzSqlInstance</span></span>

## <span data-ttu-id="d74ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d74ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d74ee-103">Define propriedades para uma instância gerenciada de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d74ee-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="d74ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d74ee-104">SYNTAX</span></span>

### <span data-ttu-id="d74ee-105">SetInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="d74ee-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74ee-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="d74ee-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>]
 [-PublicDataEndpointEnabled <Boolean>] [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74ee-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="d74ee-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-PublicDataEndpointEnabled <Boolean>]
 [-ProxyOverride <String>] [-Tag <Hashtable>] [-AssignIdentity] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d74ee-108">DESCRIPTION</span></span>
<span data-ttu-id="d74ee-109">O cmdlet **set-AzSqlInstance** modifica as propriedades de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d74ee-109">The **Set-AzSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="d74ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d74ee-110">EXAMPLES</span></span>

### <span data-ttu-id="d74ee-111">Exemplo 1: definir a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="d74ee-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
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
```

<span data-ttu-id="d74ee-112">Esse comando define a instância existente usando novos valores para-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="d74ee-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="d74ee-113">OS</span><span class="sxs-lookup"><span data-stu-id="d74ee-113">PARAMETERS</span></span>

### <span data-ttu-id="d74ee-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="d74ee-114">-AdministratorPassword</span></span>
<span data-ttu-id="d74ee-115">A nova senha de administrador do SQL para a instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-115">The new SQL administrator password for the instance.</span></span>

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

### <span data-ttu-id="d74ee-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d74ee-116">-AssignIdentity</span></span>
<span data-ttu-id="d74ee-117">Gerar e atribuir uma identidade do Azure Active Directory para esta instância para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="d74ee-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d74ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74ee-118">-DefaultProfile</span></span>
<span data-ttu-id="d74ee-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d74ee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74ee-120">-Edição</span><span class="sxs-lookup"><span data-stu-id="d74ee-120">-Edition</span></span>
<span data-ttu-id="d74ee-121">A edição a ser atribuída à instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-121">The edition to assign to the instance.</span></span>

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

### <span data-ttu-id="d74ee-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d74ee-122">-Force</span></span>
<span data-ttu-id="d74ee-123">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="d74ee-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="d74ee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74ee-124">-InputObject</span></span>
<span data-ttu-id="d74ee-125">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="d74ee-125">The AzureSqlManagedInstanceModel object to remove</span></span>

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

### <span data-ttu-id="d74ee-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d74ee-126">-LicenseType</span></span>
<span data-ttu-id="d74ee-127">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="d74ee-127">Determines which License Type to use.</span></span> <span data-ttu-id="d74ee-128">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="d74ee-128">Possible values are:</span></span>
- <span data-ttu-id="d74ee-129">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d74ee-129">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="d74ee-130">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d74ee-130">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="d74ee-131">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d74ee-131">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="d74ee-132">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d74ee-132">Managed Instance service price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="d74ee-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d74ee-133">-Name</span></span>
<span data-ttu-id="d74ee-134">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-134">Instance name.</span></span>

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

### <span data-ttu-id="d74ee-135">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="d74ee-135">-ProxyOverride</span></span>
<span data-ttu-id="d74ee-136">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-136">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="d74ee-137">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="d74ee-137">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="d74ee-138">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-138">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="d74ee-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74ee-139">-ResourceGroupName</span></span>
<span data-ttu-id="d74ee-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d74ee-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="d74ee-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74ee-141">-ResourceId</span></span>
<span data-ttu-id="d74ee-142">A ID do recurso de instância a ser removida</span><span class="sxs-lookup"><span data-stu-id="d74ee-142">The resource id of instance to remove</span></span>

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

### <span data-ttu-id="d74ee-143">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="d74ee-143">-StorageSizeInGB</span></span>
<span data-ttu-id="d74ee-144">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="d74ee-144">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="d74ee-145">-Marca</span><span class="sxs-lookup"><span data-stu-id="d74ee-145">-Tag</span></span>
<span data-ttu-id="d74ee-146">As marcas a serem associadas à instância.</span><span class="sxs-lookup"><span data-stu-id="d74ee-146">The tags to associate with the instance.</span></span>

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

### <span data-ttu-id="d74ee-147">-VCore</span><span class="sxs-lookup"><span data-stu-id="d74ee-147">-VCore</span></span>
<span data-ttu-id="d74ee-148">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="d74ee-148">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="d74ee-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d74ee-149">-Confirm</span></span>
<span data-ttu-id="d74ee-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74ee-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74ee-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74ee-151">-WhatIf</span></span>
<span data-ttu-id="d74ee-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d74ee-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74ee-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d74ee-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74ee-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74ee-154">CommonParameters</span></span>
<span data-ttu-id="d74ee-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74ee-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74ee-156">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d74ee-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74ee-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d74ee-157">INPUTS</span></span>

### <span data-ttu-id="d74ee-158">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d74ee-158">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="d74ee-159">System. String</span><span class="sxs-lookup"><span data-stu-id="d74ee-159">System.String</span></span>

## <span data-ttu-id="d74ee-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d74ee-160">OUTPUTS</span></span>

### <span data-ttu-id="d74ee-161">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="d74ee-161">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="d74ee-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d74ee-162">NOTES</span></span>

## <span data-ttu-id="d74ee-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d74ee-163">RELATED LINKS</span></span>
