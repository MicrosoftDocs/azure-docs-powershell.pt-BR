---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: 4b0d2f01336de83acbd904e08b0d0cbc62c0aca6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117261"
---
# <span data-ttu-id="92c14-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="92c14-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="92c14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92c14-102">SYNOPSIS</span></span>
<span data-ttu-id="92c14-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="92c14-103">Updates an existing server.</span></span>
<span data-ttu-id="92c14-104">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="92c14-105">Use Update-AzPostSqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="92c14-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="92c14-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92c14-106">SYNTAX</span></span>

### <span data-ttu-id="92c14-107">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="92c14-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92c14-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="92c14-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92c14-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="92c14-109">DESCRIPTION</span></span>
<span data-ttu-id="92c14-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="92c14-110">Updates an existing server.</span></span>
<span data-ttu-id="92c14-111">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="92c14-112">Use Update-AzPostSqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="92c14-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="92c14-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92c14-113">EXAMPLES</span></span>

### <span data-ttu-id="92c14-114">Exemplo 1: Atualizar o servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="92c14-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="92c14-115">Este cmdlet atualiza o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="92c14-116">Exemplo 2: Atualizar o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="92c14-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="92c14-117">Este cmdlet atualiza o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="92c14-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="92c14-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92c14-118">PARAMETERS</span></span>

### <span data-ttu-id="92c14-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="92c14-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="92c14-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="92c14-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="92c14-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92c14-121">-AsJob</span></span>
<span data-ttu-id="92c14-122">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="92c14-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="92c14-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="92c14-123">-BackupRetentionDay</span></span>
<span data-ttu-id="92c14-124">Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-124">Backup retention days for the server.</span></span>
<span data-ttu-id="92c14-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="92c14-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="92c14-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92c14-126">-DefaultProfile</span></span>
<span data-ttu-id="92c14-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92c14-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92c14-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92c14-128">-InputObject</span></span>
<span data-ttu-id="92c14-129">Parâmetro de Identidade.</span><span class="sxs-lookup"><span data-stu-id="92c14-129">Identity Parameter.</span></span>
<span data-ttu-id="92c14-130">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="92c14-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92c14-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="92c14-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="92c14-132">Defina a versão TLS mínima para conexões com o servidor quando a SSL estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="92c14-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="92c14-133">O padrão é valores TLSEnforcementDisabled.accepted: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="92c14-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92c14-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="92c14-134">-Name</span></span>
<span data-ttu-id="92c14-135">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-135">The name of the server.</span></span>

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

### <span data-ttu-id="92c14-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="92c14-136">-NoWait</span></span>
<span data-ttu-id="92c14-137">Execute o comando assíncrona.</span><span class="sxs-lookup"><span data-stu-id="92c14-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="92c14-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="92c14-138">-ReplicationRole</span></span>
<span data-ttu-id="92c14-139">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="92c14-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92c14-140">-ResourceGroupName</span></span>
<span data-ttu-id="92c14-141">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="92c14-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="92c14-142">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="92c14-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="92c14-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="92c14-143">-Sku</span></span>
<span data-ttu-id="92c14-144">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="92c14-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="92c14-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="92c14-145">-SkuCapacity</span></span>
<span data-ttu-id="92c14-146">A capacidade de escala para cima/para fora, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="92c14-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="92c14-147">-SkuFamily</span></span>
<span data-ttu-id="92c14-148">A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="92c14-148">The family of hardware.</span></span>

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

### <span data-ttu-id="92c14-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="92c14-149">-SkuTier</span></span>
<span data-ttu-id="92c14-150">O nível da SKU específica, por exemplo, Básico.</span><span class="sxs-lookup"><span data-stu-id="92c14-150">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="92c14-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="92c14-151">-SslEnforcement</span></span>
<span data-ttu-id="92c14-152">Habilita a imposição ssl ou não quando se conecta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-152">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="92c14-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="92c14-153">-StorageAutogrow</span></span>
<span data-ttu-id="92c14-154">Habilitar o Crescimento Automático do Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="92c14-154">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="92c14-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="92c14-155">-StorageInMb</span></span>
<span data-ttu-id="92c14-156">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="92c14-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92c14-157">-SubscriptionId</span></span>
<span data-ttu-id="92c14-158">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="92c14-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="92c14-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="92c14-159">-Tag</span></span>
<span data-ttu-id="92c14-160">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="92c14-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="92c14-161">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="92c14-161">-Confirm</span></span>
<span data-ttu-id="92c14-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92c14-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92c14-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92c14-163">-WhatIf</span></span>
<span data-ttu-id="92c14-164">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="92c14-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92c14-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92c14-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92c14-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92c14-166">CommonParameters</span></span>
<span data-ttu-id="92c14-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92c14-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92c14-168">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92c14-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92c14-169">Entradas</span><span class="sxs-lookup"><span data-stu-id="92c14-169">INPUTS</span></span>

### <span data-ttu-id="92c14-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="92c14-170">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="92c14-171">Saídas</span><span class="sxs-lookup"><span data-stu-id="92c14-171">OUTPUTS</span></span>

### <span data-ttu-id="92c14-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="92c14-172">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="92c14-173">Notas</span><span class="sxs-lookup"><span data-stu-id="92c14-173">NOTES</span></span>

<span data-ttu-id="92c14-174">Aliases</span><span class="sxs-lookup"><span data-stu-id="92c14-174">ALIASES</span></span>

<span data-ttu-id="92c14-175">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="92c14-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92c14-176">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="92c14-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92c14-177">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92c14-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92c14-178">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade.</span><span class="sxs-lookup"><span data-stu-id="92c14-178">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="92c14-179">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="92c14-180">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="92c14-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="92c14-181">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="92c14-182">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="92c14-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92c14-183">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="92c14-183">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="92c14-184">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92c14-184">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92c14-185">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="92c14-185">The name is case insensitive.</span></span>
  - <span data-ttu-id="92c14-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="92c14-186">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="92c14-187">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="92c14-187">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="92c14-188">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="92c14-188">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92c14-189">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="92c14-189">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="92c14-190">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92c14-190">RELATED LINKS</span></span>

