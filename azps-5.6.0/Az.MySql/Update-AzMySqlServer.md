---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: 46408fc5cd6f718f26c4f55eb7f8bab56891d8b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887480"
---
# <span data-ttu-id="09a65-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="09a65-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="09a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09a65-102">SYNOPSIS</span></span>
<span data-ttu-id="09a65-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="09a65-103">Updates an existing server.</span></span>
<span data-ttu-id="09a65-104">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="09a65-105">Use Update-AzMySqlConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="09a65-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="09a65-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09a65-106">SYNTAX</span></span>

### <span data-ttu-id="09a65-107">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09a65-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="09a65-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="09a65-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-MinimalTlsVersion <MinimalTlsVersionEnum>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09a65-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09a65-109">DESCRIPTION</span></span>
<span data-ttu-id="09a65-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="09a65-110">Updates an existing server.</span></span>
<span data-ttu-id="09a65-111">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="09a65-112">Use Update-AzMySqlConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="09a65-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="09a65-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09a65-113">EXAMPLES</span></span>

### <span data-ttu-id="09a65-114">Exemplo 1: Atualizar servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="09a65-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="09a65-115">Este cmdlet atualiza o servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="09a65-116">Exemplo 2: Atualizar servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="09a65-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="09a65-117">Este cmdlet atualiza o servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="09a65-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="09a65-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09a65-118">PARAMETERS</span></span>

### <span data-ttu-id="09a65-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="09a65-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="09a65-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="09a65-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="09a65-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09a65-121">-AsJob</span></span>
<span data-ttu-id="09a65-122">Execute o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="09a65-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="09a65-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="09a65-123">-BackupRetentionDay</span></span>
<span data-ttu-id="09a65-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-124">Backup retention days for the server.</span></span>
<span data-ttu-id="09a65-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="09a65-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="09a65-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09a65-126">-DefaultProfile</span></span>
<span data-ttu-id="09a65-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09a65-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09a65-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09a65-128">-InputObject</span></span>
<span data-ttu-id="09a65-129">Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="09a65-129">Identity Parameter.</span></span>
<span data-ttu-id="09a65-130">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="09a65-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09a65-131">-MinimalTlsVersion</span><span class="sxs-lookup"><span data-stu-id="09a65-131">-MinimalTlsVersion</span></span>
<span data-ttu-id="09a65-132">Defina a versão TLS mínima para conexões com o servidor quando o SSL estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="09a65-132">Set the minimal TLS version for connections to server when SSL is enabled.</span></span>
<span data-ttu-id="09a65-133">O padrão é TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span><span class="sxs-lookup"><span data-stu-id="09a65-133">Default is TLSEnforcementDisabled.accepted values: TLS1_0, TLS1_1, TLS1_2, TLSEnforcementDisabled.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.MinimalTlsVersionEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a65-134">-Name</span><span class="sxs-lookup"><span data-stu-id="09a65-134">-Name</span></span>
<span data-ttu-id="09a65-135">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-135">The name of the server.</span></span>

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

### <span data-ttu-id="09a65-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09a65-136">-NoWait</span></span>
<span data-ttu-id="09a65-137">Execute o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="09a65-137">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="09a65-138">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="09a65-138">-ReplicationRole</span></span>
<span data-ttu-id="09a65-139">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-139">The replication role of the server.</span></span>

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

### <span data-ttu-id="09a65-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09a65-140">-ResourceGroupName</span></span>
<span data-ttu-id="09a65-141">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="09a65-141">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="09a65-142">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="09a65-142">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="09a65-143">-Sku</span><span class="sxs-lookup"><span data-stu-id="09a65-143">-Sku</span></span>
<span data-ttu-id="09a65-144">O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="09a65-144">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="09a65-145">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="09a65-145">-SkuCapacity</span></span>
<span data-ttu-id="09a65-146">A capacidade de dimensionar/sair, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-146">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="09a65-147">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="09a65-147">-SkuFamily</span></span>
<span data-ttu-id="09a65-148">A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="09a65-148">The family of hardware.</span></span>

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

### <span data-ttu-id="09a65-149">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="09a65-149">-SkuTier</span></span>
<span data-ttu-id="09a65-150">A camada da SKU específica, por exemplo, Basic.</span><span class="sxs-lookup"><span data-stu-id="09a65-150">The tier of the particular SKU, e.g. Basic.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a65-151">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="09a65-151">-SslEnforcement</span></span>
<span data-ttu-id="09a65-152">Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-152">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a65-153">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="09a65-153">-StorageAutogrow</span></span>
<span data-ttu-id="09a65-154">Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="09a65-154">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09a65-155">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="09a65-155">-StorageInMb</span></span>
<span data-ttu-id="09a65-156">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-156">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="09a65-157">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09a65-157">-SubscriptionId</span></span>
<span data-ttu-id="09a65-158">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="09a65-158">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="09a65-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="09a65-159">-Tag</span></span>
<span data-ttu-id="09a65-160">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="09a65-160">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="09a65-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09a65-161">-Confirm</span></span>
<span data-ttu-id="09a65-162">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09a65-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09a65-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09a65-163">-WhatIf</span></span>
<span data-ttu-id="09a65-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09a65-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09a65-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09a65-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09a65-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09a65-166">CommonParameters</span></span>
<span data-ttu-id="09a65-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09a65-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09a65-168">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09a65-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09a65-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09a65-169">INPUTS</span></span>

### <span data-ttu-id="09a65-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="09a65-170">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="09a65-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09a65-171">OUTPUTS</span></span>

### <span data-ttu-id="09a65-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="09a65-172">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="09a65-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="09a65-173">NOTES</span></span>

<span data-ttu-id="09a65-174">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09a65-174">ALIASES</span></span>

<span data-ttu-id="09a65-175">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="09a65-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="09a65-176">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="09a65-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="09a65-177">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="09a65-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="09a65-178">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="09a65-178">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="09a65-179">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-179">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="09a65-180">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="09a65-180">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="09a65-181">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-181">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="09a65-182">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="09a65-182">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="09a65-183">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-183">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="09a65-184">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="09a65-184">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="09a65-185">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09a65-185">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="09a65-186">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="09a65-186">The name is case insensitive.</span></span>
  - <span data-ttu-id="09a65-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="09a65-187">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="09a65-188">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="09a65-188">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="09a65-189">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="09a65-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="09a65-190">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="09a65-190">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="09a65-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09a65-191">RELATED LINKS</span></span>

