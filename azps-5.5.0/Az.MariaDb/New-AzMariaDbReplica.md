---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbReplica.md
ms.openlocfilehash: 0ce25af607d2460abf2ec4585dacc124a1f2e65c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112999"
---
# <span data-ttu-id="7f589-101">New-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="7f589-101">New-AzMariaDbReplica</span></span>

## <span data-ttu-id="7f589-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f589-102">SYNOPSIS</span></span>
<span data-ttu-id="7f589-103">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-103">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="7f589-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f589-104">SYNTAX</span></span>

### <span data-ttu-id="7f589-105">Nomedo Servidor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7f589-105">ServerName (Default)</span></span>
```
New-AzMariaDbReplica -MasterName <String> -ReplicaName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7f589-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="7f589-106">ServerObject</span></span>
```
New-AzMariaDbReplica -Master <IServer> -ReplicaName <String> [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7f589-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f589-107">DESCRIPTION</span></span>
<span data-ttu-id="7f589-108">Cria uma réplica de um servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-108">Creates a replica of a MariaDB server.</span></span>

## <span data-ttu-id="7f589-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f589-109">EXAMPLES</span></span>

### <span data-ttu-id="7f589-110">Exemplo 1: Criar uma replica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="7f589-110">Example 1: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbReplica -MasterName mariadb-test-9pebvn -ReplicaName mariadb-test-9pebvn-rep01 -ResourceGroupName mariadb-test-qu5ov0

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep01 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7f589-111">Esse comando cria uma replica db para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-111">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="7f589-112">Exemplo 2: Criar uma replica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="7f589-112">Example 2: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | New-AzMariaDbReplica -ReplicaName mariadb-test-9pebvn-rep02

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep02 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7f589-113">Esse comando cria uma replica db para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-113">This command creates a replica db for a MariaDB.</span></span>

### <span data-ttu-id="7f589-114">Exemplo 3: Criar uma replica db para um MariaDB</span><span class="sxs-lookup"><span data-stu-id="7f589-114">Example 3: Create a replica db for a MariaDB</span></span>
```powershell
PS C:\> $mariaDb = Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 
PS C:\> New-AzMariaDbReplica -Master $mariaDb -ReplicaName mariadb-test-9pebvn-rep03

Name                      Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                      -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-9pebvn-rep03 eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7f589-115">Esse comando com inputobject de parâmetro cria uma replica db com inputobject de parâmetro para um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-115">This command with parameter inputobject creates a replica db with parameter inputobject for a MariaDB.</span></span>

## <span data-ttu-id="7f589-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f589-116">PARAMETERS</span></span>

### <span data-ttu-id="7f589-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f589-117">-AsJob</span></span>
<span data-ttu-id="7f589-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7f589-118">Run the command as a job</span></span>

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

### <span data-ttu-id="7f589-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f589-119">-DefaultProfile</span></span>
<span data-ttu-id="7f589-120">região DefaultParameters As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f589-120">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f589-121">-Local</span><span class="sxs-lookup"><span data-stu-id="7f589-121">-Location</span></span>
<span data-ttu-id="7f589-122">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7f589-122">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7f589-123">-Mestre</span><span class="sxs-lookup"><span data-stu-id="7f589-123">-Master</span></span>
<span data-ttu-id="7f589-124">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7f589-124">The source server object to restore from.</span></span>
<span data-ttu-id="7f589-125">Para construir, confira a seção ANOTAÇÕES para propriedades MASTER e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7f589-125">To construct, see NOTES section for MASTER properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f589-126">-NomeDoMedo Mestre</span><span class="sxs-lookup"><span data-stu-id="7f589-126">-MasterName</span></span>
<span data-ttu-id="7f589-127">Nome do servidor MariaDB.</span><span class="sxs-lookup"><span data-stu-id="7f589-127">MariaDB server name.</span></span>

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

### <span data-ttu-id="7f589-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7f589-128">-NoWait</span></span>
<span data-ttu-id="7f589-129">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="7f589-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7f589-130">-ReplicaName</span><span class="sxs-lookup"><span data-stu-id="7f589-130">-ReplicaName</span></span>
<span data-ttu-id="7f589-131">Replicar nome.</span><span class="sxs-lookup"><span data-stu-id="7f589-131">Replica name.</span></span>

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

### <span data-ttu-id="7f589-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f589-132">-ResourceGroupName</span></span>
<span data-ttu-id="7f589-133">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="7f589-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7f589-134">-SKU</span><span class="sxs-lookup"><span data-stu-id="7f589-134">-Sku</span></span>
<span data-ttu-id="7f589-135">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7f589-135">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="7f589-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f589-136">-SubscriptionId</span></span>
<span data-ttu-id="7f589-137">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7f589-137">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7f589-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f589-138">-Tag</span></span>
<span data-ttu-id="7f589-139">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="7f589-139">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7f589-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7f589-140">-Confirm</span></span>
<span data-ttu-id="7f589-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f589-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f589-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f589-142">-WhatIf</span></span>
<span data-ttu-id="7f589-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7f589-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f589-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f589-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f589-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f589-145">CommonParameters</span></span>
<span data-ttu-id="7f589-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f589-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f589-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f589-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f589-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="7f589-148">INPUTS</span></span>

### <span data-ttu-id="7f589-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7f589-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7f589-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="7f589-150">OUTPUTS</span></span>

### <span data-ttu-id="7f589-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7f589-151">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7f589-152">Notas</span><span class="sxs-lookup"><span data-stu-id="7f589-152">NOTES</span></span>

<span data-ttu-id="7f589-153">Aliases</span><span class="sxs-lookup"><span data-stu-id="7f589-153">ALIASES</span></span>

<span data-ttu-id="7f589-154">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="7f589-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f589-155">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7f589-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f589-156">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f589-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f589-157">MASTER: <IServer> O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7f589-157">MASTER <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="7f589-158">`Location <String>`: o local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7f589-158">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="7f589-159">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="7f589-159">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="7f589-160">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="7f589-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7f589-161">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-161">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="7f589-162">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="7f589-162">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="7f589-163">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="7f589-163">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="7f589-164">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-164">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="7f589-165">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="7f589-165">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="7f589-166">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7f589-166">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="7f589-167">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="7f589-167">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="7f589-168">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="7f589-168">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="7f589-169">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-169">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="7f589-170">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-170">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="7f589-171">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="7f589-171">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="7f589-172">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7f589-172">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="7f589-173">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="7f589-173">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="7f589-174">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="7f589-174">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="7f589-175">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-175">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="7f589-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-176">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="7f589-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-177">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="7f589-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7f589-178">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="7f589-179">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-179">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="7f589-180">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7f589-180">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="7f589-181">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="7f589-181">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="7f589-182">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f589-182">RELATED LINKS</span></span>

