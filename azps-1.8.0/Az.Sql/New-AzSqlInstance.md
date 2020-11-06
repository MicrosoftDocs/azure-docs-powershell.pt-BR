---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstance.md
ms.openlocfilehash: bfa1785004e13400395bd6a6fc93bdec29a69809
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598891"
---
# <span data-ttu-id="a1d9b-101">New-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a1d9b-101">New-AzSqlInstance</span></span>

## <span data-ttu-id="a1d9b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d9b-103">Cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-103">Creates an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="a1d9b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1d9b-104">SYNTAX</span></span>

### <span data-ttu-id="a1d9b-105">NewByEditionAndComputeGenerationParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1d9b-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Collation <String>] [-PublicDataEndpointEnabled]
 [-ProxyOverride <String>] [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d9b-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="a1d9b-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Collation <String>] [-PublicDataEndpointEnabled] [-ProxyOverride <String>]
 [-TimezoneId <String>] [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d9b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1d9b-107">DESCRIPTION</span></span>
<span data-ttu-id="a1d9b-108">O cmdlet **New-AzSqlInstance** cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-108">The **New-AzSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="a1d9b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1d9b-109">EXAMPLES</span></span>

### <span data-ttu-id="a1d9b-110">Exemplo 1: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="a1d9b-111">Esse comando cria uma nova instância usando parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="a1d9b-112">Exemplo 2: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-112">Example 2: Create a new instance</span></span>
```
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
```

<span data-ttu-id="a1d9b-113">Esse comando cria uma nova instância usando o uso de parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="a1d9b-114">OS</span><span class="sxs-lookup"><span data-stu-id="a1d9b-114">PARAMETERS</span></span>

### <span data-ttu-id="a1d9b-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="a1d9b-115">-AdministratorCredential</span></span>
<span data-ttu-id="a1d9b-116">A credencial de autenticação SQL da instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-116">The SQL authentication credential of the instance.</span></span>

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

### <span data-ttu-id="a1d9b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d9b-117">-AsJob</span></span>
<span data-ttu-id="a1d9b-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a1d9b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1d9b-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a1d9b-119">-AssignIdentity</span></span>
<span data-ttu-id="a1d9b-120">Gerar e atribuir uma identidade do Azure Active Directory para esta instância gerenciada para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a1d9b-121">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="a1d9b-121">-Collation</span></span>
<span data-ttu-id="a1d9b-122">O agrupamento da instância gerenciada do SQL do Azure a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-122">The collation of the Azure SQL Managed Instance to use.</span></span>

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

### <span data-ttu-id="a1d9b-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a1d9b-123">-ComputeGeneration</span></span>
<span data-ttu-id="a1d9b-124">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-124">The compute generation for the instance.</span></span>

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

### <span data-ttu-id="a1d9b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d9b-125">-DefaultProfile</span></span>
<span data-ttu-id="a1d9b-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d9b-127">-Edição</span><span class="sxs-lookup"><span data-stu-id="a1d9b-127">-Edition</span></span>
<span data-ttu-id="a1d9b-128">A edição para a instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-128">The edition for the instance.</span></span>

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

### <span data-ttu-id="a1d9b-129">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a1d9b-129">-LicenseType</span></span>
<span data-ttu-id="a1d9b-130">Determina qual tipo de licença usar.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-130">Determines which License Type to use.</span></span> <span data-ttu-id="a1d9b-131">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a1d9b-131">Possible values are:</span></span>
- <span data-ttu-id="a1d9b-132">BasePrice-o benefício híbrido do Azure (AHB) foi aplicado o preço com desconto para os proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-132">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="a1d9b-133">O preço do serviço de instância gerenciado será descontado para os proprietários de licença existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-133">Managed Instance service price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="a1d9b-134">LicenseIncluded-o AHB (benefício híbrido do Azure) não é aplicado com o preço de desconto dos proprietários de licenças existentes do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-134">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="a1d9b-135">O preço do serviço de instância gerenciada incluirá um novo custo de licença do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-135">Managed Instance service price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d9b-136">-Local</span><span class="sxs-lookup"><span data-stu-id="a1d9b-136">-Location</span></span>
<span data-ttu-id="a1d9b-137">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-137">The location in which to create the instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d9b-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1d9b-138">-Name</span></span>
<span data-ttu-id="a1d9b-139">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-139">Instance name.</span></span>

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

### <span data-ttu-id="a1d9b-140">-ProxyOverride</span><span class="sxs-lookup"><span data-stu-id="a1d9b-140">-ProxyOverride</span></span>
<span data-ttu-id="a1d9b-141">O tipo de conexão usado para conexão com a instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-141">The connection type used for connecting to the instance.</span></span>

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

### <span data-ttu-id="a1d9b-142">-PublicDataEndpointEnabled</span><span class="sxs-lookup"><span data-stu-id="a1d9b-142">-PublicDataEndpointEnabled</span></span>
<span data-ttu-id="a1d9b-143">Se o ponto de extremidade de dados públicos está ou não habilitado para a instância.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-143">Whether or not the public data endpoint is enabled for the instance.</span></span>

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

### <span data-ttu-id="a1d9b-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d9b-144">-ResourceGroupName</span></span>
<span data-ttu-id="a1d9b-145">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d9b-146">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a1d9b-146">-SkuName</span></span>
<span data-ttu-id="a1d9b-147">O nome da SKU para a instância, por exemplo, ' GP_Gen4 ', ' BC_Gen4 '.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-147">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

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

### <span data-ttu-id="a1d9b-148">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="a1d9b-148">-StorageSizeInGB</span></span>
<span data-ttu-id="a1d9b-149">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-149">Determines how much Storage size to associate with instance</span></span>

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

### <span data-ttu-id="a1d9b-150">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="a1d9b-150">-SubnetId</span></span>
<span data-ttu-id="a1d9b-151">A ID de sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="a1d9b-151">The Subnet Id to use for instance creation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d9b-152">-Marca</span><span class="sxs-lookup"><span data-stu-id="a1d9b-152">-Tag</span></span>
<span data-ttu-id="a1d9b-153">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-153">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="a1d9b-154">-TimeZoneID</span><span class="sxs-lookup"><span data-stu-id="a1d9b-154">-TimezoneId</span></span>
<span data-ttu-id="a1d9b-155">A ID de fuso horário da instância a ser definida.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-155">The time zone id for the instance to set.</span></span> <span data-ttu-id="a1d9b-156">Uma lista de IDs de fuso horário é exposta por meio do modo de exibição do sys.time_zone_info (Transact-SQL).</span><span class="sxs-lookup"><span data-stu-id="a1d9b-156">A list of time zone ids is exposed through the sys.time_zone_info (Transact-SQL) view.</span></span>

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

### <span data-ttu-id="a1d9b-157">-VCore</span><span class="sxs-lookup"><span data-stu-id="a1d9b-157">-VCore</span></span>
<span data-ttu-id="a1d9b-158">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="a1d9b-158">Determines how much VCore to associate with instance</span></span>

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

### <span data-ttu-id="a1d9b-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1d9b-159">-Confirm</span></span>
<span data-ttu-id="a1d9b-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d9b-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d9b-161">-WhatIf</span></span>
<span data-ttu-id="a1d9b-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d9b-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d9b-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d9b-164">CommonParameters</span></span>
<span data-ttu-id="a1d9b-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d9b-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d9b-166">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1d9b-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d9b-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1d9b-167">INPUTS</span></span>

### <span data-ttu-id="a1d9b-168">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a1d9b-168">None</span></span>

## <span data-ttu-id="a1d9b-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1d9b-169">OUTPUTS</span></span>

### <span data-ttu-id="a1d9b-170">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="a1d9b-170">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a1d9b-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1d9b-171">NOTES</span></span>

## <span data-ttu-id="a1d9b-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1d9b-172">RELATED LINKS</span></span>
