---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: c658780407454f780ccbd00cb824dd1032f3463d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115005"
---
# <span data-ttu-id="1ceb4-101">New-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="1ceb4-101">New-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="1ceb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ceb4-102">SYNOPSIS</span></span>
<span data-ttu-id="1ceb4-103">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-103">Creates a new server.</span></span>

## <span data-ttu-id="1ceb4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ceb4-104">SYNTAX</span></span>

```
New-AzPostgreSqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-Location <String>] [-PublicAccess <String>] [-Sku <String>] [-SkuTier <String>] [-StorageInMb <Int32>]
 [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>] [-Version <ServerVersion>] [-Vnet <String>]
 [-VnetPrefix <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1ceb4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ceb4-105">DESCRIPTION</span></span>
<span data-ttu-id="1ceb4-106">Cria um novo servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-106">Creates a new server.</span></span>

## <span data-ttu-id="1ceb4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ceb4-107">EXAMPLES</span></span>

### <span data-ttu-id="1ceb4-108">Exemplo 1: Criar um novo servidor flexível PostgreSql com argumentos</span><span class="sxs-lookup"><span data-stu-id="1ceb4-108">Example 1: Create a new PostgreSql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest \
-Location eastus -AdministratorUserName postgresqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellPostgreSqlTest ...
Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName       SkuTier        
----          -------- ------------------ ------- ----------------------- -------       -------        
postgresql-test eastus postgresqltest      12     10240                   Standard_B1ms Burstable 

```



### <span data-ttu-id="1ceb4-109">Exemplo 2: Criar um novo servidor flexível PostgreSql com configuração padrão</span><span class="sxs-lookup"><span data-stu-id="1ceb4-109">Example 2: Create a new PostgreSql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server postgresql-test is using sku Standard_D2s_v3 (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="1ceb4-110">Esse cmdlet cria um servidor flexível PostgreSql com valores de parâmetro padrão e provisiona o servidor dentro de uma nova rede virtual e tem uma sub-rede delegada ao servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-110">This cmdlet creates PostgreSql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="1ceb4-111">Os valores padrão de localização são Oeste dos EUA 2, SKU é Standard_D2s_v3, a camada SKU é GeneralPurpose e o tamanho de armazenamento é 128GiB.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-111">The default values of location is West US 2, Sku is Standard_D2s_v3, Sku tier is GeneralPurpose, and storage size is 128GiB.</span></span>


<span data-ttu-id="1ceb4-112">Se você quiser encontrar a senha gerada automaticamente para seu servidor, use o ConvertFrom-SecureString para converter a propriedade 'SecuredPassword' em texto sem texto.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>
<span data-ttu-id="1ceb4-113">(Por exemplo, $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="1ceb4-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="1ceb4-114">Exemplo 3: Criar um novo servidor flexível PostgreSql com rede virtual</span><span class="sxs-lookup"><span data-stu-id="1ceb4-114">Example 3: Create a new PostgreSql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzPostgreSqlFlexibleServer  -ResourceGroupName PowershellPostgreSqlTest -Vnet $Vnet

Resource group PowershellPostgreSqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellPostgreSqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellPostgreSqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="1ceb4-115">Esse cmdlet cria um servidor flexível PostgreSql com id da vnet ou nome de vnet fornecido por um usuário.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-115">This cmdlet creates PostgreSql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="1ceb4-116">Se a rede virtual não existir, o cmdlet criará uma.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="1ceb4-117">Exemplo 4: Criar um novo servidor flexível PostgreSql com nome de rede virtual e sub-rede</span><span class="sxs-lookup"><span data-stu-id="1ceb4-117">Example 4: Create a new PostgreSql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -Vnet postgresql-vnet -Subnet postgresql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellPostgreSqlTest exists ? : True
Creating new vnet postgresql-vnet in resource group PowershellPostgreSqlTest
Creating new subnet postgresql-subnet in resource group PowershellPostgreSqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="1ceb4-118">Esse cmdlet cria um servidor flexível PostgreSql com nome de vnet, nome da sub-rede, prefixo de vnet e prefixo de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-118">This cmdlet creates PostgreSql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="1ceb4-119">Se a rede virtual e a sub-rede não existirem, o cmdlet criará um.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="1ceb4-120">Exemplo 7: Criar um novo servidor flexível PostgreSql com acesso público a todos os IPs</span><span class="sxs-lookup"><span data-stu-id="1ceb4-120">Example 7: Create a new PostgreSql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess All

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 
```

<span data-ttu-id="1ceb4-121">Esse cmdlet cria um servidor flexível PostgreSql aberto para todos os endereços IP.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-121">This cmdlet creates PostgreSql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="1ceb4-122">Exemplo 8: Criar um novo servidor flexível PostgreSql com firewall</span><span class="sxs-lookup"><span data-stu-id="1ceb4-122">Example 8: Create a new PostgreSql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzPostgreSqlFlexibleServer -Name postgresql-test -ResourceGroupName PowershellPostgreSqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellPostgreSqlTest exists ? : True
Creating MySQL server postgresql-test in group PowershellPostgreSqlTest...
Your server postgresql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/postgresql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- -------          -------        
postgresql-test eastus postgresqltest      12     131072                   Standard_D2s_v3 GeneralPurpose 

```

<span data-ttu-id="1ceb4-123">Esse cmdlet cria um servidor flexível PostgreSql aberto para endereços IP especificados.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-123">This cmdlet creates PostgreSql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="1ceb4-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ceb4-124">PARAMETERS</span></span>

### <span data-ttu-id="1ceb4-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1ceb4-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1ceb4-126">A senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-126">The password of the administrator.</span></span>
<span data-ttu-id="1ceb4-127">Mínimo de 8 caracteres e máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="1ceb4-128">A senha deve conter caracteres de três das seguintes categorias: letras maiúsculas em inglês, letras minúsculas em inglês, números e caracteres não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

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

### <span data-ttu-id="1ceb4-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="1ceb4-129">-AdministratorUserName</span></span>
<span data-ttu-id="1ceb4-130">Nome de usuário do administrador para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-130">Administrator username for the server.</span></span>
<span data-ttu-id="1ceb4-131">Depois de definido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-131">Once set, it cannot be changed.</span></span>

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

### <span data-ttu-id="1ceb4-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ceb4-132">-AsJob</span></span>
<span data-ttu-id="1ceb4-133">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-133">Run the command as a job.</span></span>

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

### <span data-ttu-id="1ceb4-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="1ceb4-134">-BackupRetentionDay</span></span>
<span data-ttu-id="1ceb4-135">Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-135">Backup retention days for the server.</span></span>
<span data-ttu-id="1ceb4-136">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-136">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="1ceb4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ceb4-137">-DefaultProfile</span></span>
<span data-ttu-id="1ceb4-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ceb4-139">-Local</span><span class="sxs-lookup"><span data-stu-id="1ceb4-139">-Location</span></span>
<span data-ttu-id="1ceb4-140">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-140">The location the resource resides in.</span></span>

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

### <span data-ttu-id="1ceb4-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ceb4-141">-Name</span></span>
<span data-ttu-id="1ceb4-142">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-142">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ceb4-143">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ceb4-143">-NoWait</span></span>
<span data-ttu-id="1ceb4-144">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-144">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="1ceb4-145">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="1ceb4-145">-PublicAccess</span></span>
<span data-ttu-id="1ceb4-146">Determina o acesso público.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-146">Determines the public access.</span></span>
<span data-ttu-id="1ceb4-147">Insira um ou intervalo de endereços IP a serem incluídos na lista de IPs permitida.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-147">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="1ceb4-148">Os intervalos de endereços IP devem ser separados por traços e não conter espaços.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-148">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="1ceb4-149">Especificar 0.0.0.0 permite o acesso público de todos os recursos implantados no Azure para acessar seu servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-149">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="1ceb4-150">Especificar nenhum endereço IP define o servidor no modo de acesso público, mas não cria uma regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-150">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

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

### <span data-ttu-id="1ceb4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ceb4-151">-ResourceGroupName</span></span>
<span data-ttu-id="1ceb4-152">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-152">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1ceb4-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ceb4-153">-Sku</span></span>
<span data-ttu-id="1ceb4-154">O nome da sKU, normalmente, tier + família + cores, por exemplo, Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-154">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

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

### <span data-ttu-id="1ceb4-155">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1ceb4-155">-SkuTier</span></span>
<span data-ttu-id="1ceb4-156">Nível de cálculo do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-156">Compute tier of the server.</span></span>
<span data-ttu-id="1ceb4-157">Valores aceitos: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-157">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="1ceb4-158">Padrão: indizível.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-158">Default: Burstable.</span></span>

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

### <span data-ttu-id="1ceb4-159">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="1ceb4-159">-StorageInMb</span></span>
<span data-ttu-id="1ceb4-160">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-160">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="1ceb4-161">-Sub-rede</span><span class="sxs-lookup"><span data-stu-id="1ceb4-161">-Subnet</span></span>
<span data-ttu-id="1ceb4-162">O Nome ou ID de uma Sub-rede existente ou o nome de uma nova para criar.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-162">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="1ceb4-163">Observe que a sub-rede será delegada ao Microsoft.DBforPostgreSQL/flexibleServers.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-163">Please note that the subnet will be delegated to Microsoft.DBforPostgreSQL/flexibleServers.</span></span>
<span data-ttu-id="1ceb4-164">Após a delegação, essa sub-rede não pode ser usada para nenhum outro tipo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-164">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

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

### <span data-ttu-id="1ceb4-165">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="1ceb4-165">-SubnetPrefix</span></span>
<span data-ttu-id="1ceb4-166">O prefixo de endereço IP da sub-rede a ser usado ao criar uma nova vnet no formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-166">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="1ceb4-167">O valor padrão é 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-167">Default value is 10.0.0.0/24.</span></span>

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

### <span data-ttu-id="1ceb4-168">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ceb4-168">-SubscriptionId</span></span>
<span data-ttu-id="1ceb4-169">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-169">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ceb4-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="1ceb4-170">-Tag</span></span>
<span data-ttu-id="1ceb4-171">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-171">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ceb4-172">-Versão</span><span class="sxs-lookup"><span data-stu-id="1ceb4-172">-Version</span></span>
<span data-ttu-id="1ceb4-173">Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-173">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ceb4-174">-Vnet</span><span class="sxs-lookup"><span data-stu-id="1ceb4-174">-Vnet</span></span>
<span data-ttu-id="1ceb4-175">O Nome ou ID de uma rede virtual existente ou o nome de uma nova para criar.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-175">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="1ceb4-176">O nome deve estar entre 2 a 64 caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-176">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="1ceb4-177">O nome deve começar com uma letra ou número, terminar com uma letra, um número ou um sublinhado e pode conter apenas letras, números, sublinhados, pontos ou hífens.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-177">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

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

### <span data-ttu-id="1ceb4-178">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="1ceb4-178">-VnetPrefix</span></span>
<span data-ttu-id="1ceb4-179">O prefixo de endereço IP a ser usado ao criar uma nova vnet no formato CIDR.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-179">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="1ceb4-180">O valor padrão é 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-180">Default value is 10.0.0.0/16.</span></span>

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

### <span data-ttu-id="1ceb4-181">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1ceb4-181">-Confirm</span></span>
<span data-ttu-id="1ceb4-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ceb4-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ceb4-183">-WhatIf</span></span>
<span data-ttu-id="1ceb4-184">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ceb4-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ceb4-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ceb4-186">CommonParameters</span></span>
<span data-ttu-id="1ceb4-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ceb4-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ceb4-188">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ceb4-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ceb4-189">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ceb4-189">INPUTS</span></span>

## <span data-ttu-id="1ceb4-190">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ceb4-190">OUTPUTS</span></span>

### <span data-ttu-id="1ceb4-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="1ceb4-191">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="1ceb4-192">Notas</span><span class="sxs-lookup"><span data-stu-id="1ceb4-192">NOTES</span></span>

<span data-ttu-id="1ceb4-193">Aliases</span><span class="sxs-lookup"><span data-stu-id="1ceb4-193">ALIASES</span></span>

## <span data-ttu-id="1ceb4-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ceb4-194">RELATED LINKS</span></span>

