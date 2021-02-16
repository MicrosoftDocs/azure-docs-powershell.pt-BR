---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restore-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restore-AzMariaDbServer.md
ms.openlocfilehash: 95988d83cbb4c3dcf0b5da890bf38f8c40eb4dfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118428"
---
# <span data-ttu-id="095f0-101">Restore-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="095f0-101">Restore-AzMariaDbServer</span></span>

## <span data-ttu-id="095f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="095f0-102">SYNOPSIS</span></span>
<span data-ttu-id="095f0-103">Restaure um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="095f0-103">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="095f0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="095f0-104">SYNTAX</span></span>

```
Restore-AzMariaDbServer -Name <String> -RestorePointInTime <DateTime> [-InputObject <IServer>]
 [-ResourceGroupName <String>] [-ServerName <String>] [-SubscriptionId <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="095f0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="095f0-105">DESCRIPTION</span></span>
<span data-ttu-id="095f0-106">Restaure um MariaDB de um MariaDB existente.</span><span class="sxs-lookup"><span data-stu-id="095f0-106">Restore a MariaDB from a existing MariaDB.</span></span>

## <span data-ttu-id="095f0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="095f0-107">EXAMPLES</span></span>

### <span data-ttu-id="095f0-108">Exemplo 1: Restaurar um PointInTime MariaDB pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-108">Example 1: Restore a PointInTime MariaDB by server name.</span></span>
```powershell
PS C:\> Restore-AzMariaDbServer -Name restore-db01 -ServerName mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db01 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="095f0-109">Este comando restaura um PointInTime MariaDB pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-109">This command restore a PointInTime MariaDB by server name.</span></span>

### <span data-ttu-id="095f0-110">Exemplo 2: Restaurar um PointInTime MariaDB por objeto de servidor</span><span class="sxs-lookup"><span data-stu-id="095f0-110">Example 2: Restore a PointInTime MariaDB by server object</span></span>
```powershell
PS C:\> $db = Get-AzMariaDbServer -Name mariadb-test-usegeo -ResourceGroupName mariadb-test-4rih5z
PS C:\>Restore-AzMariaDbServer -Name restore-db02 -InputObject $db -UsePointInTimeRestore -RestorePointInTime $(Get-Date) -Location eastus

Name         Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----         -------- ------------------ ------- ----------------------- -------   -------        --------------
restore-db02 eastus   adminuser          10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="095f0-111">Esse comando restaura um PointInTime MariaDB por objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-111">This command restore a PointInTime MariaDB by server object.</span></span>

## <span data-ttu-id="095f0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="095f0-112">PARAMETERS</span></span>

### <span data-ttu-id="095f0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="095f0-113">-AsJob</span></span>
<span data-ttu-id="095f0-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="095f0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="095f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095f0-115">-DefaultProfile</span></span>
<span data-ttu-id="095f0-116">região DefaultParameters As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="095f0-116">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095f0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="095f0-117">-InputObject</span></span>
<span data-ttu-id="095f0-118">O objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="095f0-118">The source server object to restore from.</span></span>
<span data-ttu-id="095f0-119">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="095f0-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="095f0-120">-Local</span><span class="sxs-lookup"><span data-stu-id="095f0-120">-Location</span></span>
<span data-ttu-id="095f0-121">O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="095f0-121">The location the resource resides in.</span></span>

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

### <span data-ttu-id="095f0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="095f0-122">-Name</span></span>
<span data-ttu-id="095f0-123">O nome do servidor para restauração.</span><span class="sxs-lookup"><span data-stu-id="095f0-123">The dest server name to restore from.</span></span>

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

### <span data-ttu-id="095f0-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="095f0-124">-NoWait</span></span>
<span data-ttu-id="095f0-125">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="095f0-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="095f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="095f0-127">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="095f0-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="095f0-128">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="095f0-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="095f0-129">-RestorePointInTime</span><span class="sxs-lookup"><span data-stu-id="095f0-129">-RestorePointInTime</span></span>
<span data-ttu-id="095f0-130">região PointInTimeRestore O local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="095f0-130">region PointInTimeRestore The location the resource resides in.</span></span>

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

### <span data-ttu-id="095f0-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="095f0-131">-ServerName</span></span>
<span data-ttu-id="095f0-132">O nome do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="095f0-132">The source server name to restore from.</span></span>

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

### <span data-ttu-id="095f0-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="095f0-133">-SubscriptionId</span></span>
<span data-ttu-id="095f0-134">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="095f0-134">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="095f0-135">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="095f0-135">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="095f0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="095f0-136">-Tag</span></span>
<span data-ttu-id="095f0-137">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="095f0-137">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="095f0-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="095f0-138">-Confirm</span></span>
<span data-ttu-id="095f0-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095f0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095f0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095f0-140">-WhatIf</span></span>
<span data-ttu-id="095f0-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="095f0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095f0-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="095f0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095f0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095f0-143">CommonParameters</span></span>
<span data-ttu-id="095f0-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095f0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095f0-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="095f0-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095f0-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="095f0-146">INPUTS</span></span>

### <span data-ttu-id="095f0-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="095f0-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="095f0-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="095f0-148">OUTPUTS</span></span>

### <span data-ttu-id="095f0-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="095f0-149">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="095f0-150">Notas</span><span class="sxs-lookup"><span data-stu-id="095f0-150">NOTES</span></span>

<span data-ttu-id="095f0-151">Aliases</span><span class="sxs-lookup"><span data-stu-id="095f0-151">ALIASES</span></span>

<span data-ttu-id="095f0-152">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="095f0-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="095f0-153">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="095f0-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="095f0-154">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="095f0-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="095f0-155">INPUTOBJECT: <IServer> o objeto do servidor de origem a ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="095f0-155">INPUTOBJECT <IServer>: The source server object to restore from.</span></span>
  - <span data-ttu-id="095f0-156">`Location <String>`: o local em que o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="095f0-156">`Location <String>`: The location the resource resides in.</span></span>
  - <span data-ttu-id="095f0-157">`[Tag <ITrackedResourceTags>]`: Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="095f0-157">`[Tag <ITrackedResourceTags>]`: Application-specific metadata in the form of key-value pairs.</span></span>
    - <span data-ttu-id="095f0-158">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="095f0-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="095f0-159">`[AdministratorLogin <String>]`: o nome de logon do administrador de um servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-159">`[AdministratorLogin <String>]`: The administrator's login name of a server.</span></span> <span data-ttu-id="095f0-160">Só pode ser especificado quando o servidor está sendo criado (e é necessário para criação).</span><span class="sxs-lookup"><span data-stu-id="095f0-160">Can only be specified when the server is being created (and is required for creation).</span></span>
  - <span data-ttu-id="095f0-161">`[EarliestRestoreDate <DateTime?>]`: tempo de criação do ponto de restauração mais antigo (formato ISO8601)</span><span class="sxs-lookup"><span data-stu-id="095f0-161">`[EarliestRestoreDate <DateTime?>]`: Earliest restore point creation time (ISO8601 format)</span></span>
  - <span data-ttu-id="095f0-162">`[FullyQualifiedDomainName <String>]`: o nome de domínio totalmente qualificado de um servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-162">`[FullyQualifiedDomainName <String>]`: The fully qualified domain name of a server.</span></span>
  - <span data-ttu-id="095f0-163">`[IdentityType <IdentityType?>]`: o tipo de identidade.</span><span class="sxs-lookup"><span data-stu-id="095f0-163">`[IdentityType <IdentityType?>]`: The identity type.</span></span> <span data-ttu-id="095f0-164">De definir isso como "SystemAssigned" para criar e atribuir automaticamente uma entidade do Azure Active Directory para o recurso.</span><span class="sxs-lookup"><span data-stu-id="095f0-164">Set this to 'SystemAssigned' in order to automatically create and assign an Azure Active Directory principal for the resource.</span></span>
  - <span data-ttu-id="095f0-165">`[MasterServerId <String>]`: A ID do servidor mestre de um servidor de replicação.</span><span class="sxs-lookup"><span data-stu-id="095f0-165">`[MasterServerId <String>]`: The master server id of a replica server.</span></span>
  - <span data-ttu-id="095f0-166">`[ReplicaCapacity <Int32?>]`: o número máximo de réplicas que um servidor mestre pode ter.</span><span class="sxs-lookup"><span data-stu-id="095f0-166">`[ReplicaCapacity <Int32?>]`: The maximum number of replicas that a master server can have.</span></span>
  - <span data-ttu-id="095f0-167">`[ReplicationRole <String>]`: a função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-167">`[ReplicationRole <String>]`: The replication role of the server.</span></span>
  - <span data-ttu-id="095f0-168">`[SkuCapacity <Int32?>]`: a capacidade de aumento/reajuste, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-168">`[SkuCapacity <Int32?>]`: The scale up/out capacity, representing server's compute units.</span></span>
  - <span data-ttu-id="095f0-169">`[SkuFamily <String>]`: a família de hardware.</span><span class="sxs-lookup"><span data-stu-id="095f0-169">`[SkuFamily <String>]`: The family of hardware.</span></span>
  - <span data-ttu-id="095f0-170">`[SkuName <String>]`: O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="095f0-170">`[SkuName <String>]`: The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>
  - <span data-ttu-id="095f0-171">`[SkuSize <String>]`: o código de tamanho, a ser interpretado pelo recurso conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="095f0-171">`[SkuSize <String>]`: The size code, to be interpreted by resource as appropriate.</span></span>
  - <span data-ttu-id="095f0-172">`[SkuTier <SkuTier?>]`: o nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="095f0-172">`[SkuTier <SkuTier?>]`: The tier of the particular SKU, e.g. Basic.</span></span>
  - <span data-ttu-id="095f0-173">`[SslEnforcement <SslEnforcementEnum?>]`: Habilitar a imposição ssl ou não ao se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-173">`[SslEnforcement <SslEnforcementEnum?>]`: Enable ssl enforcement or not when connect to server.</span></span>
  - <span data-ttu-id="095f0-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-174">`[StorageProfileBackupRetentionDay <Int32?>]`: Backup retention days for the server.</span></span>
  - <span data-ttu-id="095f0-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-175">`[StorageProfileGeoRedundantBackup <GeoRedundantBackup?>]`: Enable Geo-redundant or not for server backup.</span></span>
  - <span data-ttu-id="095f0-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Habilitar o crescimento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="095f0-176">`[StorageProfileStorageAutogrow <StorageAutogrow?>]`: Enable Storage Auto Grow.</span></span>
  - <span data-ttu-id="095f0-177">`[StorageProfileStorageMb <Int32?>]`: armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-177">`[StorageProfileStorageMb <Int32?>]`: Max storage allowed for a server.</span></span>
  - <span data-ttu-id="095f0-178">`[UserVisibleState <ServerState?>]`: um estado de um servidor que está visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="095f0-178">`[UserVisibleState <ServerState?>]`: A state of a server that is visible to user.</span></span>
  - <span data-ttu-id="095f0-179">`[Version <ServerVersion?>]`: Versão do servidor.</span><span class="sxs-lookup"><span data-stu-id="095f0-179">`[Version <ServerVersion?>]`: Server version.</span></span>

## <span data-ttu-id="095f0-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="095f0-180">RELATED LINKS</span></span>

