---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262654"
---
# <span data-ttu-id="fdd06-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="fdd06-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="fdd06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdd06-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd06-103">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="fdd06-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="fdd06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdd06-104">SYNTAX</span></span>

### <span data-ttu-id="fdd06-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdd06-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fdd06-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="fdd06-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fdd06-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdd06-107">DESCRIPTION</span></span>
<span data-ttu-id="fdd06-108">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="fdd06-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="fdd06-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdd06-109">EXAMPLES</span></span>

### <span data-ttu-id="fdd06-110">Exemplo 1: atualizar um banco de dados de servidor MySql por nome</span><span class="sxs-lookup"><span data-stu-id="fdd06-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="fdd06-111">Atualizar um banco de dados pelo nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="fdd06-111">Update a database by resource name.</span></span>

### <span data-ttu-id="fdd06-112">Exemplo 2: Atualize o banco de dados MySql por parâmetro.</span><span class="sxs-lookup"><span data-stu-id="fdd06-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="fdd06-113">Atualizar um banco de dados por parâmetro</span><span class="sxs-lookup"><span data-stu-id="fdd06-113">Update a database by parameter</span></span>

## <span data-ttu-id="fdd06-114">OS</span><span class="sxs-lookup"><span data-stu-id="fdd06-114">PARAMETERS</span></span>

### <span data-ttu-id="fdd06-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdd06-115">-AsJob</span></span>
<span data-ttu-id="fdd06-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fdd06-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fdd06-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="fdd06-117">-Charset</span></span>
<span data-ttu-id="fdd06-118">O charset do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdd06-118">The charset of the database.</span></span>

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

### <span data-ttu-id="fdd06-119">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="fdd06-119">-Collation</span></span>
<span data-ttu-id="fdd06-120">O agrupamento do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdd06-120">The collation of the database.</span></span>

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

### <span data-ttu-id="fdd06-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd06-121">-DefaultProfile</span></span>
<span data-ttu-id="fdd06-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdd06-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdd06-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdd06-123">-InputObject</span></span>
<span data-ttu-id="fdd06-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fdd06-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdd06-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdd06-125">-Name</span></span>
<span data-ttu-id="fdd06-126">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdd06-126">The name of the database.</span></span>

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

### <span data-ttu-id="fdd06-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fdd06-127">-NoWait</span></span>
<span data-ttu-id="fdd06-128">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="fdd06-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fdd06-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd06-129">-ResourceGroupName</span></span>
<span data-ttu-id="fdd06-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdd06-130">The name of the resource group.</span></span>
<span data-ttu-id="fdd06-131">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fdd06-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fdd06-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="fdd06-132">-ServerName</span></span>
<span data-ttu-id="fdd06-133">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdd06-133">The name of the server.</span></span>

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

### <span data-ttu-id="fdd06-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdd06-134">-SubscriptionId</span></span>
<span data-ttu-id="fdd06-135">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fdd06-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fdd06-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fdd06-136">-Confirm</span></span>
<span data-ttu-id="fdd06-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdd06-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdd06-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdd06-138">-WhatIf</span></span>
<span data-ttu-id="fdd06-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fdd06-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdd06-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fdd06-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdd06-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd06-141">CommonParameters</span></span>
<span data-ttu-id="fdd06-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd06-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd06-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdd06-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd06-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdd06-144">INPUTS</span></span>

### <span data-ttu-id="fdd06-145">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fdd06-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fdd06-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdd06-146">OUTPUTS</span></span>

### <span data-ttu-id="fdd06-147">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="fdd06-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="fdd06-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdd06-148">NOTES</span></span>

<span data-ttu-id="fdd06-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fdd06-149">ALIASES</span></span>

<span data-ttu-id="fdd06-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fdd06-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fdd06-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fdd06-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fdd06-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fdd06-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fdd06-153">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fdd06-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fdd06-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdd06-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fdd06-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdd06-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fdd06-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdd06-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fdd06-157">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fdd06-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fdd06-158">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdd06-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="fdd06-159">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="fdd06-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fdd06-160">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdd06-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fdd06-161">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fdd06-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="fdd06-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="fdd06-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fdd06-163">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdd06-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fdd06-164">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fdd06-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fdd06-165">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fdd06-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fdd06-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdd06-166">RELATED LINKS</span></span>

