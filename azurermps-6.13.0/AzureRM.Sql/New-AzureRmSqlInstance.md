---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlInstance.md
ms.openlocfilehash: 025a9acc53405aeb1e211473b5f8f13066791714
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440725"
---
# <span data-ttu-id="0dca8-101">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0dca8-101">New-AzureRmSqlInstance</span></span>

## <span data-ttu-id="0dca8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dca8-102">SYNOPSIS</span></span>
<span data-ttu-id="0dca8-103">Cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dca8-103">Creates an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dca8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dca8-104">SYNTAX</span></span>

### <span data-ttu-id="0dca8-105">NewByEditionAndComputeGenerationParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dca8-105">NewByEditionAndComputeGenerationParameterSet (Default)</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -Edition <String> -ComputeGeneration <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dca8-106">NewBySkuNameParameterSetParameter</span><span class="sxs-lookup"><span data-stu-id="0dca8-106">NewBySkuNameParameterSetParameter</span></span>
```
New-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> -AdministratorCredential <PSCredential>
 -Location <String> -SubnetId <String> -LicenseType <String> -StorageSizeInGB <Int32> -VCore <Int32>
 -SkuName <String> [-Tag <Hashtable>] [-AssignIdentity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dca8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dca8-107">DESCRIPTION</span></span>
<span data-ttu-id="0dca8-108">O cmdlet **New-AzureRmSqlInstance** cria uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dca8-108">The **New-AzureRmSqlInstance** cmdlet creates an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="0dca8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dca8-109">EXAMPLES</span></span>

### <span data-ttu-id="0dca8-110">Exemplo 1: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-110">Example 1: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance1 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -SkuName GP_Gen4
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

<span data-ttu-id="0dca8-111">Esse comando cria uma nova instância usando parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="0dca8-111">This command creates a new instance by using Edition and ComputeGeneration parameters.</span></span>

### <span data-ttu-id="0dca8-112">Exemplo 2: criar uma nova instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-112">Example 2: Create a new instance</span></span>
```
PS C:\>New-AzureRmSqlInstance -Name managedInstance2 -ResourceGroupName ResourceGroup01 -Location westcentralus -AdministratorCredential (Get-Credential) -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16 -Edition "GeneralPurpose" -ComputeGeneration Gen4
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

<span data-ttu-id="0dca8-113">Esse comando cria uma nova instância usando o uso de parâmetros de edição e ComputeGeneration.</span><span class="sxs-lookup"><span data-stu-id="0dca8-113">This command creates a new instance by using by using Edition and ComputeGeneration parameters.</span></span>

## <span data-ttu-id="0dca8-114">OS</span><span class="sxs-lookup"><span data-stu-id="0dca8-114">PARAMETERS</span></span>

### <span data-ttu-id="0dca8-115">-AdministratorCredential</span><span class="sxs-lookup"><span data-stu-id="0dca8-115">-AdministratorCredential</span></span>
<span data-ttu-id="0dca8-116">A credencial de autenticação SQL da instância.</span><span class="sxs-lookup"><span data-stu-id="0dca8-116">The SQL authentication credential of the instance.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dca8-117">-AsJob</span></span>
<span data-ttu-id="0dca8-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0dca8-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0dca8-119">-AssignIdentity</span></span>
<span data-ttu-id="0dca8-120">Gerar e atribuir uma identidade do Azure Active Directory para esta instância gerenciada para uso com serviços de gerenciamento de chaves como o cofre do Azure.</span><span class="sxs-lookup"><span data-stu-id="0dca8-120">Generate and assign an Azure Active Directory Identity for this Managed instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-121">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0dca8-121">-ComputeGeneration</span></span>
<span data-ttu-id="0dca8-122">A geração de computação para a instância.</span><span class="sxs-lookup"><span data-stu-id="0dca8-122">The compute generation for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dca8-123">-DefaultProfile</span></span>
<span data-ttu-id="0dca8-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dca8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-125">-Edição</span><span class="sxs-lookup"><span data-stu-id="0dca8-125">-Edition</span></span>
<span data-ttu-id="0dca8-126">A edição para a instância.</span><span class="sxs-lookup"><span data-stu-id="0dca8-126">The edition for the instance.</span></span>

```yaml
Type: String
Parameter Sets: NewByEditionAndComputeGenerationParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-127">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0dca8-127">-LicenseType</span></span>
<span data-ttu-id="0dca8-128">Determina qual tipo de licença de instância usar</span><span class="sxs-lookup"><span data-stu-id="0dca8-128">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-129">-Local</span><span class="sxs-lookup"><span data-stu-id="0dca8-129">-Location</span></span>
<span data-ttu-id="0dca8-130">O local no qual criar a instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-130">The location in which to create the instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dca8-131">-Name</span></span>
<span data-ttu-id="0dca8-132">Nome da instância.</span><span class="sxs-lookup"><span data-stu-id="0dca8-132">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dca8-133">-ResourceGroupName</span></span>
<span data-ttu-id="0dca8-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0dca8-134">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-135">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0dca8-135">-SkuName</span></span>
<span data-ttu-id="0dca8-136">O nome da SKU para a instância, por exemplo, ' GP_Gen4 ', ' BC_Gen4 '.</span><span class="sxs-lookup"><span data-stu-id="0dca8-136">The SKU name for the instance e.g. 'GP_Gen4', 'BC_Gen4'.</span></span>

```yaml
Type: String
Parameter Sets: NewBySkuNameParameterSetParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-137">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0dca8-137">-StorageSizeInGB</span></span>
<span data-ttu-id="0dca8-138">Determina a quantidade de tamanho de armazenamento a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-138">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-139">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="0dca8-139">-SubnetId</span></span>
<span data-ttu-id="0dca8-140">A ID de sub-rede a ser usada para criação de instâncias</span><span class="sxs-lookup"><span data-stu-id="0dca8-140">The Subnet Id to use for instance creation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="0dca8-141">-Tag</span></span>
<span data-ttu-id="0dca8-142">As marcas a serem associadas à instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-142">The tags to associate with the instance</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-143">-VCore</span><span class="sxs-lookup"><span data-stu-id="0dca8-143">-VCore</span></span>
<span data-ttu-id="0dca8-144">Determina a quantidade de VCore a ser associada à instância</span><span class="sxs-lookup"><span data-stu-id="0dca8-144">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0dca8-145">-Confirm</span></span>
<span data-ttu-id="0dca8-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dca8-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dca8-147">-WhatIf</span></span>
<span data-ttu-id="0dca8-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0dca8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dca8-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0dca8-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dca8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dca8-150">CommonParameters</span></span>
<span data-ttu-id="0dca8-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dca8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dca8-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dca8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dca8-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dca8-153">INPUTS</span></span>

### <span data-ttu-id="0dca8-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0dca8-154">None</span></span>

## <span data-ttu-id="0dca8-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dca8-155">OUTPUTS</span></span>

### <span data-ttu-id="0dca8-156">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="0dca8-156">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="0dca8-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dca8-157">NOTES</span></span>

## <span data-ttu-id="0dca8-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dca8-158">RELATED LINKS</span></span>
