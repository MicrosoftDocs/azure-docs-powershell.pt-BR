---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServer.md
ms.openlocfilehash: 3e1f79f431e5f0ff5c39c03a7f3c41a20c2543e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428222"
---
# <span data-ttu-id="e192a-101">Update-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="e192a-101">Update-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="e192a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e192a-102">SYNOPSIS</span></span>
<span data-ttu-id="e192a-103">Atualiza um servidor existente flexível do MySQL.</span><span class="sxs-lookup"><span data-stu-id="e192a-103">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="e192a-104">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="e192a-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e192a-105">Use Update-AzMySqlFlexibleServerConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e192a-105">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e192a-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e192a-106">SYNTAX</span></span>

### <span data-ttu-id="e192a-107">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="e192a-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>]
 [-ReplicationRole <String>] [-Sku <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e192a-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e192a-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-HaEnabled <HaEnabledEnum>] [-ReplicationRole <String>] [-Sku <String>]
 [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>]
 [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e192a-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e192a-109">DESCRIPTION</span></span>
<span data-ttu-id="e192a-110">Atualiza um servidor existente flexível do MySQL.</span><span class="sxs-lookup"><span data-stu-id="e192a-110">Updates an existing MySQL flexible server.</span></span>
<span data-ttu-id="e192a-111">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="e192a-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="e192a-112">Use Update-AzMySqlFlexibleServerConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="e192a-112">Use Update-AzMySqlFlexibleServerConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="e192a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e192a-113">EXAMPLES</span></span>

### <span data-ttu-id="e192a-114">Exemplo 1: atualizar o servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="e192a-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test -Sku Standard_D4ds_v4

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D4ds_v4 GeneralPurpose
```

<span data-ttu-id="e192a-115">Este cmdlet atualiza o MySql Server por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="e192a-116">Exemplo 2: Atualize o MySql Server por identidade.</span><span class="sxs-lookup"><span data-stu-id="e192a-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlFlexibleServer -BackupRetentionDay 23 -StorageInMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="e192a-117">Este cmdlet atualiza o MySql Server por identidade.</span><span class="sxs-lookup"><span data-stu-id="e192a-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="e192a-118">OS</span><span class="sxs-lookup"><span data-stu-id="e192a-118">PARAMETERS</span></span>

### <span data-ttu-id="e192a-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="e192a-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="e192a-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="e192a-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="e192a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e192a-121">-AsJob</span></span>
<span data-ttu-id="e192a-122">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e192a-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="e192a-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="e192a-123">-BackupRetentionDay</span></span>
<span data-ttu-id="e192a-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-124">Backup retention days for the server.</span></span>
<span data-ttu-id="e192a-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="e192a-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="e192a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e192a-126">-DefaultProfile</span></span>
<span data-ttu-id="e192a-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e192a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e192a-128">-HaEnabled</span><span class="sxs-lookup"><span data-stu-id="e192a-128">-HaEnabled</span></span>
<span data-ttu-id="e192a-129">Habilite ou desabilite o recurso de alta disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="e192a-129">Enable or disable high availability feature.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.HaEnabledEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e192a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e192a-130">-InputObject</span></span>
<span data-ttu-id="e192a-131">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="e192a-131">Identity Parameter.</span></span>
<span data-ttu-id="e192a-132">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e192a-132">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e192a-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e192a-133">-Name</span></span>
<span data-ttu-id="e192a-134">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-134">The name of the server.</span></span>

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

### <span data-ttu-id="e192a-135">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e192a-135">-NoWait</span></span>
<span data-ttu-id="e192a-136">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="e192a-136">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="e192a-137">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="e192a-137">-ReplicationRole</span></span>
<span data-ttu-id="e192a-138">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-138">The replication role of the server.</span></span>

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

### <span data-ttu-id="e192a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e192a-139">-ResourceGroupName</span></span>
<span data-ttu-id="e192a-140">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="e192a-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e192a-141">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="e192a-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e192a-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="e192a-142">-Sku</span></span>
<span data-ttu-id="e192a-143">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="e192a-143">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="e192a-144">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e192a-144">-SkuTier</span></span>
<span data-ttu-id="e192a-145">A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="e192a-145">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="e192a-146">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="e192a-146">-SslEnforcement</span></span>
<span data-ttu-id="e192a-147">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-147">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="e192a-148">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="e192a-148">-StorageAutogrow</span></span>
<span data-ttu-id="e192a-149">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e192a-149">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="e192a-150">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="e192a-150">-StorageInMb</span></span>
<span data-ttu-id="e192a-151">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-151">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="e192a-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e192a-152">-SubscriptionId</span></span>
<span data-ttu-id="e192a-153">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e192a-153">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="e192a-154">-Marca</span><span class="sxs-lookup"><span data-stu-id="e192a-154">-Tag</span></span>
<span data-ttu-id="e192a-155">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="e192a-155">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="e192a-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e192a-156">-Confirm</span></span>
<span data-ttu-id="e192a-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e192a-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e192a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e192a-158">-WhatIf</span></span>
<span data-ttu-id="e192a-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e192a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e192a-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e192a-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e192a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e192a-161">CommonParameters</span></span>
<span data-ttu-id="e192a-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e192a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e192a-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e192a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e192a-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e192a-164">INPUTS</span></span>

### <span data-ttu-id="e192a-165">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e192a-165">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="e192a-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e192a-166">OUTPUTS</span></span>

### <span data-ttu-id="e192a-167">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e192a-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="e192a-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e192a-168">NOTES</span></span>

<span data-ttu-id="e192a-169">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e192a-169">ALIASES</span></span>

<span data-ttu-id="e192a-170">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="e192a-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e192a-171">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="e192a-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e192a-172">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e192a-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e192a-173">INPUTobject <IMySqlIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="e192a-173">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="e192a-174">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-174">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e192a-175">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e192a-175">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e192a-176">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-176">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e192a-177">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e192a-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e192a-178">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-178">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="e192a-179">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="e192a-179">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e192a-180">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e192a-180">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e192a-181">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e192a-181">The name is case insensitive.</span></span>
  - <span data-ttu-id="e192a-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="e192a-182">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e192a-183">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e192a-183">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e192a-184">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e192a-184">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e192a-185">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e192a-185">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e192a-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e192a-186">RELATED LINKS</span></span>

