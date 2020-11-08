---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118223"
---
# <span data-ttu-id="8003f-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8003f-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="8003f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8003f-102">SYNOPSIS</span></span>
<span data-ttu-id="8003f-103">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="8003f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8003f-104">SYNTAX</span></span>

### <span data-ttu-id="8003f-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="8003f-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8003f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8003f-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8003f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8003f-107">DESCRIPTION</span></span>
<span data-ttu-id="8003f-108">Exclui uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="8003f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8003f-109">EXAMPLES</span></span>

### <span data-ttu-id="8003f-110">Exemplo 1: remover a regra de firewall do PostgreSql por nome</span><span class="sxs-lookup"><span data-stu-id="8003f-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="8003f-111">Este cmdlet Remove a regra de firewall do PostgreSql por nome.</span><span class="sxs-lookup"><span data-stu-id="8003f-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="8003f-112">Exemplo 2: remover a regra de firewall do PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="8003f-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="8003f-113">Esses cmdlets removem a regra de firewall do PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="8003f-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="8003f-114">OS</span><span class="sxs-lookup"><span data-stu-id="8003f-114">PARAMETERS</span></span>

### <span data-ttu-id="8003f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8003f-115">-AsJob</span></span>
<span data-ttu-id="8003f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8003f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8003f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8003f-117">-DefaultProfile</span></span>
<span data-ttu-id="8003f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8003f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8003f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8003f-119">-InputObject</span></span>
<span data-ttu-id="8003f-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8003f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8003f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8003f-121">-Name</span></span>
<span data-ttu-id="8003f-122">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8003f-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8003f-123">-NoWait</span></span>
<span data-ttu-id="8003f-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8003f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8003f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8003f-125">-PassThru</span></span>
<span data-ttu-id="8003f-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8003f-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8003f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8003f-127">-ResourceGroupName</span></span>
<span data-ttu-id="8003f-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8003f-128">The name of the resource group.</span></span>
<span data-ttu-id="8003f-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8003f-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8003f-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8003f-130">-ServerName</span></span>
<span data-ttu-id="8003f-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-131">The name of the server.</span></span>

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

### <span data-ttu-id="8003f-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8003f-132">-SubscriptionId</span></span>
<span data-ttu-id="8003f-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8003f-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8003f-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8003f-134">-Confirm</span></span>
<span data-ttu-id="8003f-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8003f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8003f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8003f-136">-WhatIf</span></span>
<span data-ttu-id="8003f-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8003f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8003f-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8003f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8003f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8003f-139">CommonParameters</span></span>
<span data-ttu-id="8003f-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8003f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8003f-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8003f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8003f-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8003f-142">INPUTS</span></span>

### <span data-ttu-id="8003f-143">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8003f-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="8003f-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8003f-144">OUTPUTS</span></span>

### <span data-ttu-id="8003f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8003f-145">System.Boolean</span></span>

## <span data-ttu-id="8003f-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8003f-146">NOTES</span></span>

<span data-ttu-id="8003f-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8003f-147">ALIASES</span></span>

<span data-ttu-id="8003f-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8003f-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8003f-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8003f-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8003f-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8003f-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8003f-151">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8003f-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8003f-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8003f-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8003f-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8003f-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8003f-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8003f-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8003f-156">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="8003f-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8003f-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8003f-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8003f-158">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8003f-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="8003f-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="8003f-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8003f-160">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8003f-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8003f-161">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8003f-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8003f-162">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8003f-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8003f-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8003f-163">RELATED LINKS</span></span>

