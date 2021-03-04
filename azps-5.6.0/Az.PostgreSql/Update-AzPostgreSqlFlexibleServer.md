---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 65004c35ffa9c4cb227845787c91219a319789fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888219"
---
# <span data-ttu-id="a6537-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="a6537-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="a6537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6537-102">SYNOPSIS</span></span>
<span data-ttu-id="a6537-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="a6537-103">Updates an existing server.</span></span>
<span data-ttu-id="a6537-104">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a6537-105">Use Update-AzPostSqlFlexibleServerConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a6537-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a6537-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a6537-106">SYNTAX</span></span>

### <span data-ttu-id="a6537-107">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6537-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6537-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a6537-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-MaintenanceWindow <String>] [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6537-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a6537-109">DESCRIPTION</span></span>
<span data-ttu-id="a6537-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="a6537-110">Updates an existing server.</span></span>
<span data-ttu-id="a6537-111">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="a6537-112">Use Update-AzPostgreSqlFlexibleServerConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="a6537-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="a6537-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6537-113">EXAMPLES</span></span>

### <span data-ttu-id="a6537-114">Exemplo 1: Atualizar servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="a6537-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="a6537-115">Este cmdlet atualiza o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="a6537-116">Exemplo 2: Atualizar servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="a6537-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="a6537-117">Este cmdlet atualiza o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="a6537-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="a6537-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a6537-118">PARAMETERS</span></span>

### <span data-ttu-id="a6537-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="a6537-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="a6537-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="a6537-120">The password of the administrator login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6537-121">-AsJob</span></span>
<span data-ttu-id="a6537-122">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6537-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="a6537-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="a6537-123">-BackupRetentionDay</span></span>
<span data-ttu-id="a6537-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-124">Backup retention days for the server.</span></span>
<span data-ttu-id="a6537-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="a6537-125">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6537-126">-DefaultProfile</span></span>
<span data-ttu-id="a6537-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6537-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6537-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="a6537-128">-HaEnabled</span></span>
<span data-ttu-id="a6537-129">Habilitar ou desabilitar o recurso de alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="a6537-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6537-130">-InputObject</span></span>
<span data-ttu-id="a6537-131">Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="a6537-131">Identity Parameter.</span></span>
<span data-ttu-id="a6537-132">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a6537-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-133">-MaintenanceWindow</span><span class="sxs-lookup"><span data-stu-id="a6537-133">-MaintenanceWindow</span></span>
<span data-ttu-id="a6537-134">Período de tempo (UTC) designado para manutenção.</span><span class="sxs-lookup"><span data-stu-id="a6537-134">Period of time (UTC) designated for maintenance.</span></span>
<span data-ttu-id="a6537-135">Exemplos: "Sun:23:30" para agendar no domingo, 11:30pm UTC.</span><span class="sxs-lookup"><span data-stu-id="a6537-135">Examples: "Sun:23:30" to schedule on Sunday, 11:30pm UTC.</span></span>
<span data-ttu-id="a6537-136">Para definir de volta para o passe padrão em "Desabilitado"</span><span class="sxs-lookup"><span data-stu-id="a6537-136">To set back to default pass in "Disabled"</span></span>

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

### <span data-ttu-id="a6537-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a6537-137">-Name</span></span>
<span data-ttu-id="a6537-138">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-138">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-139">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6537-139">-NoWait</span></span>
<span data-ttu-id="a6537-140">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a6537-140">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a6537-141">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="a6537-141">-ReplicationRole</span></span>
<span data-ttu-id="a6537-142">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-142">The replication role of the server.</span></span>

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

### <span data-ttu-id="a6537-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6537-143">-ResourceGroupName</span></span>
<span data-ttu-id="a6537-144">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a6537-144">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a6537-145">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a6537-145">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="a6537-146">-Sku</span></span>
<span data-ttu-id="a6537-147">O nome do sku, por exemplo, Burstable_B1ms, Standard_D2ds_v4</span><span class="sxs-lookup"><span data-stu-id="a6537-147">The name of the sku, e.g. Burstable_B1ms, Standard_D2ds_v4</span></span>

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

### <span data-ttu-id="a6537-148">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a6537-148">-SkuTier</span></span>
<span data-ttu-id="a6537-149">A camada do SKU específico.</span><span class="sxs-lookup"><span data-stu-id="a6537-149">The tier of the particular SKU.</span></span>
<span data-ttu-id="a6537-150">Valores aceitos: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="a6537-150">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="a6537-151">Padrão: imbatível.</span><span class="sxs-lookup"><span data-stu-id="a6537-151">Default: Burstable.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-152">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="a6537-152">-SslEnforcement</span></span>
<span data-ttu-id="a6537-153">Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-153">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-154">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="a6537-154">-StorageAutogrow</span></span>
<span data-ttu-id="a6537-155">Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a6537-155">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-156">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="a6537-156">-StorageInMb</span></span>
<span data-ttu-id="a6537-157">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-157">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6537-158">-SubscriptionId</span></span>
<span data-ttu-id="a6537-159">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="a6537-159">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6537-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6537-160">-Tag</span></span>
<span data-ttu-id="a6537-161">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="a6537-161">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="a6537-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6537-162">-Confirm</span></span>
<span data-ttu-id="a6537-163">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6537-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6537-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6537-164">-WhatIf</span></span>
<span data-ttu-id="a6537-165">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6537-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6537-166">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6537-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6537-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6537-167">CommonParameters</span></span>
<span data-ttu-id="a6537-168">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6537-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6537-169">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6537-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6537-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6537-170">INPUTS</span></span>

### <span data-ttu-id="a6537-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a6537-171">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a6537-172">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a6537-172">OUTPUTS</span></span>

### <span data-ttu-id="a6537-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="a6537-173">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="a6537-174">NOTES</span><span class="sxs-lookup"><span data-stu-id="a6537-174">NOTES</span></span>

<span data-ttu-id="a6537-175">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a6537-175">ALIASES</span></span>

<span data-ttu-id="a6537-176">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a6537-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6537-177">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a6537-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6537-178">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6537-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6537-179">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="a6537-179">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="a6537-180">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-180">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a6537-181">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a6537-181">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a6537-182">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-182">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a6537-183">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a6537-183">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6537-184">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="a6537-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a6537-185">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6537-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a6537-186">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a6537-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="a6537-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="a6537-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a6537-188">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a6537-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a6537-189">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a6537-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a6537-190">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a6537-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a6537-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6537-191">RELATED LINKS</span></span>

