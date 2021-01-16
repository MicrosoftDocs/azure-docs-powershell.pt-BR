---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 656fbdc012f4e6de5f80c88a20cde42a49244618
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262681"
---
# <span data-ttu-id="d2e16-101">Remove-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="d2e16-101">Remove-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="d2e16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2e16-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e16-103">Exclui um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2e16-103">Deletes a database.</span></span>

## <span data-ttu-id="d2e16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2e16-104">SYNTAX</span></span>

### <span data-ttu-id="d2e16-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2e16-105">Delete (Default)</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e16-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d2e16-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2e16-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2e16-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e16-108">Exclui um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2e16-108">Deletes a database.</span></span>

## <span data-ttu-id="d2e16-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2e16-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e16-110">Exemplo 1: remover o banco de dados MySql por nome</span><span class="sxs-lookup"><span data-stu-id="d2e16-110">Example 1: Remove MySql database by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test
```

<span data-ttu-id="d2e16-111">Este cmdlet Remove o banco de dados MySql por nome.</span><span class="sxs-lookup"><span data-stu-id="d2e16-111">This cmdlet removes MySql database by name.</span></span>

### <span data-ttu-id="d2e16-112">Exemplo 2: remover o banco de dados MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="d2e16-112">Example 2: Remove MySql database by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/databases/databasetest"
PS C:\> Remove-AzMySqlFlexibleServerDatabase -InputObject $ID
 
```

<span data-ttu-id="d2e16-113">Esses cmdlets removem o banco de dados MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d2e16-113">These cmdlets remove MySql database by identity.</span></span>

## <span data-ttu-id="d2e16-114">OS</span><span class="sxs-lookup"><span data-stu-id="d2e16-114">PARAMETERS</span></span>

### <span data-ttu-id="d2e16-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2e16-115">-AsJob</span></span>
<span data-ttu-id="d2e16-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d2e16-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d2e16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e16-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e16-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e16-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2e16-119">-InputObject</span></span>
<span data-ttu-id="d2e16-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d2e16-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2e16-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2e16-121">-Name</span></span>
<span data-ttu-id="d2e16-122">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2e16-122">The name of the database.</span></span>

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

### <span data-ttu-id="d2e16-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d2e16-123">-NoWait</span></span>
<span data-ttu-id="d2e16-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d2e16-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2e16-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2e16-125">-PassThru</span></span>
<span data-ttu-id="d2e16-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d2e16-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d2e16-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e16-127">-ResourceGroupName</span></span>
<span data-ttu-id="d2e16-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2e16-128">The name of the resource group.</span></span>
<span data-ttu-id="d2e16-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2e16-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d2e16-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d2e16-130">-ServerName</span></span>
<span data-ttu-id="d2e16-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2e16-131">The name of the server.</span></span>

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

### <span data-ttu-id="d2e16-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2e16-132">-SubscriptionId</span></span>
<span data-ttu-id="d2e16-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2e16-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d2e16-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2e16-134">-Confirm</span></span>
<span data-ttu-id="d2e16-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2e16-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e16-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2e16-136">-WhatIf</span></span>
<span data-ttu-id="d2e16-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2e16-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e16-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2e16-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e16-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e16-139">CommonParameters</span></span>
<span data-ttu-id="d2e16-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e16-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e16-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2e16-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e16-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2e16-142">INPUTS</span></span>

### <span data-ttu-id="d2e16-143">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d2e16-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d2e16-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2e16-144">OUTPUTS</span></span>

### <span data-ttu-id="d2e16-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2e16-145">System.Boolean</span></span>

## <span data-ttu-id="d2e16-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2e16-146">NOTES</span></span>

<span data-ttu-id="d2e16-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2e16-147">ALIASES</span></span>

<span data-ttu-id="d2e16-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="d2e16-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2e16-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="d2e16-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2e16-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2e16-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2e16-151">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="d2e16-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2e16-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2e16-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d2e16-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d2e16-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d2e16-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2e16-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d2e16-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d2e16-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2e16-156">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2e16-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d2e16-157">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="d2e16-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d2e16-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2e16-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d2e16-159">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d2e16-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="d2e16-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d2e16-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d2e16-161">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2e16-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d2e16-162">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d2e16-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d2e16-163">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d2e16-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d2e16-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2e16-164">RELATED LINKS</span></span>

