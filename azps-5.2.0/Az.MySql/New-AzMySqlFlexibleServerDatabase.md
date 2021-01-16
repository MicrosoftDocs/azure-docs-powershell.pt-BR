---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258649"
---
# <span data-ttu-id="48c47-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="48c47-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="48c47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48c47-102">SYNOPSIS</span></span>
<span data-ttu-id="48c47-103">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="48c47-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="48c47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48c47-104">SYNTAX</span></span>

### <span data-ttu-id="48c47-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="48c47-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="48c47-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="48c47-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48c47-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48c47-107">DESCRIPTION</span></span>
<span data-ttu-id="48c47-108">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="48c47-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="48c47-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48c47-109">EXAMPLES</span></span>

### <span data-ttu-id="48c47-110">Exemplo 1: criar um novo banco de dados do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="48c47-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="48c47-111">Crie um banco de dados com as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="48c47-111">Create a database with default settings.</span></span>

## <span data-ttu-id="48c47-112">OS</span><span class="sxs-lookup"><span data-stu-id="48c47-112">PARAMETERS</span></span>

### <span data-ttu-id="48c47-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48c47-113">-AsJob</span></span>
<span data-ttu-id="48c47-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="48c47-114">Run the command as a job</span></span>

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

### <span data-ttu-id="48c47-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="48c47-115">-Charset</span></span>
<span data-ttu-id="48c47-116">O charset do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48c47-116">The charset of the database.</span></span>

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

### <span data-ttu-id="48c47-117">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="48c47-117">-Collation</span></span>
<span data-ttu-id="48c47-118">O agrupamento do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48c47-118">The collation of the database.</span></span>

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

### <span data-ttu-id="48c47-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c47-119">-DefaultProfile</span></span>
<span data-ttu-id="48c47-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48c47-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c47-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48c47-121">-InputObject</span></span>
<span data-ttu-id="48c47-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="48c47-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48c47-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="48c47-123">-Name</span></span>
<span data-ttu-id="48c47-124">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48c47-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c47-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="48c47-125">-NoWait</span></span>
<span data-ttu-id="48c47-126">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="48c47-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="48c47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c47-127">-ResourceGroupName</span></span>
<span data-ttu-id="48c47-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48c47-128">The name of the resource group.</span></span>
<span data-ttu-id="48c47-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="48c47-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c47-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="48c47-130">-ServerName</span></span>
<span data-ttu-id="48c47-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="48c47-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c47-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48c47-132">-SubscriptionId</span></span>
<span data-ttu-id="48c47-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="48c47-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c47-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48c47-134">-Confirm</span></span>
<span data-ttu-id="48c47-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48c47-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48c47-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48c47-136">-WhatIf</span></span>
<span data-ttu-id="48c47-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48c47-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48c47-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48c47-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48c47-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c47-139">CommonParameters</span></span>
<span data-ttu-id="48c47-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c47-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c47-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48c47-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c47-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48c47-142">INPUTS</span></span>

### <span data-ttu-id="48c47-143">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="48c47-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="48c47-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48c47-144">OUTPUTS</span></span>

### <span data-ttu-id="48c47-145">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="48c47-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="48c47-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48c47-146">NOTES</span></span>

<span data-ttu-id="48c47-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="48c47-147">ALIASES</span></span>

<span data-ttu-id="48c47-148">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="48c47-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48c47-149">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="48c47-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48c47-150">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48c47-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48c47-151">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="48c47-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48c47-152">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="48c47-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="48c47-153">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48c47-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="48c47-154">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="48c47-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="48c47-155">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="48c47-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48c47-156">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="48c47-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="48c47-157">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="48c47-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="48c47-158">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48c47-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="48c47-159">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="48c47-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="48c47-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="48c47-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="48c47-161">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="48c47-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="48c47-162">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="48c47-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="48c47-163">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48c47-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="48c47-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48c47-164">RELATED LINKS</span></span>

