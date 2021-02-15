---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restore-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restore-AzPostgreSqlServer.md
ms.openlocfilehash: 7eb1105985202bd8cd05a1b2f2e546e4dd834e50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111487"
---
# <span data-ttu-id="7acc8-101">Restore-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="7acc8-101">Restore-AzPostgreSqlServer</span></span>

## <span data-ttu-id="7acc8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7acc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7acc8-103">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="7acc8-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="7acc8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7acc8-104">SYNTAX</span></span>

### <span data-ttu-id="7acc8-105">GeoRestore (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7acc8-105">GeoRestore (Default)</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7acc8-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="7acc8-106">PointInTimeRestore</span></span>
```
Restore-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="7acc8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7acc8-107">DESCRIPTION</span></span>
<span data-ttu-id="7acc8-108">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="7acc8-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="7acc8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7acc8-109">EXAMPLES</span></span>

### <span data-ttu-id="7acc8-110">Exemplo 1: Restaurar o servidor PostgreSql usando a Restauração GeoReplica</span><span class="sxs-lookup"><span data-stu-id="7acc8-110">Example 1: Restore PostgreSql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName postgresqltestserverreplica | Restore-AzPostgreSqlServer -Name PostgreSqlTestServer -ResourceGroupName PostgreSqlTestRG -UseGeoRestore

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7acc8-111">Este cmdlet restaura o servidor PostgreSql usando a Restauração GeoReplica.</span><span class="sxs-lookup"><span data-stu-id="7acc8-111">This cmdlet restores PostgreSql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="7acc8-112">Exemplo 2: Restaurar o servidor PostgreSql usando a Restauração do PointInTime</span><span class="sxs-lookup"><span data-stu-id="7acc8-112">Example 2: Restore PostgreSql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Restore-AzPostgreSqlServer -Name PostgreSqlTestServerGEO -ResourceGroupName PostgreSqlTestRG -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name                    Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                    -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestservergeo eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7acc8-113">Esses cmdlets restauram o servidor PostgreSql usando a Restauração do PointInTime.</span><span class="sxs-lookup"><span data-stu-id="7acc8-113">These cmdlets restore PostgreSql server using PointInTime Restore.</span></span>

## <span data-ttu-id="7acc8-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7acc8-114">PARAMETERS</span></span>

### <span data-ttu-id="7acc8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7acc8-115">-AsJob</span></span>
<span data-ttu-id="7acc8-116">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7acc8-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="7acc8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7acc8-117">-DefaultProfile</span></span>
<span data-ttu-id="7acc8-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7acc8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7acc8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7acc8-119">-InputObject</span></span>
<span data-ttu-id="7acc8-120">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7acc8-120">The source server object to restore from.</span></span>
<span data-ttu-id="7acc8-121">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7acc8-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7acc8-122">-Local</span><span class="sxs-lookup"><span data-stu-id="7acc8-122">-Location</span></span>
<span data-ttu-id="7acc8-123">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7acc8-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7acc8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="7acc8-124">-Name</span></span>
<span data-ttu-id="7acc8-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-125">The name of the server.</span></span>

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

### <span data-ttu-id="7acc8-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7acc8-126">-NoWait</span></span>
<span data-ttu-id="7acc8-127">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="7acc8-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="7acc8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7acc8-128">-ResourceGroupName</span></span>
<span data-ttu-id="7acc8-129">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="7acc8-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7acc8-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="7acc8-130">-RestorePointInTime</span></span>
<span data-ttu-id="7acc8-131">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7acc8-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7acc8-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="7acc8-132">-Sku</span></span>
<span data-ttu-id="7acc8-133">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7acc8-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="7acc8-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7acc8-134">-SubscriptionId</span></span>
<span data-ttu-id="7acc8-135">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="7acc8-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="7acc8-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="7acc8-136">-Tag</span></span>
<span data-ttu-id="7acc8-137">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="7acc8-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7acc8-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="7acc8-138">-UseGeoRestore</span></span>
<span data-ttu-id="7acc8-139">Usar o modo Geo para restaurar</span><span class="sxs-lookup"><span data-stu-id="7acc8-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="7acc8-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="7acc8-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="7acc8-141">Usar o modo PointInTime para restaurar</span><span class="sxs-lookup"><span data-stu-id="7acc8-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="7acc8-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7acc8-142">-Confirm</span></span>
<span data-ttu-id="7acc8-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7acc8-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7acc8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7acc8-144">-WhatIf</span></span>
<span data-ttu-id="7acc8-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7acc8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7acc8-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7acc8-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7acc8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7acc8-147">CommonParameters</span></span>
<span data-ttu-id="7acc8-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7acc8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7acc8-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7acc8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7acc8-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="7acc8-150">INPUTS</span></span>

### <span data-ttu-id="7acc8-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="7acc8-151">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7acc8-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="7acc8-152">OUTPUTS</span></span>

### <span data-ttu-id="7acc8-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="7acc8-153">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="7acc8-154">Notas</span><span class="sxs-lookup"><span data-stu-id="7acc8-154">NOTES</span></span>

<span data-ttu-id="7acc8-155">Aliases</span><span class="sxs-lookup"><span data-stu-id="7acc8-155">ALIASES</span></span>

<span data-ttu-id="7acc8-156">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="7acc8-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7acc8-157">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7acc8-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7acc8-158">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7acc8-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7acc8-159">INPUTOBJECT: <IServer> o objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7acc8-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="7acc8-160">`Location <String>`: a localização geográfica onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="7acc8-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="7acc8-161">`[Tag <ITrackedResourceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="7acc8-161">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="7acc8-162">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="7acc8-162">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7acc8-163">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-163">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="7acc8-164">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="7acc8-164">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="7acc8-165">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="7acc8-165">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="7acc8-166">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-166">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="7acc8-167">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="7acc8-167">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="7acc8-168">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7acc8-168">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="7acc8-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status mostrando se a criptografia de infraestrutura habilitada pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-169">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="7acc8-170">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="7acc8-170">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="7acc8-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão TLs mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-171">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="7acc8-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é permitido ou não para esse servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-172">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="7acc8-173">O valor é opcional, mas, se aprovado, deve ser 'Habilitado' ou 'Desabilitado'</span><span class="sxs-lookup"><span data-stu-id="7acc8-173">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="7acc8-174">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="7acc8-174">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="7acc8-175">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-175">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="7acc8-176">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-176">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="7acc8-177">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="7acc8-177">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="7acc8-178">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7acc8-178">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="7acc8-179">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="7acc8-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="7acc8-180">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="7acc8-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="7acc8-181">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="7acc8-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="7acc8-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="7acc8-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7acc8-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="7acc8-185">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="7acc8-186">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7acc8-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="7acc8-187">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="7acc8-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="7acc8-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7acc8-188">RELATED LINKS</span></span>

