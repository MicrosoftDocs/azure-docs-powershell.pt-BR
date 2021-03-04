---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 95807621ffb054610a5778872db243eea50a7efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887500"
---
# <span data-ttu-id="8213b-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="8213b-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="8213b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8213b-102">SYNOPSIS</span></span>
<span data-ttu-id="8213b-103">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="8213b-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8213b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8213b-104">SYNTAX</span></span>

### <span data-ttu-id="8213b-105">GeoRestore (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8213b-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8213b-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8213b-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8213b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8213b-107">DESCRIPTION</span></span>
<span data-ttu-id="8213b-108">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="8213b-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="8213b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8213b-109">EXAMPLES</span></span>

### <span data-ttu-id="8213b-110">Exemplo 1: Restaurar o servidor MySql usando a Restauração GeoReplica</span><span class="sxs-lookup"><span data-stu-id="8213b-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8213b-111">Este cmdlet restaura o servidor MySql usando o GeoReplica Restore.</span><span class="sxs-lookup"><span data-stu-id="8213b-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="8213b-112">Exemplo 2: Restaurar o servidor MySql usando a Restauração pointintime</span><span class="sxs-lookup"><span data-stu-id="8213b-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="8213b-113">Esses cmdlets restauram o servidor MySql usando a Restauração PointInTime.</span><span class="sxs-lookup"><span data-stu-id="8213b-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="8213b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8213b-114">PARAMETERS</span></span>

### <span data-ttu-id="8213b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8213b-115">-AsJob</span></span>
<span data-ttu-id="8213b-116">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="8213b-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="8213b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8213b-117">-DefaultProfile</span></span>
<span data-ttu-id="8213b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8213b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8213b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8213b-119">-InputObject</span></span>
<span data-ttu-id="8213b-120">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8213b-120">The source server object to restore from.</span></span>
<span data-ttu-id="8213b-121">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8213b-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8213b-122">-Location</span><span class="sxs-lookup"><span data-stu-id="8213b-122">-Location</span></span>
<span data-ttu-id="8213b-123">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="8213b-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="8213b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8213b-124">-Name</span></span>
<span data-ttu-id="8213b-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-125">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8213b-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8213b-126">-NoWait</span></span>
<span data-ttu-id="8213b-127">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8213b-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="8213b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8213b-128">-ResourceGroupName</span></span>
<span data-ttu-id="8213b-129">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="8213b-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8213b-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="8213b-130">-RestorePointInTime</span></span>
<span data-ttu-id="8213b-131">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="8213b-131">The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8213b-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="8213b-132">-Sku</span></span>
<span data-ttu-id="8213b-133">O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8213b-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="8213b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8213b-134">-SubscriptionId</span></span>
<span data-ttu-id="8213b-135">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8213b-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="8213b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="8213b-136">-Tag</span></span>
<span data-ttu-id="8213b-137">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="8213b-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="8213b-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="8213b-138">-UseGeoRestore</span></span>
<span data-ttu-id="8213b-139">Usar o modo Geo para restaurar</span><span class="sxs-lookup"><span data-stu-id="8213b-139">Use Geo mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8213b-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="8213b-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="8213b-141">Usar o modo PointInTime para restaurar</span><span class="sxs-lookup"><span data-stu-id="8213b-141">Use PointInTime mode to restore</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeRestore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8213b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8213b-142">-Confirm</span></span>
<span data-ttu-id="8213b-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8213b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8213b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8213b-144">-WhatIf</span></span>
<span data-ttu-id="8213b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8213b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8213b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8213b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8213b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8213b-147">CommonParameters</span></span>
<span data-ttu-id="8213b-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8213b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8213b-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8213b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8213b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8213b-150">INPUTS</span></span>

### <span data-ttu-id="8213b-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8213b-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8213b-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8213b-152">OUTPUTS</span></span>

### <span data-ttu-id="8213b-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="8213b-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="8213b-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="8213b-154">NOTES</span></span>

<span data-ttu-id="8213b-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8213b-155">ALIASES</span></span>

<span data-ttu-id="8213b-156">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="8213b-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8213b-157">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8213b-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8213b-158">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8213b-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8213b-159">INPUTOBJECT <IServer> : O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="8213b-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="8213b-160">`Location <String>`: A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="8213b-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="8213b-161">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="8213b-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="8213b-162">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="8213b-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8213b-163">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="8213b-164">Só pode ser especificado quando o servidor está sendo criado (e é necessário para a criação).</span><span class="sxs-lookup"><span data-stu-id="8213b-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="8213b-165">`[EarliestRestoreDate <DateTime?>]`: Tempo de criação de ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="8213b-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="8213b-166">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="8213b-167">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="8213b-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="8213b-168">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="8213b-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="8213b-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="8213b-170">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="8213b-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="8213b-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão Tls mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="8213b-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="8213b-173">O valor é opcional, mas, se passado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="8213b-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="8213b-174">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="8213b-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="8213b-175">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="8213b-176">`[SkuCapacity <Int32?>]`: A capacidade de dimensionar/sair, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="8213b-177">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="8213b-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="8213b-178">`[SkuName <String>]`: O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="8213b-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="8213b-179">`[SkuSize <String>]`: O código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="8213b-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="8213b-180">`[SkuTier <SkuTier?>]`: A camada da SKU específica, por exemplo, Basic.</span><span class="sxs-lookup"><span data-stu-id="8213b-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="8213b-181">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="8213b-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="8213b-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar geo redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="8213b-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8213b-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="8213b-185">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="8213b-186">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="8213b-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="8213b-187">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="8213b-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="8213b-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8213b-188">RELATED LINKS</span></span>

