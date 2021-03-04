---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 092e109de5fd38fcad924886f55d918a91e12aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892139"
---
# <span data-ttu-id="7b6b2-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="7b6b2-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="7b6b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7b6b2-103">Restaure um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="7b6b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b6b2-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7b6b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b6b2-105">DESCRIPTION</span></span>
<span data-ttu-id="7b6b2-106">Restaure um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="7b6b2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-107">EXAMPLES</span></span>

### <span data-ttu-id="7b6b2-108">Exemplo 1: Restaurar um PointInTime MariaDB pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7b6b2-109">Este comando restaura um PointInTime MariaDB pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="7b6b2-110">Exemplo 2: Restaurar um PointInTime MariaDB pelo objeto server</span><span class="sxs-lookup"><span data-stu-id="7b6b2-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="7b6b2-111">Este comando restaura um Objeto PointInTime MariaDB por servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="7b6b2-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-112">PARAMETERS</span></span>

### <span data-ttu-id="7b6b2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b6b2-113">-AsJob</span></span>
<span data-ttu-id="7b6b2-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="7b6b2-114">Run the command as a job</span></span>

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

### <span data-ttu-id="7b6b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b6b2-115">-DefaultProfile</span></span>
<span data-ttu-id="7b6b2-116">região DefaultParameters As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b6b2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b6b2-117">-InputObject</span></span>
<span data-ttu-id="7b6b2-118">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-118">The source server object to restore from.</span></span>
<span data-ttu-id="7b6b2-119">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7b6b2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7b6b2-120">-Location</span></span>
<span data-ttu-id="7b6b2-121">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="7b6b2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7b6b2-122">-Name</span></span>
<span data-ttu-id="7b6b2-123">O nome do servidor de dest a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="7b6b2-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7b6b2-124">-NoWait</span></span>
<span data-ttu-id="7b6b2-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="7b6b2-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="7b6b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b6b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b6b2-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7b6b2-128">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="7b6b2-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="7b6b2-129">-RestorePointInTime</span></span>
<span data-ttu-id="7b6b2-130">região PointInTimeRestore O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="7b6b2-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7b6b2-131">-ServerName</span></span>
<span data-ttu-id="7b6b2-132">O nome do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="7b6b2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b6b2-133">-SubscriptionId</span></span>
<span data-ttu-id="7b6b2-134">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7b6b2-135">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7b6b2-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="7b6b2-136">-Tag</span></span>
<span data-ttu-id="7b6b2-137">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="7b6b2-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b6b2-138">-Confirm</span></span>
<span data-ttu-id="7b6b2-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b6b2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b6b2-140">-WhatIf</span></span>
<span data-ttu-id="7b6b2-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b6b2-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b6b2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b6b2-143">CommonParameters</span></span>
<span data-ttu-id="7b6b2-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b6b2-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b6b2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b6b2-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-146">INPUTS</span></span>

### <span data-ttu-id="7b6b2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7b6b2-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7b6b2-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-148">OUTPUTS</span></span>

### <span data-ttu-id="7b6b2-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="7b6b2-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="7b6b2-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b6b2-150">NOTES</span></span>

<span data-ttu-id="7b6b2-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7b6b2-151">ALIASES</span></span>

<span data-ttu-id="7b6b2-152">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7b6b2-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7b6b2-153">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7b6b2-154">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7b6b2-155">INPUTOBJECT <IServer> : O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="7b6b2-156">`Location <String>`: O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="7b6b2-157">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="7b6b2-158">`[(Any) <String>]`: Isso indica que qualquer propriedade pode ser adicionada a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7b6b2-159">`[AdministratorLogin <String>]`: O nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="7b6b2-160">Só pode ser especificado quando o servidor está sendo criado (e é necessário para a criação).</span><span class="sxs-lookup"><span data-stu-id="7b6b2-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="7b6b2-161">`[EarliestRestoreDate <DateTime?>]`: Tempo de criação de ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="7b6b2-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="7b6b2-162">`[FullyQualifiedDomainName <String>]`: O nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="7b6b2-163">`[IdentityType <IdentityType?>]`: O tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="7b6b2-164">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="7b6b2-165">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de réplica.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="7b6b2-166">`[ReplicaCapacity <Int32?>]`: O número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="7b6b2-167">`[ReplicationRole <String>]`: A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="7b6b2-168">`[SkuCapacity <Int32?>]`: A capacidade de dimensionar/sair, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="7b6b2-169">`[SkuFamily <String>]`: A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="7b6b2-170">`[SkuName <String>]`: O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="7b6b2-171">`[SkuSize <String>]`: O código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="7b6b2-172">`[SkuTier <SkuTier?>]`: A camada da SKU específica, por exemplo, Basic.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="7b6b2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="7b6b2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="7b6b2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar geo redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="7b6b2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="7b6b2-177">`[StorageProfileStorageMb <Int32?>]`: Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="7b6b2-178">`[UserVisibleState <ServerState?>]`: Um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="7b6b2-179">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="7b6b2-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="7b6b2-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b6b2-180">RELATED LINKS</span></span>

