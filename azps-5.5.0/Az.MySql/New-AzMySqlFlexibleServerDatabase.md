---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 9d8933aad3b3e24893062e43a3b3232bd0b57cfb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114743"
---
# <span data-ttu-id="ec4c0-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4c0-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="ec4c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4c0-103">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ec4c0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec4c0-104">SYNTAX</span></span>

### <span data-ttu-id="ec4c0-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="ec4c0-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec4c0-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec4c0-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec4c0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec4c0-107">DESCRIPTION</span></span>
<span data-ttu-id="ec4c0-108">Cria um novo banco de dados ou atualiza um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="ec4c0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ec4c0-109">EXAMPLES</span></span>

### <span data-ttu-id="ec4c0-110">Exemplo 1: Criar um novo banco de dados do servidor MySql</span><span class="sxs-lookup"><span data-stu-id="ec4c0-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="ec4c0-111">Criar um banco de dados com configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-111">Create a database with default settings.</span></span>

## <span data-ttu-id="ec4c0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec4c0-112">PARAMETERS</span></span>

### <span data-ttu-id="ec4c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec4c0-113">-AsJob</span></span>
<span data-ttu-id="ec4c0-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="ec4c0-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ec4c0-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="ec4c0-115">-Charset</span></span>
<span data-ttu-id="ec4c0-116">O charset do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-116">The charset of the database.</span></span>

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

### <span data-ttu-id="ec4c0-117">-Colagem</span><span class="sxs-lookup"><span data-stu-id="ec4c0-117">-Collation</span></span>
<span data-ttu-id="ec4c0-118">O colamento do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-118">The collation of the database.</span></span>

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

### <span data-ttu-id="ec4c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4c0-119">-DefaultProfile</span></span>
<span data-ttu-id="ec4c0-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4c0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec4c0-121">-InputObject</span></span>
<span data-ttu-id="ec4c0-122">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ec4c0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ec4c0-123">-Name</span></span>
<span data-ttu-id="ec4c0-124">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-124">The name of the database.</span></span>

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

### <span data-ttu-id="ec4c0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ec4c0-125">-NoWait</span></span>
<span data-ttu-id="ec4c0-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="ec4c0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ec4c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec4c0-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-128">The name of the resource group.</span></span>
<span data-ttu-id="ec4c0-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ec4c0-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec4c0-130">-ServerName</span></span>
<span data-ttu-id="ec4c0-131">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-131">The name of the server.</span></span>

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

### <span data-ttu-id="ec4c0-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec4c0-132">-SubscriptionId</span></span>
<span data-ttu-id="ec4c0-133">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ec4c0-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ec4c0-134">-Confirm</span></span>
<span data-ttu-id="ec4c0-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4c0-136">-WhatIf</span></span>
<span data-ttu-id="ec4c0-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4c0-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4c0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4c0-139">CommonParameters</span></span>
<span data-ttu-id="ec4c0-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4c0-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec4c0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4c0-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="ec4c0-142">INPUTS</span></span>

### <span data-ttu-id="ec4c0-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="ec4c0-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="ec4c0-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="ec4c0-144">OUTPUTS</span></span>

### <span data-ttu-id="ec4c0-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="ec4c0-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="ec4c0-146">Notas</span><span class="sxs-lookup"><span data-stu-id="ec4c0-146">NOTES</span></span>

<span data-ttu-id="ec4c0-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="ec4c0-147">ALIASES</span></span>

<span data-ttu-id="ec4c0-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ec4c0-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec4c0-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec4c0-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec4c0-151">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="ec4c0-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec4c0-152">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ec4c0-153">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ec4c0-154">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ec4c0-155">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="ec4c0-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec4c0-156">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="ec4c0-157">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ec4c0-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ec4c0-159">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="ec4c0-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ec4c0-161">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ec4c0-162">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ec4c0-163">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ec4c0-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ec4c0-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec4c0-164">RELATED LINKS</span></span>

