---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126035"
---
# <span data-ttu-id="c93c2-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="c93c2-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="c93c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c93c2-102">SYNOPSIS</span></span>
<span data-ttu-id="c93c2-103">Restaurar um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="c93c2-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="c93c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c93c2-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c93c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c93c2-105">DESCRIPTION</span></span>
<span data-ttu-id="c93c2-106">Restaurar um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="c93c2-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="c93c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c93c2-107">EXAMPLES</span></span>

### <span data-ttu-id="c93c2-108">Exemplo 1: restaurar um PointInTime MariaDB por nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c93c2-109">Esse comando restaura um PointInTime MariaDB pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="c93c2-110">Exemplo 2: restaurar um PointInTime MariaDB por objeto do servidor</span><span class="sxs-lookup"><span data-stu-id="c93c2-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c93c2-111">Esse comando restaura um PointInTime MariaDB por objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="c93c2-112">OS</span><span class="sxs-lookup"><span data-stu-id="c93c2-112">PARAMETERS</span></span>

### <span data-ttu-id="c93c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c93c2-113">-AsJob</span></span>
<span data-ttu-id="c93c2-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c93c2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c93c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93c2-115">-DefaultProfile</span></span>
<span data-ttu-id="c93c2-116">Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c93c2-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c93c2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c93c2-117">-InputObject</span></span>
<span data-ttu-id="c93c2-118">O objeto do servidor de origem do qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c93c2-118">The source server object to restore from.</span></span>
<span data-ttu-id="c93c2-119">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c93c2-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c93c2-120">-Local</span><span class="sxs-lookup"><span data-stu-id="c93c2-120">-Location</span></span>
<span data-ttu-id="c93c2-121">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="c93c2-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="c93c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c93c2-122">-Name</span></span>
<span data-ttu-id="c93c2-123">O nome do servidor de destino do qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c93c2-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="c93c2-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c93c2-124">-NoWait</span></span>
<span data-ttu-id="c93c2-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c93c2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c93c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="c93c2-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="c93c2-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c93c2-128">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="c93c2-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c93c2-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="c93c2-129">-RestorePointInTime</span></span>
<span data-ttu-id="c93c2-130">região PointInTimeRestore o local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="c93c2-130">region PointInTimeRestore The location the resource resides in.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c93c2-131">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="c93c2-131">-ServerName</span></span>
<span data-ttu-id="c93c2-132">O nome do servidor de origem para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c93c2-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="c93c2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c93c2-133">-SubscriptionId</span></span>
<span data-ttu-id="c93c2-134">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c93c2-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c93c2-135">A ID da assinatura é parte do URI de cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c93c2-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c93c2-136">-Marca</span><span class="sxs-lookup"><span data-stu-id="c93c2-136">-Tag</span></span>
<span data-ttu-id="c93c2-137">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c93c2-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="c93c2-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c93c2-138">-Confirm</span></span>
<span data-ttu-id="c93c2-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c93c2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93c2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c93c2-140">-WhatIf</span></span>
<span data-ttu-id="c93c2-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c93c2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93c2-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c93c2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93c2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93c2-143">CommonParameters</span></span>
<span data-ttu-id="c93c2-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93c2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93c2-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c93c2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93c2-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c93c2-146">INPUTS</span></span>

### <span data-ttu-id="c93c2-147">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c93c2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c93c2-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c93c2-148">OUTPUTS</span></span>

### <span data-ttu-id="c93c2-149">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="c93c2-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c93c2-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c93c2-150">NOTES</span></span>

<span data-ttu-id="c93c2-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c93c2-151">ALIASES</span></span>

<span data-ttu-id="c93c2-152">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c93c2-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c93c2-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c93c2-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c93c2-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c93c2-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c93c2-155">INPUTobject <IServer> : o objeto do servidor de origem para o qual restaurar.</span><span class="sxs-lookup"><span data-stu-id="c93c2-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="c93c2-156">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="c93c2-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="c93c2-157">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="c93c2-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="c93c2-158">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="c93c2-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="c93c2-159">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="c93c2-160">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="c93c2-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="c93c2-161">`[EarliestRestoreDate <DateTime?>]`: Hora de criação do ponto de restauração mais antiga (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="c93c2-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="c93c2-162">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="c93c2-163">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="c93c2-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="c93c2-164">Defina como "SystemAssigned" para criar e atribuir automaticamente uma entidade de segurança do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c93c2-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="c93c2-165">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="c93c2-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="c93c2-166">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="c93c2-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="c93c2-167">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="c93c2-168">`[SkuCapacity <Int32?>]`: A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="c93c2-169">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="c93c2-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="c93c2-170">`[SkuName <String>]`: O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="c93c2-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="c93c2-171">`[SkuSize <String>]`: O código de tamanho a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="c93c2-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="c93c2-172">`[SkuTier <SkuTier?>]`: A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="c93c2-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="c93c2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="c93c2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="c93c2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="c93c2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c93c2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="c93c2-177">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="c93c2-178">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que é visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c93c2-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="c93c2-179">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="c93c2-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="c93c2-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c93c2-180">RELATED LINKS</span></span>

