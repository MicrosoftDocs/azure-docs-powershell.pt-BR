---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115254"
---
# <span data-ttu-id="d8618-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="d8618-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="d8618-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8618-102">SYNOPSIS</span></span>
<span data-ttu-id="d8618-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="d8618-103">Updates an existing server.</span></span>
<span data-ttu-id="d8618-104">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d8618-105">Use Update-AzMariaDbConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d8618-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d8618-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8618-106">SYNTAX</span></span>

### <span data-ttu-id="d8618-107">Nomedo Servidor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8618-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d8618-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="d8618-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8618-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8618-109">DESCRIPTION</span></span>
<span data-ttu-id="d8618-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="d8618-110">Updates an existing server.</span></span>
<span data-ttu-id="d8618-111">O corpo da solicitação pode conter de uma a várias das propriedades presentes na definição normal do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="d8618-112">Use Update-AzMariaDbConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="d8618-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="d8618-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d8618-113">EXAMPLES</span></span>

### <span data-ttu-id="d8618-114">Exemplo 1: Atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="d8618-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="d8618-115">Este comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d8618-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="d8618-116">Exemplo 2: Atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="d8618-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="d8618-117">Este comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="d8618-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="d8618-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8618-118">PARAMETERS</span></span>

### <span data-ttu-id="d8618-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="d8618-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="d8618-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="d8618-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="d8618-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8618-121">-AsJob</span></span>
<span data-ttu-id="d8618-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d8618-122">Run the command as a job</span></span>

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

### <span data-ttu-id="d8618-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="d8618-123">-BackupRetentionDay</span></span>
<span data-ttu-id="d8618-124">Backup de dias de retenção para o servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="d8618-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8618-125">-DefaultProfile</span></span>
<span data-ttu-id="d8618-126">região DefaultParameters As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8618-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8618-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="d8618-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="d8618-128">Habilitar a redundância geográfica ou não para backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="d8618-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8618-129">-InputObject</span></span>
<span data-ttu-id="d8618-130">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d8618-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8618-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8618-131">-Name</span></span>
<span data-ttu-id="d8618-132">Nome do servidor MariaDB</span><span class="sxs-lookup"><span data-stu-id="d8618-132">MariaDB server name</span></span>

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

### <span data-ttu-id="d8618-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8618-133">-NoWait</span></span>
<span data-ttu-id="d8618-134">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="d8618-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8618-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="d8618-135">-ReplicationRole</span></span>
<span data-ttu-id="d8618-136">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="d8618-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8618-137">-ResourceGroupName</span></span>
<span data-ttu-id="d8618-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8618-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="d8618-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="d8618-139">-Sku</span></span>
<span data-ttu-id="d8618-140">O nome da sKU, normalmente, tier + família + cores, por exemplo, B_Gen4_1, GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="d8618-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="d8618-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="d8618-141">-SslEnforcement</span></span>
<span data-ttu-id="d8618-142">Habilita a imposição ssl ou não quando se conecta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="d8618-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="d8618-143">-StorageAutogrow</span></span>
<span data-ttu-id="d8618-144">Habilitar o Crescimento Automático do Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d8618-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="d8618-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="d8618-145">-StorageInMb</span></span>
<span data-ttu-id="d8618-146">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="d8618-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8618-147">-SubscriptionId</span></span>
<span data-ttu-id="d8618-148">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="d8618-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="d8618-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="d8618-149">-Tag</span></span>
<span data-ttu-id="d8618-150">Metadados específicos do aplicativo na forma de pares de valor-chave.</span><span class="sxs-lookup"><span data-stu-id="d8618-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="d8618-151">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d8618-151">-Confirm</span></span>
<span data-ttu-id="d8618-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8618-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8618-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8618-153">-WhatIf</span></span>
<span data-ttu-id="d8618-154">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d8618-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8618-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8618-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8618-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8618-156">CommonParameters</span></span>
<span data-ttu-id="d8618-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8618-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8618-158">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8618-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8618-159">Entradas</span><span class="sxs-lookup"><span data-stu-id="d8618-159">INPUTS</span></span>

### <span data-ttu-id="d8618-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="d8618-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="d8618-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="d8618-161">OUTPUTS</span></span>

### <span data-ttu-id="d8618-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="d8618-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="d8618-163">Notas</span><span class="sxs-lookup"><span data-stu-id="d8618-163">NOTES</span></span>

<span data-ttu-id="d8618-164">Aliases</span><span class="sxs-lookup"><span data-stu-id="d8618-164">ALIASES</span></span>

<span data-ttu-id="d8618-165">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d8618-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8618-166">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d8618-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8618-167">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8618-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8618-168">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="d8618-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8618-169">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d8618-170">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d8618-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d8618-171">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d8618-172">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d8618-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8618-173">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="d8618-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d8618-174">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8618-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8618-175">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d8618-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8618-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d8618-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d8618-177">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d8618-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d8618-178">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8618-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="d8618-179">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d8618-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d8618-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8618-180">RELATED LINKS</span></span>

