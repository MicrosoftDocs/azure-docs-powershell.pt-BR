---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: 1af66eec2e67048ed85d90c0cdae2867b932b2b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115000"
---
# <span data-ttu-id="84a15-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="84a15-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="84a15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="84a15-102">SYNOPSIS</span></span>
<span data-ttu-id="84a15-103">Cria uma nova réplica de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="84a15-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="84a15-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84a15-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84a15-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="84a15-105">DESCRIPTION</span></span>
<span data-ttu-id="84a15-106">Cria uma nova réplica de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="84a15-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="84a15-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84a15-107">EXAMPLES</span></span>

### <span data-ttu-id="84a15-108">Exemplo 1: Criar uma nova réplica de servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="84a15-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="84a15-109">Este cmdlet cria uma nova réplica de servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="84a15-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="84a15-110">Exemplo 2: Criar uma nova replica de servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="84a15-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="84a15-111">Este cmdlet cria uma nova réplica de servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="84a15-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="84a15-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84a15-112">PARAMETERS</span></span>

### <span data-ttu-id="84a15-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84a15-113">-AsJob</span></span>
<span data-ttu-id="84a15-114">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="84a15-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="84a15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a15-115">-DefaultProfile</span></span>
<span data-ttu-id="84a15-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="84a15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a15-117">-Local</span><span class="sxs-lookup"><span data-stu-id="84a15-117">-Location</span></span>
<span data-ttu-id="84a15-118">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="84a15-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="84a15-119">-Mestre</span><span class="sxs-lookup"><span data-stu-id="84a15-119">-Master</span></span>
<span data-ttu-id="84a15-120">O objeto do servidor de origem para criar uma réplica.</span><span class="sxs-lookup"><span data-stu-id="84a15-120">The source server object to create replica from.</span></span>
<span data-ttu-id="84a15-121">Para construir, confira a seção ANOTAÇÕES para propriedades MASTER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="84a15-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84a15-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="84a15-122">-NoWait</span></span>
<span data-ttu-id="84a15-123">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="84a15-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="84a15-124">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="84a15-124">-ReplicaName</span></span>
<span data-ttu-id="84a15-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicaServerName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a15-126">-ResourceGroupName</span></span>
<span data-ttu-id="84a15-127">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="84a15-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="84a15-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="84a15-128">-Sku</span></span>
<span data-ttu-id="84a15-129">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="84a15-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="84a15-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84a15-130">-SubscriptionId</span></span>
<span data-ttu-id="84a15-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="84a15-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="84a15-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="84a15-132">-Confirm</span></span>
<span data-ttu-id="84a15-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a15-134">-WhatIf</span></span>
<span data-ttu-id="84a15-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="84a15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a15-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="84a15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a15-137">CommonParameters</span></span>
<span data-ttu-id="84a15-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a15-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84a15-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a15-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="84a15-140">INPUTS</span></span>

### <span data-ttu-id="84a15-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="84a15-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="84a15-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="84a15-142">OUTPUTS</span></span>

### <span data-ttu-id="84a15-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="84a15-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="84a15-144">Notas</span><span class="sxs-lookup"><span data-stu-id="84a15-144">NOTES</span></span>

<span data-ttu-id="84a15-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="84a15-145">ALIASES</span></span>

<span data-ttu-id="84a15-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="84a15-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="84a15-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="84a15-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="84a15-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="84a15-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="84a15-149">MASTER: <IServer> O objeto do servidor de origem para criar uma réplica.</span><span class="sxs-lookup"><span data-stu-id="84a15-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="84a15-150">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="84a15-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="84a15-151">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="84a15-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="84a15-152">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="84a15-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="84a15-153">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="84a15-154">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="84a15-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="84a15-155">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="84a15-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="84a15-156">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="84a15-157">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="84a15-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="84a15-158">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="84a15-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="84a15-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="84a15-160">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="84a15-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="84a15-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão TLs mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="84a15-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="84a15-163">O valor é opcional, mas, se aprovado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="84a15-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="84a15-164">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="84a15-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="84a15-165">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="84a15-166">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="84a15-167">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="84a15-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="84a15-168">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="84a15-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="84a15-169">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="84a15-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="84a15-170">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="84a15-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="84a15-171">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="84a15-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="84a15-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="84a15-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="84a15-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="84a15-175">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="84a15-176">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="84a15-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="84a15-177">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="84a15-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="84a15-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="84a15-178">RELATED LINKS</span></span>

