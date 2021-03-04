---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0db4d25f224f1c6984ba9b57184859e8fa2c6c28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892135"
---
# <span data-ttu-id="408a3-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="408a3-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="408a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="408a3-102">SYNOPSIS</span></span>
<span data-ttu-id="408a3-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="408a3-103">Updates an existing server.</span></span>
<span data-ttu-id="408a3-104">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="408a3-105">Use Update-AzMariaDbConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="408a3-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="408a3-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="408a3-106">SYNTAX</span></span>

### <span data-ttu-id="408a3-107">ServerName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="408a3-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="408a3-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="408a3-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="408a3-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="408a3-109">DESCRIPTION</span></span>
<span data-ttu-id="408a3-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="408a3-110">Updates an existing server.</span></span>
<span data-ttu-id="408a3-111">O corpo da solicitação pode conter uma a muitas das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="408a3-112">Use Update-AzMariaDbConfiguration se quiser atualizar parâmetros de servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="408a3-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="408a3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="408a3-113">EXAMPLES</span></span>

### <span data-ttu-id="408a3-114">Exemplo 1: Atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="408a3-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="408a3-115">Este comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="408a3-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="408a3-116">Exemplo 2: Atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="408a3-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="408a3-117">Este comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="408a3-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="408a3-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="408a3-118">PARAMETERS</span></span>

### <span data-ttu-id="408a3-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="408a3-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="408a3-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="408a3-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="408a3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="408a3-121">-AsJob</span></span>
<span data-ttu-id="408a3-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="408a3-122">Run the command as a job</span></span>

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

### <span data-ttu-id="408a3-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="408a3-123">-BackupRetentionDay</span></span>
<span data-ttu-id="408a3-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="408a3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408a3-125">-DefaultProfile</span></span>
<span data-ttu-id="408a3-126">região DefaultParameters As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="408a3-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="408a3-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="408a3-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="408a3-128">Habilitar Geo-redundante ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-128">Enable Geo-redundant or not for server backup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.GeoRedundantBackup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="408a3-129">-InputObject</span></span>
<span data-ttu-id="408a3-130">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="408a3-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="408a3-131">-Name</span></span>
<span data-ttu-id="408a3-132">Nome do servidor MariaDB</span><span class="sxs-lookup"><span data-stu-id="408a3-132">MariaDB server name</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="408a3-133">-NoWait</span></span>
<span data-ttu-id="408a3-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="408a3-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="408a3-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="408a3-135">-ReplicationRole</span></span>
<span data-ttu-id="408a3-136">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="408a3-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408a3-137">-ResourceGroupName</span></span>
<span data-ttu-id="408a3-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="408a3-138">The name of the resource group that contains the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="408a3-139">-Sku</span></span>
<span data-ttu-id="408a3-140">O nome do sku, normalmente, camada + família + núcleos, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="408a3-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="408a3-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="408a3-141">-SslEnforcement</span></span>
<span data-ttu-id="408a3-142">Habilitar a imposição ssl ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-142">Enable ssl enforcement or not when connect to server.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.SslEnforcementEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="408a3-143">-StorageAutogrow</span></span>
<span data-ttu-id="408a3-144">Habilitar o Crescimento Automático de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="408a3-144">Enable Storage Auto Grow.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Support.StorageAutogrow
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="408a3-145">-StorageInMb</span></span>
<span data-ttu-id="408a3-146">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="408a3-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="408a3-147">-SubscriptionId</span></span>
<span data-ttu-id="408a3-148">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="408a3-148">The subscription ID is part of the URI for every service call</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408a3-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="408a3-149">-Tag</span></span>
<span data-ttu-id="408a3-150">Metadados específicos do aplicativo na forma de pares de valores-chave.</span><span class="sxs-lookup"><span data-stu-id="408a3-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="408a3-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="408a3-151">-Confirm</span></span>
<span data-ttu-id="408a3-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="408a3-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408a3-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408a3-153">-WhatIf</span></span>
<span data-ttu-id="408a3-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="408a3-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408a3-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="408a3-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408a3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408a3-156">CommonParameters</span></span>
<span data-ttu-id="408a3-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408a3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408a3-158">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="408a3-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408a3-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="408a3-159">INPUTS</span></span>

### <span data-ttu-id="408a3-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="408a3-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="408a3-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="408a3-161">OUTPUTS</span></span>

### <span data-ttu-id="408a3-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="408a3-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="408a3-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="408a3-163">NOTES</span></span>

<span data-ttu-id="408a3-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="408a3-164">ALIASES</span></span>

<span data-ttu-id="408a3-165">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="408a3-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="408a3-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="408a3-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="408a3-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="408a3-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="408a3-168">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="408a3-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="408a3-169">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="408a3-170">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="408a3-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="408a3-171">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="408a3-172">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="408a3-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="408a3-173">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="408a3-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="408a3-174">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="408a3-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="408a3-175">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="408a3-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="408a3-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="408a3-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="408a3-177">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="408a3-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="408a3-178">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="408a3-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="408a3-179">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="408a3-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="408a3-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="408a3-180">RELATED LINKS</span></span>

