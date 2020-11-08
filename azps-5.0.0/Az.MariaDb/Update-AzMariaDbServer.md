---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbServer.md
ms.openlocfilehash: 0a6286c7574a2bf7226f8d4b80a5cac62c535a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126032"
---
# <span data-ttu-id="39b33-101">Update-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="39b33-101">Update-AzMariaDbServer</span></span>

## <span data-ttu-id="39b33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39b33-102">SYNOPSIS</span></span>
<span data-ttu-id="39b33-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="39b33-103">Updates an existing server.</span></span>
<span data-ttu-id="39b33-104">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="39b33-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="39b33-105">Use Update-AzMariaDbConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="39b33-105">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="39b33-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39b33-106">SYNTAX</span></span>

### <span data-ttu-id="39b33-107">ServerName (padrão)</span><span class="sxs-lookup"><span data-stu-id="39b33-107">ServerName (Default)</span></span>
```
Update-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>]
 [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>] [-Sku <String>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="39b33-108">ServerObject</span><span class="sxs-lookup"><span data-stu-id="39b33-108">ServerObject</span></span>
```
Update-AzMariaDbServer -InputObject <IMariaDbIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-GeoRedundantBackup <GeoRedundantBackup>] [-ReplicationRole <String>]
 [-Sku <String>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="39b33-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39b33-109">DESCRIPTION</span></span>
<span data-ttu-id="39b33-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="39b33-110">Updates an existing server.</span></span>
<span data-ttu-id="39b33-111">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="39b33-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="39b33-112">Use Update-AzMariaDbConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="39b33-112">Use Update-AzMariaDbConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="39b33-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39b33-113">EXAMPLES</span></span>

### <span data-ttu-id="39b33-114">Exemplo 1: atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="39b33-114">Example 1: Update MariaDB</span></span>
```powershell
PS C:\> Update-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 -StorageInMb 8192

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    8192                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="39b33-115">Esse comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="39b33-115">This command updates a MariaDB.</span></span>

### <span data-ttu-id="39b33-116">Exemplo 2: atualizar MariaDB</span><span class="sxs-lookup"><span data-stu-id="39b33-116">Example 2: Update MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-4rmtig -ResourceGroupName mariadb-test-qu5ov0 | Update-AzMariaDbServer -StorageInMb (8192+1024)

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-4rmtig eastus   xofavpndqj         10.2    9216                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="39b33-117">Esse comando atualiza um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="39b33-117">This command updates a MariaDB.</span></span>

## <span data-ttu-id="39b33-118">OS</span><span class="sxs-lookup"><span data-stu-id="39b33-118">PARAMETERS</span></span>

### <span data-ttu-id="39b33-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="39b33-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="39b33-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="39b33-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="39b33-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39b33-121">-AsJob</span></span>
<span data-ttu-id="39b33-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="39b33-122">Run the command as a job</span></span>

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

### <span data-ttu-id="39b33-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="39b33-123">-BackupRetentionDay</span></span>
<span data-ttu-id="39b33-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-124">Backup retention days for the server.</span></span>

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

### <span data-ttu-id="39b33-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b33-125">-DefaultProfile</span></span>
<span data-ttu-id="39b33-126">Region Defaultparameters as credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39b33-126">region DefaultParameters The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39b33-127">-GeoRedundantBackup</span><span class="sxs-lookup"><span data-stu-id="39b33-127">-GeoRedundantBackup</span></span>
<span data-ttu-id="39b33-128">Habilite a redundância geográfica ou não para o backup do servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-128">Enable Geo-redundant or not for server backup.</span></span>

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

### <span data-ttu-id="39b33-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39b33-129">-InputObject</span></span>
<span data-ttu-id="39b33-130">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="39b33-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="39b33-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="39b33-131">-Name</span></span>
<span data-ttu-id="39b33-132">Nome do servidor MariaDB</span><span class="sxs-lookup"><span data-stu-id="39b33-132">MariaDB server name</span></span>

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

### <span data-ttu-id="39b33-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="39b33-133">-NoWait</span></span>
<span data-ttu-id="39b33-134">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="39b33-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="39b33-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="39b33-135">-ReplicationRole</span></span>
<span data-ttu-id="39b33-136">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="39b33-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b33-137">-ResourceGroupName</span></span>
<span data-ttu-id="39b33-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="39b33-138">The name of the resource group that contains the resource.</span></span>

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

### <span data-ttu-id="39b33-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="39b33-139">-Sku</span></span>
<span data-ttu-id="39b33-140">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="39b33-140">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="39b33-141">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="39b33-141">-SslEnforcement</span></span>
<span data-ttu-id="39b33-142">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-142">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="39b33-143">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="39b33-143">-StorageAutogrow</span></span>
<span data-ttu-id="39b33-144">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="39b33-144">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="39b33-145">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="39b33-145">-StorageInMb</span></span>
<span data-ttu-id="39b33-146">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-146">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="39b33-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="39b33-147">-SubscriptionId</span></span>
<span data-ttu-id="39b33-148">A ID da assinatura faz parte do URI para cada chamada de serviço</span><span class="sxs-lookup"><span data-stu-id="39b33-148">The subscription ID is part of the URI for every service call</span></span>

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

### <span data-ttu-id="39b33-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="39b33-149">-Tag</span></span>
<span data-ttu-id="39b33-150">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="39b33-150">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="39b33-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="39b33-151">-Confirm</span></span>
<span data-ttu-id="39b33-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39b33-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39b33-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39b33-153">-WhatIf</span></span>
<span data-ttu-id="39b33-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39b33-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39b33-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39b33-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39b33-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b33-156">CommonParameters</span></span>
<span data-ttu-id="39b33-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b33-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b33-158">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39b33-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b33-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39b33-159">INPUTS</span></span>

### <span data-ttu-id="39b33-160">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="39b33-160">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="39b33-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39b33-161">OUTPUTS</span></span>

### <span data-ttu-id="39b33-162">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="39b33-162">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="39b33-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39b33-163">NOTES</span></span>

<span data-ttu-id="39b33-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="39b33-164">ALIASES</span></span>

<span data-ttu-id="39b33-165">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="39b33-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="39b33-166">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="39b33-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="39b33-167">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="39b33-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="39b33-168">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="39b33-168">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="39b33-169">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-169">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="39b33-170">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="39b33-170">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="39b33-171">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-171">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="39b33-172">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="39b33-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="39b33-173">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="39b33-173">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="39b33-174">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="39b33-174">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="39b33-175">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="39b33-175">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="39b33-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="39b33-176">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="39b33-177">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="39b33-177">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="39b33-178">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="39b33-178">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="39b33-179">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="39b33-179">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="39b33-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39b33-180">RELATED LINKS</span></span>

