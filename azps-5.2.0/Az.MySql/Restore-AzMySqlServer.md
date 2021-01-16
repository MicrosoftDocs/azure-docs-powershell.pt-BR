---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/restore-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Restore-AzMySqlServer.md
ms.openlocfilehash: 7a53cefa9aca7e4ea679b31763c19e82d4d1e841
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262672"
---
# <span data-ttu-id="74a3e-101">Restore-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="74a3e-101">Restore-AzMySqlServer</span></span>

## <span data-ttu-id="74a3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74a3e-102">SYNOPSIS</span></span>
<span data-ttu-id="74a3e-103">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="74a3e-103">Restore a server from an existing backup</span></span>

## <span data-ttu-id="74a3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74a3e-104">SYNTAX</span></span>

### <span data-ttu-id="74a3e-105">Georestore (padrão)</span><span class="sxs-lookup"><span data-stu-id="74a3e-105">GeoRestore (Default)</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer> -UseGeoRestore
 [-SubscriptionId <String>] [-Location <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74a3e-106">PointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="74a3e-106">PointInTimeRestore</span></span>
```
Restore-AzMySqlServer -Name <String> -ResourceGroupName <String> -InputObject <IServer>
 -RestorePointInTime <DateTime> -UsePointInTimeRestore [-SubscriptionId <String>] [-Location <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="74a3e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74a3e-107">DESCRIPTION</span></span>
<span data-ttu-id="74a3e-108">Restaurar um servidor de um backup existente</span><span class="sxs-lookup"><span data-stu-id="74a3e-108">Restore a server from an existing backup</span></span>

## <span data-ttu-id="74a3e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74a3e-109">EXAMPLES</span></span>

### <span data-ttu-id="74a3e-110">Exemplo 1: restaurar o servidor MySql usando a restauração georéplica</span><span class="sxs-lookup"><span data-stu-id="74a3e-110">Example 1: Restore MySql server using GeoReplica Restore</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test-replica | Restore-AzMySqlServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -UseGeoRestore 

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="74a3e-111">Esse cmdlet restaura o MySql Server usando a restauração georeplicada.</span><span class="sxs-lookup"><span data-stu-id="74a3e-111">This cmdlet restores MySql server using GeoReplica Restore.</span></span>

### <span data-ttu-id="74a3e-112">Exemplo 2: restaurar o servidor MySql usando a restauração do PointInTime</span><span class="sxs-lookup"><span data-stu-id="74a3e-112">Example 2: Restore MySql server using PointInTime Restore</span></span>
```powershell
PS C:\> $restorePointInTime = (Get-Date).AddMinutes(-10)
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Restore-AzMySqlServer -Name mysql-test-restore -ResourceGroupName PowershellMySqlTest -RestorePointInTime $restorePointInTime -UsePointInTimeRestore

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-restore eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="74a3e-113">Esses cmdlets restauram o MySql Server usando a restauração do PointInTime.</span><span class="sxs-lookup"><span data-stu-id="74a3e-113">These cmdlets restore MySql server using PointInTime Restore.</span></span>

## <span data-ttu-id="74a3e-114">OS</span><span class="sxs-lookup"><span data-stu-id="74a3e-114">PARAMETERS</span></span>

### <span data-ttu-id="74a3e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74a3e-115">-AsJob</span></span>
<span data-ttu-id="74a3e-116">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="74a3e-116">Run the command as a job.</span></span>

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

### <span data-ttu-id="74a3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a3e-117">-DefaultProfile</span></span>
<span data-ttu-id="74a3e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74a3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74a3e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74a3e-119">-InputObject</span></span>
<span data-ttu-id="74a3e-120">O objeto do servidor de origem do qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="74a3e-120">The source server object to restore from.</span></span>
<span data-ttu-id="74a3e-121">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="74a3e-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74a3e-122">-Local</span><span class="sxs-lookup"><span data-stu-id="74a3e-122">-Location</span></span>
<span data-ttu-id="74a3e-123">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="74a3e-123">The location the resource resides in.</span></span>

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

### <span data-ttu-id="74a3e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="74a3e-124">-Name</span></span>
<span data-ttu-id="74a3e-125">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-125">The name of the server.</span></span>

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

### <span data-ttu-id="74a3e-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="74a3e-126">-NoWait</span></span>
<span data-ttu-id="74a3e-127">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="74a3e-127">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="74a3e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74a3e-128">-ResourceGroupName</span></span>
<span data-ttu-id="74a3e-129">O nome do grupo de recursos que contém o recurso, você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="74a3e-129">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="74a3e-130">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="74a3e-130">-RestorePointInTime</span></span>
<span data-ttu-id="74a3e-131">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="74a3e-131">The location the resource resides in.</span></span>

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

### <span data-ttu-id="74a3e-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="74a3e-132">-Sku</span></span>
<span data-ttu-id="74a3e-133">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="74a3e-133">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="74a3e-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74a3e-134">-SubscriptionId</span></span>
<span data-ttu-id="74a3e-135">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="74a3e-135">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="74a3e-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="74a3e-136">-Tag</span></span>
<span data-ttu-id="74a3e-137">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="74a3e-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="74a3e-138">-UseGeoRestore</span><span class="sxs-lookup"><span data-stu-id="74a3e-138">-UseGeoRestore</span></span>
<span data-ttu-id="74a3e-139">Usar o modo geográfico para restaurar</span><span class="sxs-lookup"><span data-stu-id="74a3e-139">Use Geo mode to restore</span></span>

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

### <span data-ttu-id="74a3e-140">-UsePointInTimeRestore</span><span class="sxs-lookup"><span data-stu-id="74a3e-140">-UsePointInTimeRestore</span></span>
<span data-ttu-id="74a3e-141">Usar o modo PointInTime para restaurar</span><span class="sxs-lookup"><span data-stu-id="74a3e-141">Use PointInTime mode to restore</span></span>

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

### <span data-ttu-id="74a3e-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74a3e-142">-Confirm</span></span>
<span data-ttu-id="74a3e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74a3e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74a3e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a3e-144">-WhatIf</span></span>
<span data-ttu-id="74a3e-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74a3e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a3e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74a3e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74a3e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a3e-147">CommonParameters</span></span>
<span data-ttu-id="74a3e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a3e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a3e-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74a3e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a3e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74a3e-150">INPUTS</span></span>

### <span data-ttu-id="74a3e-151">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="74a3e-151">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="74a3e-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74a3e-152">OUTPUTS</span></span>

### <span data-ttu-id="74a3e-153">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="74a3e-153">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="74a3e-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74a3e-154">NOTES</span></span>

<span data-ttu-id="74a3e-155">ALIASES</span><span class="sxs-lookup"><span data-stu-id="74a3e-155">ALIASES</span></span>

<span data-ttu-id="74a3e-156">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="74a3e-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74a3e-157">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="74a3e-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74a3e-158">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74a3e-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74a3e-159">INPUTobject <IServer> : o objeto do servidor de origem para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="74a3e-159">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="74a3e-160">`Location <String>`: A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="74a3e-160">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="74a3e-161">`SkuName <String>`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="74a3e-161">`SkuName <String>`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="74a3e-162">`[Tag <ITrackedResourceTags>]`: Marcas do recurso.</span><span class="sxs-lookup"><span data-stu-id="74a3e-162">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="74a3e-163">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="74a3e-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="74a3e-164">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-164">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="74a3e-165">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="74a3e-165">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="74a3e-166">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="74a3e-166">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="74a3e-167">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-167">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="74a3e-168">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="74a3e-168">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="74a3e-169">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="74a3e-169">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="74a3e-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status que mostra se o servidor habilitou a criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="74a3e-170">`[InfrastructureEncryption <InfrastructureEncryption?>]`: Status showing whether the server enabled infrastructure encryption.</span></span>
  - <span data-ttu-id="74a3e-171">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="74a3e-171">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="74a3e-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Impor uma versão do TLS mínima para o servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-172">`[MinimalTlsVersion <MinimalTlsVersionEnum?>]`: Enforce a minimal Tls version for the server.</span></span>
  - <span data-ttu-id="74a3e-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Se o acesso à rede pública é ou não permitido para este servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-173">`[PublicNetworkAccess <PublicNetworkAccessEnum?>]`: Whether or not public network access is allowed for this server.</span></span> <span data-ttu-id="74a3e-174">O valor é opcional, mas se transmitido, deve ser ' Enabled ' ou ' disabled '</span><span class="sxs-lookup"><span data-stu-id="74a3e-174">Value is optional but if passed in, must be 'Enabled' or 'Disabled'</span></span>
  - <span data-ttu-id="74a3e-175">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="74a3e-175">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="74a3e-176">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-176">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="74a3e-177">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-177">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="74a3e-178">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="74a3e-178">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="74a3e-179">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="74a3e-179">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="74a3e-180">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="74a3e-180">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="74a3e-181">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-181">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="74a3e-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-182">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="74a3e-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-183">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="74a3e-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74a3e-184">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="74a3e-185">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-185">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="74a3e-186">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="74a3e-186">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="74a3e-187">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="74a3e-187">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="74a3e-188">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74a3e-188">RELATED LINKS</span></span>

