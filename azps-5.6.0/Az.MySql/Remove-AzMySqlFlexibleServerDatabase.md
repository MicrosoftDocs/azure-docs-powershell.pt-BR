---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9f2fbae69d2831d063ea6bfa92e2f1ece90e9f12
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885900"
---
# <span data-ttu-id="877dc-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="877dc-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="877dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="877dc-102">SYNOPSIS</span></span>
<span data-ttu-id="877dc-103">Exclui um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="877dc-103">Deletes a database.</span></span>

## <span data-ttu-id="877dc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="877dc-104">SYNTAX</span></span>

### <span data-ttu-id="877dc-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="877dc-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="877dc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="877dc-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="877dc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="877dc-107">DESCRIPTION</span></span>
<span data-ttu-id="877dc-108">Exclui um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="877dc-108">Deletes a database.</span></span>

## <span data-ttu-id="877dc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="877dc-109">EXAMPLES</span></span>

### <span data-ttu-id="877dc-110">Exemplo 1: Remover banco de dados MySql pelo nome</span><span class="sxs-lookup"><span data-stu-id="877dc-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="877dc-111">Este cmdlet remove o banco de dados MySql pelo nome.</span><span class="sxs-lookup"><span data-stu-id="877dc-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="877dc-112">Exemplo 2: Remover banco de dados MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="877dc-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="877dc-113">Esses cmdlets removem o banco de dados MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="877dc-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="877dc-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="877dc-114">PARAMETERS</span></span>

### <span data-ttu-id="877dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="877dc-115">-AsJob</span></span>
<span data-ttu-id="877dc-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="877dc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="877dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877dc-117">-DefaultProfile</span></span>
<span data-ttu-id="877dc-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="877dc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="877dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="877dc-119">-InputObject</span></span>
<span data-ttu-id="877dc-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="877dc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="877dc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="877dc-121">-Name</span></span>
<span data-ttu-id="877dc-122">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="877dc-122">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877dc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="877dc-123">-NoWait</span></span>
<span data-ttu-id="877dc-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="877dc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="877dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="877dc-125">-PassThru</span></span>
<span data-ttu-id="877dc-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="877dc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="877dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="877dc-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="877dc-128">The name of the resource group.</span></span>
<span data-ttu-id="877dc-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="877dc-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877dc-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="877dc-130">-ServerName</span></span>
<span data-ttu-id="877dc-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="877dc-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877dc-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="877dc-132">-SubscriptionId</span></span>
<span data-ttu-id="877dc-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="877dc-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="877dc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="877dc-134">-Confirm</span></span>
<span data-ttu-id="877dc-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="877dc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="877dc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="877dc-136">-WhatIf</span></span>
<span data-ttu-id="877dc-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="877dc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="877dc-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="877dc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="877dc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877dc-139">CommonParameters</span></span>
<span data-ttu-id="877dc-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877dc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877dc-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="877dc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877dc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="877dc-142">INPUTS</span></span>

### <span data-ttu-id="877dc-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="877dc-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="877dc-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="877dc-144">OUTPUTS</span></span>

### <span data-ttu-id="877dc-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="877dc-145">System.Boolean</span></span>

## <span data-ttu-id="877dc-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="877dc-146">NOTES</span></span>

<span data-ttu-id="877dc-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="877dc-147">ALIASES</span></span>

<span data-ttu-id="877dc-148">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="877dc-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="877dc-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="877dc-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="877dc-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="877dc-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="877dc-151">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="877dc-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="877dc-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="877dc-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="877dc-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="877dc-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="877dc-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="877dc-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="877dc-155">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="877dc-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="877dc-156">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="877dc-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="877dc-157">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="877dc-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="877dc-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="877dc-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="877dc-159">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="877dc-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="877dc-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="877dc-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="877dc-161">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="877dc-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="877dc-162">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="877dc-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="877dc-163">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="877dc-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="877dc-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="877dc-164">RELATED LINKS</span></span>

