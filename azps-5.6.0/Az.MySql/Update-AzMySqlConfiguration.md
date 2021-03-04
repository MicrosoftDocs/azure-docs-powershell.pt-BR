---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlConfiguration.md
ms.openlocfilehash: bff7f24ef88c8f6fc5022aae019a9c6f32bf95f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887486"
---
# <span data-ttu-id="c50d3-101">Update-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="c50d3-101">Update-AzMySqlConfiguration</span></span>

## <span data-ttu-id="c50d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c50d3-102">SYNOPSIS</span></span>
<span data-ttu-id="c50d3-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="c50d3-104">Use Update-AzMySqlServer em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="c50d3-104">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c50d3-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c50d3-105">SYNTAX</span></span>

### <span data-ttu-id="c50d3-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c50d3-106">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c50d3-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c50d3-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c50d3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c50d3-108">DESCRIPTION</span></span>
<span data-ttu-id="c50d3-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="c50d3-110">Use Update-AzMySqlServer em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="c50d3-110">Use Update-AzMySqlServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="c50d3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c50d3-111">EXAMPLES</span></span>

### <span data-ttu-id="c50d3-112">Exemplo 1: Atualizar a configuração do MySql pelo nome</span><span class="sxs-lookup"><span data-stu-id="c50d3-112">Example 1: Update MySql configuration by name</span></span>
```powershell
PS C:\> Update-AzMySqlConfiguration -Name net_retry_count -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Value 15

Name            Value
----            -----
net_retry_count 15
```

<span data-ttu-id="c50d3-113">Este cmdlet atualiza a configuração do MySql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="c50d3-113">This cmdlet updates MySql configuration by name.</span></span>

### <span data-ttu-id="c50d3-114">Exemplo 2: atualizar a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="c50d3-114">Example 2: Update MySql configuration by identity.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/configurations/wait_timeout"
PS C:\> Update-AzMySqlConfiguration -InputObject $ID -Value 150

Name         Value
----         -----
wait_timeout 150
```

<span data-ttu-id="c50d3-115">Esses cmdlets atualizam a configuração do MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="c50d3-115">These cmdlets update MySql configuration by identity.</span></span>

## <span data-ttu-id="c50d3-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c50d3-116">PARAMETERS</span></span>

### <span data-ttu-id="c50d3-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c50d3-117">-AsJob</span></span>
<span data-ttu-id="c50d3-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c50d3-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c50d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c50d3-119">-DefaultProfile</span></span>
<span data-ttu-id="c50d3-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c50d3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c50d3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c50d3-121">-InputObject</span></span>
<span data-ttu-id="c50d3-122">Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="c50d3-122">Identity Parameter.</span></span>
<span data-ttu-id="c50d3-123">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c50d3-123">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c50d3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c50d3-124">-Name</span></span>
<span data-ttu-id="c50d3-125">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-125">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c50d3-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c50d3-126">-NoWait</span></span>
<span data-ttu-id="c50d3-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="c50d3-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c50d3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c50d3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c50d3-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c50d3-129">The name of the resource group.</span></span>
<span data-ttu-id="c50d3-130">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c50d3-130">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c50d3-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c50d3-131">-ServerName</span></span>
<span data-ttu-id="c50d3-132">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-132">The name of the server.</span></span>

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

### <span data-ttu-id="c50d3-133">-Source</span><span class="sxs-lookup"><span data-stu-id="c50d3-133">-Source</span></span>
<span data-ttu-id="c50d3-134">Origem da configuração.</span><span class="sxs-lookup"><span data-stu-id="c50d3-134">Source of the configuration.</span></span>

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

### <span data-ttu-id="c50d3-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c50d3-135">-SubscriptionId</span></span>
<span data-ttu-id="c50d3-136">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c50d3-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c50d3-137">-Value</span><span class="sxs-lookup"><span data-stu-id="c50d3-137">-Value</span></span>
<span data-ttu-id="c50d3-138">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="c50d3-138">Value of the configuration.</span></span>

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

### <span data-ttu-id="c50d3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c50d3-139">-Confirm</span></span>
<span data-ttu-id="c50d3-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c50d3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c50d3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c50d3-141">-WhatIf</span></span>
<span data-ttu-id="c50d3-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c50d3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c50d3-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c50d3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c50d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c50d3-144">CommonParameters</span></span>
<span data-ttu-id="c50d3-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c50d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c50d3-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c50d3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c50d3-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c50d3-147">INPUTS</span></span>

### <span data-ttu-id="c50d3-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c50d3-148">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c50d3-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c50d3-149">OUTPUTS</span></span>

### <span data-ttu-id="c50d3-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="c50d3-150">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="c50d3-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="c50d3-151">NOTES</span></span>

<span data-ttu-id="c50d3-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c50d3-152">ALIASES</span></span>

<span data-ttu-id="c50d3-153">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="c50d3-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c50d3-154">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="c50d3-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c50d3-155">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c50d3-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c50d3-156">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity.</span><span class="sxs-lookup"><span data-stu-id="c50d3-156">INPUTOBJECT <IMySqlIdentity>: Identity Parameter.</span></span>
  - <span data-ttu-id="c50d3-157">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-157">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c50d3-158">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c50d3-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c50d3-159">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-159">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c50d3-160">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c50d3-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c50d3-161">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-161">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c50d3-162">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="c50d3-162">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c50d3-163">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c50d3-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c50d3-164">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c50d3-164">The name is case insensitive.</span></span>
  - <span data-ttu-id="c50d3-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="c50d3-165">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c50d3-166">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c50d3-166">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c50d3-167">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c50d3-167">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c50d3-168">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c50d3-168">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c50d3-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c50d3-169">RELATED LINKS</span></span>

