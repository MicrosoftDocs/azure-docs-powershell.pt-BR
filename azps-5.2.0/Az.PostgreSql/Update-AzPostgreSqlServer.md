---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlServer.md
ms.openlocfilehash: ecb568a356d0f1cf5ed36d966028e2d0ca4f813a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257901"
---
# <span data-ttu-id="0b397-101">Update-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="0b397-101">Update-AzPostgreSqlServer</span></span>

## <span data-ttu-id="0b397-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b397-102">SYNOPSIS</span></span>
<span data-ttu-id="0b397-103">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="0b397-103">Updates an existing server.</span></span>
<span data-ttu-id="0b397-104">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="0b397-104">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0b397-105">Use Update-AzPostSqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0b397-105">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0b397-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b397-106">SYNTAX</span></span>

### <span data-ttu-id="0b397-107">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b397-107">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-BackupRetentionDay <Int32>] [-ReplicationRole <String>]
 [-Sku <String>] [-SkuCapacity <Int32>] [-SkuFamily <String>] [-SkuTier <SkuTier>]
 [-SslEnforcement <SslEnforcementEnum>] [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b397-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0b397-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-AdministratorLoginPassword <SecureString>]
 [-BackupRetentionDay <Int32>] [-ReplicationRole <String>] [-Sku <String>] [-SkuCapacity <Int32>]
 [-SkuFamily <String>] [-SkuTier <SkuTier>] [-SslEnforcement <SslEnforcementEnum>]
 [-StorageAutogrow <StorageAutogrow>] [-StorageInMb <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b397-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b397-109">DESCRIPTION</span></span>
<span data-ttu-id="0b397-110">Atualiza um servidor existente.</span><span class="sxs-lookup"><span data-stu-id="0b397-110">Updates an existing server.</span></span>
<span data-ttu-id="0b397-111">O corpo da solicitação pode conter uma para muitas das propriedades presentes na definição do servidor normal.</span><span class="sxs-lookup"><span data-stu-id="0b397-111">The request body can contain one to many of the properties present in the normal server definition.</span></span>
<span data-ttu-id="0b397-112">Use Update-AzPostSqlConfiguration em vez disso, se quiser atualizar parâmetros do servidor, como wait_timeout ou net_retry_count.</span><span class="sxs-lookup"><span data-stu-id="0b397-112">Use Update-AzPostSqlConfiguration instead if you want update server parameters such as wait_timeout or net_retry_count.</span></span>

## <span data-ttu-id="0b397-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b397-113">EXAMPLES</span></span>

### <span data-ttu-id="0b397-114">Exemplo 1: atualizar o servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="0b397-114">Example 1: Update PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Update-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SslEnforcement Disabled

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0b397-115">Este cmdlet atualiza o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-115">This cmdlet updates PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="0b397-116">Exemplo 2: Atualize o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0b397-116">Example 2: Update PostgreSql server by identity.</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer | Update-AzPostgreSqlServer -BackupRetentionDay 23

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0b397-117">Este cmdlet atualiza o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="0b397-117">This cmdlet updates PostgreSql server by identity.</span></span>

## <span data-ttu-id="0b397-118">OS</span><span class="sxs-lookup"><span data-stu-id="0b397-118">PARAMETERS</span></span>

### <span data-ttu-id="0b397-119">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="0b397-119">-AdministratorLoginPassword</span></span>
<span data-ttu-id="0b397-120">A senha do logon do administrador.</span><span class="sxs-lookup"><span data-stu-id="0b397-120">The password of the administrator login.</span></span>

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

### <span data-ttu-id="0b397-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b397-121">-AsJob</span></span>
<span data-ttu-id="0b397-122">Executar o comando como um trabalho.</span><span class="sxs-lookup"><span data-stu-id="0b397-122">Run the command as a job.</span></span>

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

### <span data-ttu-id="0b397-123">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="0b397-123">-BackupRetentionDay</span></span>
<span data-ttu-id="0b397-124">Dias de retenção de backup para o servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-124">Backup retention days for the server.</span></span>
<span data-ttu-id="0b397-125">A contagem de dias está entre 7 e 35.</span><span class="sxs-lookup"><span data-stu-id="0b397-125">Day count is between 7 and 35.</span></span>

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

### <span data-ttu-id="0b397-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b397-126">-DefaultProfile</span></span>
<span data-ttu-id="0b397-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0b397-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b397-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b397-128">-InputObject</span></span>
<span data-ttu-id="0b397-129">Parâmetro de identidade.</span><span class="sxs-lookup"><span data-stu-id="0b397-129">Identity Parameter.</span></span>
<span data-ttu-id="0b397-130">Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="0b397-130">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0b397-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b397-131">-Name</span></span>
<span data-ttu-id="0b397-132">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-132">The name of the server.</span></span>

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

### <span data-ttu-id="0b397-133">-Nowait</span><span class="sxs-lookup"><span data-stu-id="0b397-133">-NoWait</span></span>
<span data-ttu-id="0b397-134">Executar o comando de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0b397-134">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0b397-135">-ReplicationRole</span><span class="sxs-lookup"><span data-stu-id="0b397-135">-ReplicationRole</span></span>
<span data-ttu-id="0b397-136">A função de replicação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-136">The replication role of the server.</span></span>

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

### <span data-ttu-id="0b397-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b397-137">-ResourceGroupName</span></span>
<span data-ttu-id="0b397-138">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="0b397-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0b397-139">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="0b397-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0b397-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b397-140">-Sku</span></span>
<span data-ttu-id="0b397-141">O nome do SKU, geralmente, a camada + família + núcleos, por exemplo B_Gen4_1 GP_Gen5_8.</span><span class="sxs-lookup"><span data-stu-id="0b397-141">The name of the sku, typically, tier + family + cores, e.g. B_Gen4_1, GP_Gen5_8.</span></span>

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

### <span data-ttu-id="0b397-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="0b397-142">-SkuCapacity</span></span>
<span data-ttu-id="0b397-143">A capacidade de dimensionamento/saída, representando as unidades de computação do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-143">The scale up/out capacity, representing server's compute units.</span></span>

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

### <span data-ttu-id="0b397-144">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="0b397-144">-SkuFamily</span></span>
<span data-ttu-id="0b397-145">A família de hardware.</span><span class="sxs-lookup"><span data-stu-id="0b397-145">The family of hardware.</span></span>

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

### <span data-ttu-id="0b397-146">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="0b397-146">-SkuTier</span></span>
<span data-ttu-id="0b397-147">A camada do SKU específico, por exemplo, básico.</span><span class="sxs-lookup"><span data-stu-id="0b397-147">The tier of the particular SKU, e.g. Basic.</span></span>

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

### <span data-ttu-id="0b397-148">-SslEnforcement</span><span class="sxs-lookup"><span data-stu-id="0b397-148">-SslEnforcement</span></span>
<span data-ttu-id="0b397-149">Habilite a imposição de SSL ou não quando se conectar ao servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-149">Enable ssl enforcement or not when connect to server.</span></span>

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

### <span data-ttu-id="0b397-150">-StorageAutogrow</span><span class="sxs-lookup"><span data-stu-id="0b397-150">-StorageAutogrow</span></span>
<span data-ttu-id="0b397-151">Habilite o aumento automático do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b397-151">Enable Storage Auto Grow.</span></span>

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

### <span data-ttu-id="0b397-152">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="0b397-152">-StorageInMb</span></span>
<span data-ttu-id="0b397-153">Armazenamento máximo permitido para um servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-153">Max storage allowed for a server.</span></span>

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

### <span data-ttu-id="0b397-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b397-154">-SubscriptionId</span></span>
<span data-ttu-id="0b397-155">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b397-155">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0b397-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="0b397-156">-Tag</span></span>
<span data-ttu-id="0b397-157">Metadados específicos do aplicativo na forma de pares de valor chave.</span><span class="sxs-lookup"><span data-stu-id="0b397-157">Application-specific metadata in the form of key-value pairs.</span></span>

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

### <span data-ttu-id="0b397-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0b397-158">-Confirm</span></span>
<span data-ttu-id="0b397-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b397-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b397-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b397-160">-WhatIf</span></span>
<span data-ttu-id="0b397-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0b397-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b397-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b397-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b397-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b397-163">CommonParameters</span></span>
<span data-ttu-id="0b397-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b397-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b397-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b397-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b397-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b397-166">INPUTS</span></span>

### <span data-ttu-id="0b397-167">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0b397-167">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="0b397-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b397-168">OUTPUTS</span></span>

### <span data-ttu-id="0b397-169">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0b397-169">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0b397-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b397-170">NOTES</span></span>

<span data-ttu-id="0b397-171">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0b397-171">ALIASES</span></span>

<span data-ttu-id="0b397-172">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="0b397-172">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b397-173">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="0b397-173">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b397-174">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b397-174">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b397-175">INPUTobject <IPostgreSqlIdentity> : Parameter de identidade.</span><span class="sxs-lookup"><span data-stu-id="0b397-175">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="0b397-176">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-176">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0b397-177">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b397-177">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0b397-178">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-178">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0b397-179">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="0b397-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0b397-180">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="0b397-180">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0b397-181">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b397-181">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0b397-182">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0b397-182">The name is case insensitive.</span></span>
  - <span data-ttu-id="0b397-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="0b397-183">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0b397-184">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="0b397-184">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0b397-185">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="0b397-185">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0b397-186">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0b397-186">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0b397-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b397-187">RELATED LINKS</span></span>

