---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 3e3e63bee89eb9ae89cb647b81ea7d0da792ae3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887710"
---
# <span data-ttu-id="cc221-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="cc221-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="cc221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc221-102">SYNOPSIS</span></span>
<span data-ttu-id="cc221-103">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="cc221-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc221-104">SYNTAX</span></span>

### <span data-ttu-id="cc221-105">ServerName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc221-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc221-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="cc221-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cc221-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc221-107">DESCRIPTION</span></span>
<span data-ttu-id="cc221-108">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="cc221-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc221-109">EXAMPLES</span></span>

### <span data-ttu-id="cc221-110">Exemplo 1: Criar uma réplica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="cc221-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cc221-111">Este comando cria uma réplica db para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="cc221-112">Exemplo 2: Criar uma réplica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="cc221-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cc221-113">Este comando cria uma réplica db para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="cc221-114">Exemplo 3: Criar uma réplica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="cc221-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="cc221-115">Esse comando com inputobject de parâmetro cria uma réplica db com inputobject de parâmetro para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="cc221-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc221-116">PARAMETERS</span></span>

### <span data-ttu-id="cc221-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc221-117">-AsJob</span></span>
<span data-ttu-id="cc221-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="cc221-118">Run the command as a job</span></span>

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

### <span data-ttu-id="cc221-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc221-119">-DefaultProfile</span></span>
<span data-ttu-id="cc221-120">região DefaultParameters As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc221-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc221-121">-Location</span><span class="sxs-lookup"><span data-stu-id="cc221-121">-Location</span></span>
<span data-ttu-id="cc221-122">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="cc221-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="cc221-123">-Master</span><span class="sxs-lookup"><span data-stu-id="cc221-123">-Master</span></span>
<span data-ttu-id="cc221-124">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="cc221-124">The source server object to restore from.</span></span>
<span data-ttu-id="cc221-125">Para construir, consulte a seção NOTES para propriedades MASTER e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cc221-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: ServerObject
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc221-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="cc221-126">-MasterName</span></span>
<span data-ttu-id="cc221-127">Nome do servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="cc221-127">MariaDB server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc221-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc221-128">-NoWait</span></span>
<span data-ttu-id="cc221-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="cc221-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc221-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="cc221-130">-ReplicaName</span></span>
<span data-ttu-id="cc221-131">Nome da réplica.</span><span class="sxs-lookup"><span data-stu-id="cc221-131">Replica name.</span></span>

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

### <span data-ttu-id="cc221-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc221-132">-ResourceGroupName</span></span>
<span data-ttu-id="cc221-133">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="cc221-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc221-134">-Sku</span><span class="sxs-lookup"><span data-stu-id="cc221-134">-Sku</span></span>
<span data-ttu-id="cc221-135">O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cc221-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="cc221-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc221-136">-SubscriptionId</span></span>
<span data-ttu-id="cc221-137">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="cc221-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cc221-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc221-138">-Tag</span></span>
<span data-ttu-id="cc221-139">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="cc221-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="cc221-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc221-140">-Confirm</span></span>
<span data-ttu-id="cc221-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc221-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc221-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc221-142">-WhatIf</span></span>
<span data-ttu-id="cc221-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc221-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc221-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc221-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc221-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc221-145">CommonParameters</span></span>
<span data-ttu-id="cc221-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc221-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc221-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc221-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc221-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc221-148">INPUTS</span></span>

### <span data-ttu-id="cc221-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cc221-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cc221-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc221-150">OUTPUTS</span></span>

### <span data-ttu-id="cc221-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="cc221-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="cc221-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc221-152">NOTES</span></span>

<span data-ttu-id="cc221-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc221-153">ALIASES</span></span>

<span data-ttu-id="cc221-154">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cc221-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc221-155">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cc221-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc221-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc221-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc221-157">MASTER <IServer> : O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="cc221-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="cc221-158">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="cc221-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="cc221-159">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="cc221-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="cc221-160">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="cc221-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="cc221-161">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="cc221-162">Só pode ser especificado quando o servidor está sendo criado (e é necessário para a criação).</span><span class="sxs-lookup"><span data-stu-id="cc221-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="cc221-163">`[EarliestRestoreDate <DateTime?>]`: Tempo de criação de ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="cc221-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="cc221-164">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="cc221-165">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="cc221-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="cc221-166">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="cc221-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="cc221-167">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="cc221-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="cc221-168">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="cc221-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="cc221-169">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="cc221-170">`[SkuCapacity <Int32?>]`: A capacidade de dimensionar/sair, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="cc221-171">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="cc221-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="cc221-172">`[SkuName <String>]`: O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="cc221-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="cc221-173">`[SkuSize <String>]`: O código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="cc221-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="cc221-174">`[SkuTier <SkuTier?>]`: A camada da SKU específica, por exemplo, Basic.</span><span class="sxs-lookup"><span data-stu-id="cc221-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="cc221-175">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="cc221-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="cc221-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar geo redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="cc221-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cc221-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="cc221-179">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="cc221-180">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="cc221-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="cc221-181">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="cc221-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="cc221-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc221-182">RELATED LINKS</span></span>

