---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlServer.md
ms.openlocfilehash: e23cc8b942033805d8ed8cd122b19e6a59bf457c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117615"
---
# <span data-ttu-id="b2eb4-101">Update-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="b2eb4-101">Update-AzMySqlServer</span></span>

## <span data-ttu-id="b2eb4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="b2eb4-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-103">Updates an existing server.</span></span>
<span data-ttu-id="b2eb4-104">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="b2eb4-105">Use Update-AzMySqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-105">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="b2eb4-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2eb4-106">SYNTAX</span></span>

### <span data-ttu-id="b2eb4-107">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2eb4-107">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2eb4-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b2eb4-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlServer -InputObject <IMySqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2eb4-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2eb4-109">DESCRIPTION</span></span>
<span data-ttu-id="b2eb4-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-110">Updates an existing server.</span></span>
<span data-ttu-id="b2eb4-111">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="b2eb4-112">Use Update-AzMySqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-112">Use Update-AzMySqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="b2eb4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2eb4-113">EXAMPLES</span></span>

### <span data-ttu-id="b2eb4-114">Exemplo 1: atualizar o servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="b2eb4-114">Example 1: Update MySql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -SslEnforcement Disabled

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b2eb4-115">Este cmdlet atualiza o MySql Server por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-115">This cmdlet updates MySql server by resource group and server name.</span></span>

### <span data-ttu-id="b2eb4-116">Exemplo 2: Atualize o MySql Server por identidade.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-116">Example 2: Update MySql server by identity.</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Update-AzMySqlServer -BackupRetentionDay 23 -StorageMb 10240

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="b2eb4-117">Este cmdlet atualiza o MySql Server por identidade.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-117">This cmdlet updates MySql server by identity.</span></span>

## <span data-ttu-id="b2eb4-118">OS</span><span class="sxs-lookup"><span data-stu-id="b2eb4-118">PARAMETERS</span></span>

### <span data-ttu-id="b2eb4-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="b2eb4-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="b2eb4-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="b2eb4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2eb4-121">-AsJob</span></span>
<span data-ttu-id="b2eb4-122">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="b2eb4-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="b2eb4-123">-BackupRetentionDay</span></span>
<span data-ttu-id="b2eb4-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-124">Backup retention days for the server.</span></span>
<span data-ttu-id="b2eb4-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="b2eb4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2eb4-126">-DefaultProfile</span></span>
<span data-ttu-id="b2eb4-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2eb4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2eb4-128">-InputObject</span></span>
<span data-ttu-id="b2eb4-129">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-129">Identity Parameter.</span></span>
<span data-ttu-id="b2eb4-130">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2eb4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2eb4-131">-Name</span></span>
<span data-ttu-id="b2eb4-132">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-132">The name of the server.</span></span>

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

### <span data-ttu-id="b2eb4-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b2eb4-133">-NoWait</span></span>
<span data-ttu-id="b2eb4-134">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="b2eb4-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="b2eb4-135">-ReplicationRole</span></span>
<span data-ttu-id="b2eb4-136">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="b2eb4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2eb4-137">-ResourceGroupName</span></span>
<span data-ttu-id="b2eb4-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b2eb4-139">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b2eb4-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="b2eb4-140">-Sku</span></span>
<span data-ttu-id="b2eb4-141">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="b2eb4-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b2eb4-142">-SkuCapacity</span></span>
<span data-ttu-id="b2eb4-143">A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="b2eb4-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="b2eb4-144">-SkuFamily</span></span>
<span data-ttu-id="b2eb4-145">A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-145">The family of hardware.</span></span>

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

### <span data-ttu-id="b2eb4-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="b2eb4-146">-SkuTier</span></span>
<span data-ttu-id="b2eb4-147">A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="b2eb4-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="b2eb4-148">-SslEnforcement</span></span>
<span data-ttu-id="b2eb4-149">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="b2eb4-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="b2eb4-150">-StorageAutogrow</span></span>
<span data-ttu-id="b2eb4-151">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="b2eb4-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="b2eb4-152">-StorageInMb</span></span>
<span data-ttu-id="b2eb4-153">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="b2eb4-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2eb4-154">-SubscriptionId</span></span>
<span data-ttu-id="b2eb4-155">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b2eb4-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2eb4-156">-Tag</span></span>
<span data-ttu-id="b2eb4-157">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="b2eb4-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2eb4-158">-Confirm</span></span>
<span data-ttu-id="b2eb4-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2eb4-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2eb4-160">-WhatIf</span></span>
<span data-ttu-id="b2eb4-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2eb4-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2eb4-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2eb4-163">CommonParameters</span></span>
<span data-ttu-id="b2eb4-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2eb4-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2eb4-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2eb4-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2eb4-166">INPUTS</span></span>

### <span data-ttu-id="b2eb4-167">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b2eb4-167">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b2eb4-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2eb4-168">OUTPUTS</span></span>

### <span data-ttu-id="b2eb4-169">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="b2eb4-169">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="b2eb4-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2eb4-170">NOTES</span></span>

<span data-ttu-id="b2eb4-171">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b2eb4-171">ALIASES</span></span>

<span data-ttu-id="b2eb4-172">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b2eb4-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2eb4-173">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2eb4-174">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2eb4-175">INPUTobject <IMySqlIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-175">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="b2eb4-176">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b2eb4-177">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b2eb4-178">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b2eb4-179">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b2eb4-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2eb4-180">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b2eb4-181">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b2eb4-182">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="b2eb4-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b2eb4-184">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b2eb4-185">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b2eb4-186">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b2eb4-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b2eb4-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2eb4-187">RELATED LINKS</span></span>

