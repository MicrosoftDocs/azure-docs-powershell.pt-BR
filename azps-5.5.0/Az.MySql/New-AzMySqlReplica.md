---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlReplica.md
ms.openlocfilehash: 58158888b99a5f4662de7530576eca084f849966
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118417"
---
# <span data-ttu-id="58a62-101">New-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="58a62-101">New-AzMySqlReplica</span></span>

## <span data-ttu-id="58a62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58a62-102">SYNOPSIS</span></span>
<span data-ttu-id="58a62-103">Cria uma nova réplica de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="58a62-103">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="58a62-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58a62-104">SYNTAX</span></span>

```
New-AzMySqlReplica -Replica <String> -ResourceGroupName <String> -Master <IServer> [-SubscriptionId <String>]
 [-Location <String>] [-Sku <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="58a62-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="58a62-105">DESCRIPTION</span></span>
<span data-ttu-id="58a62-106">Cria uma nova réplica de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="58a62-106">Creates a new replica from an existing database.</span></span>

## <span data-ttu-id="58a62-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58a62-107">EXAMPLES</span></span>

### <span data-ttu-id="58a62-108">Exemplo 1: Criar uma nova replica do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="58a62-108">Example 1: Create a new MySql server replica</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | New-AzMySqlReplica -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="58a62-109">Este cmdlet cria uma nova replica do servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="58a62-109">This cmdlet creates a new MySql server replica.</span></span>

### <span data-ttu-id="58a62-110">Exemplo 2: Criar uma nova replica do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="58a62-110">Example 2: Create a new MySql server replica</span></span>
```powershell
PS C:\> $mysql = Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
PS C:\> New-AzMySqlReplica -Master $mysql -Replica mysql-test-replica -ResourceGroupName PowershellMySqlTest

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="58a62-111">Este cmdlet com parâmetro mestre(inputobject) cria uma nova replica do servidor MySql.</span><span class="sxs-lookup"><span data-stu-id="58a62-111">This cmdlet with parameter master(inputobject) creates a new MySql server replica.</span></span>

## <span data-ttu-id="58a62-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58a62-112">PARAMETERS</span></span>

### <span data-ttu-id="58a62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58a62-113">-AsJob</span></span>
<span data-ttu-id="58a62-114">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="58a62-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="58a62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a62-115">-DefaultProfile</span></span>
<span data-ttu-id="58a62-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58a62-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a62-117">-Local</span><span class="sxs-lookup"><span data-stu-id="58a62-117">-Location</span></span>
<span data-ttu-id="58a62-118">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="58a62-118">The location the resource resides in.</span></span>

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

### <span data-ttu-id="58a62-119">-Mestre</span><span class="sxs-lookup"><span data-stu-id="58a62-119">-Master</span></span>
<span data-ttu-id="58a62-120">O objeto do servidor de origem para criar uma réplica.</span><span class="sxs-lookup"><span data-stu-id="58a62-120">The source server object to create replica from.</span></span>
<span data-ttu-id="58a62-121">Para construir, confira a seção ANOTAÇÕES para propriedades MASTER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="58a62-121">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58a62-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="58a62-122">-NoWait</span></span>
<span data-ttu-id="58a62-123">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="58a62-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="58a62-124">-Replicar</span><span class="sxs-lookup"><span data-stu-id="58a62-124">-Replica</span></span>
<span data-ttu-id="58a62-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-125">The name of the server.</span></span>

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

### <span data-ttu-id="58a62-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a62-126">-ResourceGroupName</span></span>
<span data-ttu-id="58a62-127">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="58a62-127">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="58a62-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="58a62-128">-Sku</span></span>
<span data-ttu-id="58a62-129">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="58a62-129">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="58a62-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58a62-130">-SubscriptionId</span></span>
<span data-ttu-id="58a62-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="58a62-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="58a62-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="58a62-132">-Confirm</span></span>
<span data-ttu-id="58a62-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58a62-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a62-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a62-134">-WhatIf</span></span>
<span data-ttu-id="58a62-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="58a62-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a62-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58a62-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a62-137">CommonParameters</span></span>
<span data-ttu-id="58a62-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58a62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a62-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58a62-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a62-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="58a62-140">INPUTS</span></span>

### <span data-ttu-id="58a62-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="58a62-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="58a62-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="58a62-142">OUTPUTS</span></span>

### <span data-ttu-id="58a62-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="58a62-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="58a62-144">Notas</span><span class="sxs-lookup"><span data-stu-id="58a62-144">NOTES</span></span>

<span data-ttu-id="58a62-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="58a62-145">ALIASES</span></span>

<span data-ttu-id="58a62-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="58a62-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58a62-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="58a62-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58a62-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="58a62-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58a62-149">MASTER: <IServer> O objeto do servidor de origem para criar uma réplica.</span><span class="sxs-lookup"><span data-stu-id="58a62-149">MASTER <IServer>: The source server object to create replica from.</span></span>
  - <span data-ttu-id="58a62-150">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="58a62-150">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="58a62-151">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="58a62-151">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="58a62-152">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="58a62-152">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="58a62-153">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-153">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="58a62-154">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="58a62-154">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="58a62-155">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="58a62-155">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="58a62-156">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-156">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="58a62-157">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="58a62-157">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="58a62-158">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="58a62-158">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="58a62-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-159">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="58a62-160">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="58a62-160">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="58a62-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão TLs mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-161">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="58a62-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-162">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="58a62-163">O valor é opcional, mas, se aprovado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="58a62-163">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="58a62-164">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="58a62-164">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="58a62-165">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-165">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="58a62-166">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-166">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="58a62-167">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="58a62-167">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="58a62-168">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="58a62-168">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="58a62-169">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="58a62-169">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="58a62-170">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="58a62-170">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="58a62-171">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-171">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="58a62-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-172">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="58a62-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-173">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="58a62-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="58a62-174">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="58a62-175">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-175">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="58a62-176">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="58a62-176">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="58a62-177">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="58a62-177">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="58a62-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58a62-178">RELATED LINKS</span></span>

