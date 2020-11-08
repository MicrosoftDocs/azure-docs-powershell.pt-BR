---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113519"
---
# <span data-ttu-id="c25bf-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="c25bf-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="c25bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c25bf-102">SYNOPSIS</span></span>
<span data-ttu-id="c25bf-103">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="c25bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c25bf-104">SYNTAX</span></span>

### <span data-ttu-id="c25bf-105">ServerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c25bf-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c25bf-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="c25bf-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c25bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c25bf-107">DESCRIPTION</span></span>
<span data-ttu-id="c25bf-108">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="c25bf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c25bf-109">EXAMPLES</span></span>

### <span data-ttu-id="c25bf-110">Exemplo 1: criar um BD de réplica para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="c25bf-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c25bf-111">Esse comando cria um BD de réplica para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="c25bf-112">Exemplo 2: criar um BD de réplica para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="c25bf-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c25bf-113">Esse comando cria um BD de réplica para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="c25bf-114">Exemplo 3: criar um BD de réplica para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="c25bf-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c25bf-115">Esse comando com o parâmetro InputObject cria um BD de réplica com o parâmetro InputObject para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="c25bf-116">OS</span><span class="sxs-lookup"><span data-stu-id="c25bf-116">PARAMETERS</span></span>

### <span data-ttu-id="c25bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c25bf-117">-AsJob</span></span>
<span data-ttu-id="c25bf-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c25bf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c25bf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25bf-119">-DefaultProfile</span></span>
<span data-ttu-id="c25bf-120">Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c25bf-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25bf-121">-Local</span><span class="sxs-lookup"><span data-stu-id="c25bf-121">-Location</span></span>
<span data-ttu-id="c25bf-122">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="c25bf-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c25bf-123">-Mestre</span><span class="sxs-lookup"><span data-stu-id="c25bf-123">-Master</span></span>
<span data-ttu-id="c25bf-124">O objeto do servidor de origem do qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c25bf-124">The source server object to restore from.</span></span>
<span data-ttu-id="c25bf-125">Para construir, consulte a seção de anotações para propriedades MESTRAs e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c25bf-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="c25bf-126">-MasterName</span><span class="sxs-lookup"><span data-stu-id="c25bf-126">-MasterName</span></span>
<span data-ttu-id="c25bf-127">Nome do servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c25bf-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="c25bf-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c25bf-128">-NoWait</span></span>
<span data-ttu-id="c25bf-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c25bf-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c25bf-130">-Replicaname</span><span class="sxs-lookup"><span data-stu-id="c25bf-130">-ReplicaName</span></span>
<span data-ttu-id="c25bf-131">Nome da réplica.</span><span class="sxs-lookup"><span data-stu-id="c25bf-131">Replica name.</span></span>

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

### <span data-ttu-id="c25bf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25bf-132">-ResourceGroupName</span></span>
<span data-ttu-id="c25bf-133">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="c25bf-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c25bf-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="c25bf-134">-Sku</span></span>
<span data-ttu-id="c25bf-135">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c25bf-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="c25bf-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c25bf-136">-SubscriptionId</span></span>
<span data-ttu-id="c25bf-137">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c25bf-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c25bf-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="c25bf-138">-Tag</span></span>
<span data-ttu-id="c25bf-139">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c25bf-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c25bf-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c25bf-140">-Confirm</span></span>
<span data-ttu-id="c25bf-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c25bf-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25bf-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25bf-142">-WhatIf</span></span>
<span data-ttu-id="c25bf-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c25bf-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25bf-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c25bf-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25bf-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25bf-145">CommonParameters</span></span>
<span data-ttu-id="c25bf-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25bf-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25bf-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c25bf-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25bf-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c25bf-148">INPUTS</span></span>

### <span data-ttu-id="c25bf-149">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c25bf-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c25bf-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c25bf-150">OUTPUTS</span></span>

### <span data-ttu-id="c25bf-151">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c25bf-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c25bf-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c25bf-152">NOTES</span></span>

<span data-ttu-id="c25bf-153">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c25bf-153">ALIASES</span></span>

<span data-ttu-id="c25bf-154">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c25bf-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c25bf-155">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c25bf-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c25bf-156">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c25bf-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c25bf-157">Mestre <IServer> : o objeto do servidor de origem para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c25bf-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="c25bf-158">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="c25bf-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="c25bf-159">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c25bf-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="c25bf-160">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c25bf-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c25bf-161">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c25bf-162">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="c25bf-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c25bf-163">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="c25bf-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c25bf-164">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c25bf-165">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="c25bf-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c25bf-166">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c25bf-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c25bf-167">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="c25bf-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c25bf-168">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="c25bf-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c25bf-169">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c25bf-170">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c25bf-171">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="c25bf-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c25bf-172">`[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c25bf-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c25bf-173">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="c25bf-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c25bf-174">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="c25bf-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c25bf-175">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c25bf-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c25bf-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c25bf-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c25bf-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c25bf-179">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c25bf-180">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c25bf-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c25bf-181">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="c25bf-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c25bf-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c25bf-182">RELATED LINKS</span></span>

