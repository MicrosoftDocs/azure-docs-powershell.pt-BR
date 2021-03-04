---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 7d356bc977ce02d998230ad755f43479e09f0a66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887483"
---
# <span data-ttu-id="71ef5-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="71ef5-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="71ef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="71ef5-103">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="71ef5-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="71ef5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71ef5-104">SYNTAX</span></span>

### <span data-ttu-id="71ef5-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71ef5-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71ef5-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="71ef5-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71ef5-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71ef5-107">DESCRIPTION</span></span>
<span data-ttu-id="71ef5-108">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="71ef5-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="71ef5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71ef5-109">EXAMPLES</span></span>

### <span data-ttu-id="71ef5-110">Exemplo 1: Atualizar um banco de dados de servidor MySql pelo nome</span><span class="sxs-lookup"><span data-stu-id="71ef5-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="71ef5-111">Atualize um banco de dados pelo nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="71ef5-111">Update a database by resource name.</span></span>

### <span data-ttu-id="71ef5-112">Exemplo 2: Atualizar o banco de dados MySql por parâmetro.</span><span class="sxs-lookup"><span data-stu-id="71ef5-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="71ef5-113">Atualizar um banco de dados por parâmetro</span><span class="sxs-lookup"><span data-stu-id="71ef5-113">Update a database by parameter</span></span>

## <span data-ttu-id="71ef5-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71ef5-114">PARAMETERS</span></span>

### <span data-ttu-id="71ef5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71ef5-115">-AsJob</span></span>
<span data-ttu-id="71ef5-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="71ef5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="71ef5-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="71ef5-117">-Charset</span></span>
<span data-ttu-id="71ef5-118">O charset do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71ef5-118">The charset of the database.</span></span>

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

### <span data-ttu-id="71ef5-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="71ef5-119">-Collation</span></span>
<span data-ttu-id="71ef5-120">O colamento do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71ef5-120">The collation of the database.</span></span>

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

### <span data-ttu-id="71ef5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ef5-121">-DefaultProfile</span></span>
<span data-ttu-id="71ef5-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71ef5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71ef5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71ef5-123">-InputObject</span></span>
<span data-ttu-id="71ef5-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="71ef5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71ef5-125">-Name</span><span class="sxs-lookup"><span data-stu-id="71ef5-125">-Name</span></span>
<span data-ttu-id="71ef5-126">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71ef5-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ef5-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71ef5-127">-NoWait</span></span>
<span data-ttu-id="71ef5-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="71ef5-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71ef5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ef5-129">-ResourceGroupName</span></span>
<span data-ttu-id="71ef5-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71ef5-130">The name of the resource group.</span></span>
<span data-ttu-id="71ef5-131">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="71ef5-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="71ef5-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71ef5-132">-ServerName</span></span>
<span data-ttu-id="71ef5-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="71ef5-133">The name of the server.</span></span>

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

### <span data-ttu-id="71ef5-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71ef5-134">-SubscriptionId</span></span>
<span data-ttu-id="71ef5-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="71ef5-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="71ef5-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71ef5-136">-Confirm</span></span>
<span data-ttu-id="71ef5-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71ef5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ef5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ef5-138">-WhatIf</span></span>
<span data-ttu-id="71ef5-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71ef5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ef5-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71ef5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ef5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ef5-141">CommonParameters</span></span>
<span data-ttu-id="71ef5-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71ef5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ef5-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71ef5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ef5-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71ef5-144">INPUTS</span></span>

### <span data-ttu-id="71ef5-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="71ef5-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="71ef5-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71ef5-146">OUTPUTS</span></span>

### <span data-ttu-id="71ef5-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="71ef5-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="71ef5-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="71ef5-148">NOTES</span></span>

<span data-ttu-id="71ef5-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="71ef5-149">ALIASES</span></span>

<span data-ttu-id="71ef5-150">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="71ef5-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71ef5-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="71ef5-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71ef5-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71ef5-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71ef5-153">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="71ef5-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71ef5-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="71ef5-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71ef5-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71ef5-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71ef5-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="71ef5-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71ef5-157">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="71ef5-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71ef5-158">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="71ef5-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="71ef5-159">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="71ef5-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71ef5-160">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71ef5-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="71ef5-161">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="71ef5-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="71ef5-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="71ef5-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71ef5-163">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="71ef5-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71ef5-164">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="71ef5-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="71ef5-165">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71ef5-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71ef5-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71ef5-166">RELATED LINKS</span></span>

