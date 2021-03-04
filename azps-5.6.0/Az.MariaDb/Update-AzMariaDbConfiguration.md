---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: dc2a36a9ac8c2595ef2f60b8edc40582ad864ff8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892138"
---
# <span data-ttu-id="eeabd-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeabd-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="eeabd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeabd-102">SYNOPSIS</span></span>
<span data-ttu-id="eeabd-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="eeabd-104">Use Update-AzMariaDbServer em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="eeabd-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="eeabd-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eeabd-105">SYNTAX</span></span>

### <span data-ttu-id="eeabd-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eeabd-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eeabd-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eeabd-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eeabd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eeabd-108">DESCRIPTION</span></span>
<span data-ttu-id="eeabd-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="eeabd-110">Use Update-AzMariaDberver em vez disso, se quiser atualizar AdministratorLoginPassword, sku, etc.</span><span class="sxs-lookup"><span data-stu-id="eeabd-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="eeabd-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eeabd-111">EXAMPLES</span></span>

### <span data-ttu-id="eeabd-112">Exemplo 1: Atualizar configuração do MariaDB</span><span class="sxs-lookup"><span data-stu-id="eeabd-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="eeabd-113">Este comando atualiza uma configuração de MariaDB.</span><span class="sxs-lookup"><span data-stu-id="eeabd-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="eeabd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eeabd-114">PARAMETERS</span></span>

### <span data-ttu-id="eeabd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eeabd-115">-AsJob</span></span>
<span data-ttu-id="eeabd-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="eeabd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="eeabd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeabd-117">-DefaultProfile</span></span>
<span data-ttu-id="eeabd-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eeabd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeabd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeabd-119">-InputObject</span></span>
<span data-ttu-id="eeabd-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="eeabd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeabd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="eeabd-121">-Name</span></span>
<span data-ttu-id="eeabd-122">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="eeabd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="eeabd-123">-NoWait</span></span>
<span data-ttu-id="eeabd-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="eeabd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eeabd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeabd-125">-ResourceGroupName</span></span>
<span data-ttu-id="eeabd-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="eeabd-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="eeabd-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="eeabd-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="eeabd-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eeabd-128">-ServerName</span></span>
<span data-ttu-id="eeabd-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-129">The name of the server.</span></span>

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

### <span data-ttu-id="eeabd-130">-Source</span><span class="sxs-lookup"><span data-stu-id="eeabd-130">-Source</span></span>
<span data-ttu-id="eeabd-131">Origem da configuração.</span><span class="sxs-lookup"><span data-stu-id="eeabd-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="eeabd-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eeabd-132">-SubscriptionId</span></span>
<span data-ttu-id="eeabd-133">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="eeabd-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="eeabd-134">-Value</span><span class="sxs-lookup"><span data-stu-id="eeabd-134">-Value</span></span>
<span data-ttu-id="eeabd-135">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="eeabd-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="eeabd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eeabd-136">-Confirm</span></span>
<span data-ttu-id="eeabd-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeabd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeabd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeabd-138">-WhatIf</span></span>
<span data-ttu-id="eeabd-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="eeabd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeabd-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eeabd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeabd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeabd-141">CommonParameters</span></span>
<span data-ttu-id="eeabd-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeabd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeabd-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eeabd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeabd-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeabd-144">INPUTS</span></span>

### <span data-ttu-id="eeabd-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="eeabd-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="eeabd-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eeabd-146">OUTPUTS</span></span>

### <span data-ttu-id="eeabd-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="eeabd-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="eeabd-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="eeabd-148">NOTES</span></span>

<span data-ttu-id="eeabd-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="eeabd-149">ALIASES</span></span>

<span data-ttu-id="eeabd-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="eeabd-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eeabd-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="eeabd-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eeabd-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eeabd-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eeabd-153">INPUTOBJECT <IMariaDbIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="eeabd-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eeabd-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="eeabd-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="eeabd-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="eeabd-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="eeabd-157">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="eeabd-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eeabd-158">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="eeabd-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="eeabd-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="eeabd-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="eeabd-160">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="eeabd-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="eeabd-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="eeabd-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="eeabd-162">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="eeabd-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="eeabd-163">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="eeabd-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="eeabd-164">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="eeabd-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="eeabd-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eeabd-165">RELATED LINKS</span></span>

