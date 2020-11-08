---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/new-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/New-AzPostgreSqlReplica.md
ms.openlocfilehash: e3c0d7e8d3b3d9fe42bc97c40ad54424b7bfd0da
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110353"
---
# <span data-ttu-id="5e7d0-101">New-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="5e7d0-101">New-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="5e7d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e7d0-103">Cria uma nova réplica a partir de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="5e7d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e7d0-104">SYNTAX</span></span>

```
New-AzPostgreSqlReplica -ReplicaName <String> -ResourceGroupName <String> -Master <IServer>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e7d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e7d0-105">DESCRIPTION</span></span>
<span data-ttu-id="5e7d0-106">Cria uma nova réplica a partir de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="5e7d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e7d0-107">EXAMPLES</span></span>

### <span data-ttu-id="5e7d0-108">Exemplo 1: criar uma nova réplica do servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="5e7d0-108">Example 1: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | New-AzPostgreSqlReplica -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5e7d0-109">Esse cmdlet cria uma nova réplica do servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-109">This cmdlet creates a new PostgreSql server replica.</span></span>

### <span data-ttu-id="5e7d0-110">Exemplo 2: criar uma nova réplica do servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="5e7d0-110">Example 2: Create a new PostgreSql server replica</span></span>
```powershell
PS C:\> $pgDb = Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 
PS C:\> New-AzPostgreSqlReplica -Master $pgDb -ReplicaName PostgreSqlTestServerReplica -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5e7d0-111">Esse cmdlet cria uma nova réplica do servidor PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-111">This cmdlet creates a new PostgreSql server replica.</span></span>

## <span data-ttu-id="5e7d0-112">OS</span><span class="sxs-lookup"><span data-stu-id="5e7d0-112">PARAMETERS</span></span>

### <span data-ttu-id="5e7d0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e7d0-113">-AsJob</span></span>
<span data-ttu-id="5e7d0-114">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="5e7d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e7d0-115">-DefaultProfile</span></span>
<span data-ttu-id="5e7d0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e7d0-117">-Local</span><span class="sxs-lookup"><span data-stu-id="5e7d0-117">-Location</span></span>
<span data-ttu-id="5e7d0-118">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="5e7d0-119">-Mestre</span><span class="sxs-lookup"><span data-stu-id="5e7d0-119">-Master</span></span>
<span data-ttu-id="5e7d0-120">O objeto do servidor de origem do qual criar a réplica.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-120">The source server object to create replica from.</span></span>
<span data-ttu-id="5e7d0-121">Para construir, consulte a seção de anotações para propriedades MESTRAs e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e7d0-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5e7d0-122">-NoWait</span></span>
<span data-ttu-id="5e7d0-123">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5e7d0-124">-Replicaname</span><span class="sxs-lookup"><span data-stu-id="5e7d0-124">-ReplicaName</span></span>
<span data-ttu-id="5e7d0-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-125">The name of the server.</span></span>

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

### <span data-ttu-id="5e7d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e7d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e7d0-127">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5e7d0-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="5e7d0-128">-Sku</span></span>
<span data-ttu-id="5e7d0-129">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="5e7d0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e7d0-130">-SubscriptionId</span></span>
<span data-ttu-id="5e7d0-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5e7d0-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e7d0-132">-Confirm</span></span>
<span data-ttu-id="5e7d0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e7d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e7d0-134">-WhatIf</span></span>
<span data-ttu-id="5e7d0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e7d0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e7d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e7d0-137">CommonParameters</span></span>
<span data-ttu-id="5e7d0-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e7d0-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e7d0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e7d0-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e7d0-140">INPUTS</span></span>

### <span data-ttu-id="5e7d0-141">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="5e7d0-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="5e7d0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e7d0-142">OUTPUTS</span></span>

### <span data-ttu-id="5e7d0-143">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="5e7d0-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="5e7d0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e7d0-144">NOTES</span></span>

<span data-ttu-id="5e7d0-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5e7d0-145">ALIASES</span></span>

<span data-ttu-id="5e7d0-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5e7d0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e7d0-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e7d0-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e7d0-149">Mestre <IServer> : o objeto do servidor de origem para o qual criar a réplica.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="5e7d0-150">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-150">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="5e7d0-151">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-151">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="5e7d0-152">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5e7d0-153">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="5e7d0-154">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="5e7d0-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="5e7d0-155">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="5e7d0-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="5e7d0-156">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="5e7d0-157">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="5e7d0-158">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="5e7d0-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status que mostra se o servidor habilitou a criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="5e7d0-160">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="5e7d0-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão do TLS mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="5e7d0-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é ou não permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="5e7d0-163">O valor é opcional, mas se transmitido, deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="5e7d0-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="5e7d0-164">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="5e7d0-165">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="5e7d0-166">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="5e7d0-167">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="5e7d0-168">`[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="5e7d0-169">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="5e7d0-170">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="5e7d0-171">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="5e7d0-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="5e7d0-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="5e7d0-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="5e7d0-175">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="5e7d0-176">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="5e7d0-177">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="5e7d0-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="5e7d0-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e7d0-178">RELATED LINKS</span></span>

