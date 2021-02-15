---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: f6634f83e89abe4c775779c052ad9ee7b21bea6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112717"
---
# <span data-ttu-id="5aeda-101">Update-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5aeda-101">Update-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="5aeda-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5aeda-102">SYNOPSIS</span></span>
<span data-ttu-id="5aeda-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="5aeda-103">Updates an existing server.</span></span>
<span data-ttu-id="5aeda-104">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5aeda-105">Use Update-AzPostSqlFlexibleServerConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5aeda-105">Use Update-AzPostSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5aeda-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5aeda-106">SYNTAX</span></span>

### <span data-ttu-id="5aeda-107">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5aeda-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5aeda-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5aeda-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity>
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5aeda-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5aeda-109">DESCRIPTION</span></span>
<span data-ttu-id="5aeda-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="5aeda-110">Updates an existing server.</span></span>
<span data-ttu-id="5aeda-111">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="5aeda-112">Use Update-AzPostgreSqlFlexibleServerConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="5aeda-112">Use Update-AzPostgreSqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="5aeda-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5aeda-113">EXAMPLES</span></span>

### <span data-ttu-id="5aeda-114">Exemplo 1: Atualizar o servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="5aeda-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -Sku Standard_D4s_v3

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus postgresql_test     12     131072                  Standard_D4s_v3 GeneralPurpose
```

<span data-ttu-id="5aeda-115">Este cmdlet atualiza o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="5aeda-116">Exemplo 2: Atualizar o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="5aeda-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Update-AzPostgreSqlFlexibleServer -BackupRetentionDay 23 -StorageMb 10240

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql_test     12     131072                  Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="5aeda-117">Este cmdlet atualiza o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="5aeda-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="5aeda-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5aeda-118">PARAMETERS</span></span>

### <span data-ttu-id="5aeda-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5aeda-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5aeda-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="5aeda-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="5aeda-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aeda-121">-AsJob</span></span>
<span data-ttu-id="5aeda-122">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="5aeda-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="5aeda-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5aeda-123">-BackupRetentionDay</span></span>
<span data-ttu-id="5aeda-124">Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-124">Backup retention days for the server.</span></span>
<span data-ttu-id="5aeda-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="5aeda-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="5aeda-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aeda-126">-DefaultProfile</span></span>
<span data-ttu-id="5aeda-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5aeda-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aeda-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="5aeda-128">-HaEnabled</span></span>
<span data-ttu-id="5aeda-129">Habilitar ou desabilitar o recurso de alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="5aeda-129">Enable or disable high availability feature.</span></span>

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

### <span data-ttu-id="5aeda-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aeda-130">-InputObject</span></span>
<span data-ttu-id="5aeda-131">Parâmetro de Identidade.</span><span class="sxs-lookup"><span data-stu-id="5aeda-131">Identity Parameter.</span></span>
<span data-ttu-id="5aeda-132">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="5aeda-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5aeda-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="5aeda-133">-Name</span></span>
<span data-ttu-id="5aeda-134">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-134">The name of the server.</span></span>

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

### <span data-ttu-id="5aeda-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5aeda-135">-NoWait</span></span>
<span data-ttu-id="5aeda-136">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5aeda-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="5aeda-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="5aeda-137">-ReplicationRole</span></span>
<span data-ttu-id="5aeda-138">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="5aeda-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aeda-139">-ResourceGroupName</span></span>
<span data-ttu-id="5aeda-140">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="5aeda-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5aeda-141">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="5aeda-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5aeda-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="5aeda-142">-Sku</span></span>
<span data-ttu-id="5aeda-143">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="5aeda-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="5aeda-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5aeda-144">-SkuTier</span></span>
<span data-ttu-id="5aeda-145">O nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="5aeda-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="5aeda-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="5aeda-146">-SslEnforcement</span></span>
<span data-ttu-id="5aeda-147">Habilita a imposição ssl ou não quando se conecta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="5aeda-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="5aeda-148">-StorageAutogrow</span></span>
<span data-ttu-id="5aeda-149">Habilitar o Crescimento Automático do Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5aeda-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="5aeda-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5aeda-150">-StorageInMb</span></span>
<span data-ttu-id="5aeda-151">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="5aeda-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5aeda-152">-SubscriptionId</span></span>
<span data-ttu-id="5aeda-153">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="5aeda-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5aeda-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="5aeda-154">-Tag</span></span>
<span data-ttu-id="5aeda-155">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="5aeda-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="5aeda-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5aeda-156">-Confirm</span></span>
<span data-ttu-id="5aeda-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aeda-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aeda-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aeda-158">-WhatIf</span></span>
<span data-ttu-id="5aeda-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5aeda-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aeda-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5aeda-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aeda-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aeda-161">CommonParameters</span></span>
<span data-ttu-id="5aeda-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aeda-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aeda-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5aeda-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aeda-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="5aeda-164">INPUTS</span></span>

### <span data-ttu-id="5aeda-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5aeda-165">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="5aeda-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="5aeda-166">OUTPUTS</span></span>

### <span data-ttu-id="5aeda-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5aeda-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5aeda-168">Notas</span><span class="sxs-lookup"><span data-stu-id="5aeda-168">NOTES</span></span>

<span data-ttu-id="5aeda-169">Aliases</span><span class="sxs-lookup"><span data-stu-id="5aeda-169">ALIASES</span></span>

<span data-ttu-id="5aeda-170">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="5aeda-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5aeda-171">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5aeda-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5aeda-172">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5aeda-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5aeda-173">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade.</span><span class="sxs-lookup"><span data-stu-id="5aeda-173">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="5aeda-174">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5aeda-175">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5aeda-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5aeda-176">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5aeda-177">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="5aeda-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5aeda-178">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="5aeda-178">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5aeda-179">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5aeda-179">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5aeda-180">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5aeda-180">The name is case insensitive.</span></span>
  - <span data-ttu-id="5aeda-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="5aeda-181">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5aeda-182">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5aeda-182">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5aeda-183">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5aeda-183">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5aeda-184">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5aeda-184">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5aeda-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5aeda-185">RELATED LINKS</span></span>

