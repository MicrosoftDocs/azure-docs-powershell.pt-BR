---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114754"
---
# <span data-ttu-id="71141-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71141-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="71141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71141-102">SYNOPSIS</span></span>
<span data-ttu-id="71141-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="71141-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71141-104">SYNTAX</span></span>

### <span data-ttu-id="71141-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71141-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71141-106">Obter</span><span class="sxs-lookup"><span data-stu-id="71141-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71141-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71141-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71141-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="71141-108">DESCRIPTION</span></span>
<span data-ttu-id="71141-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="71141-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71141-110">EXAMPLES</span></span>

### <span data-ttu-id="71141-111">Exemplo 1: Lista todas as Regras de Firewall no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="71141-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="71141-112">Este cmdlet lista toda a Regra de Firewall no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="71141-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="71141-113">Exemplo 2: Obter Regra de Firewall por nome</span><span class="sxs-lookup"><span data-stu-id="71141-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="71141-114">Este cmdlet obtém a Regra de Firewall por nome.</span><span class="sxs-lookup"><span data-stu-id="71141-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="71141-115">Exemplo 3: Obter Regra de Firewall por identidade</span><span class="sxs-lookup"><span data-stu-id="71141-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="71141-116">Este cmdlet obtém a Regra de Firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="71141-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="71141-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71141-117">PARAMETERS</span></span>

### <span data-ttu-id="71141-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71141-118">-DefaultProfile</span></span>
<span data-ttu-id="71141-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71141-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71141-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71141-120">-InputObject</span></span>
<span data-ttu-id="71141-121">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71141-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71141-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="71141-122">-Name</span></span>
<span data-ttu-id="71141-123">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71141-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71141-124">-ResourceGroupName</span></span>
<span data-ttu-id="71141-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71141-125">The name of the resource group.</span></span>
<span data-ttu-id="71141-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="71141-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71141-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71141-127">-ServerName</span></span>
<span data-ttu-id="71141-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71141-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71141-129">-SubscriptionId</span></span>
<span data-ttu-id="71141-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="71141-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71141-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71141-131">CommonParameters</span></span>
<span data-ttu-id="71141-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71141-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71141-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71141-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71141-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="71141-134">INPUTS</span></span>

### <span data-ttu-id="71141-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="71141-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="71141-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="71141-136">OUTPUTS</span></span>

### <span data-ttu-id="71141-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="71141-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="71141-138">Notas</span><span class="sxs-lookup"><span data-stu-id="71141-138">NOTES</span></span>

<span data-ttu-id="71141-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="71141-139">ALIASES</span></span>

<span data-ttu-id="71141-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="71141-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71141-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="71141-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71141-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71141-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71141-143">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="71141-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71141-144">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="71141-145">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71141-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="71141-146">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="71141-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="71141-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71141-148">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="71141-149">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="71141-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="71141-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="71141-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="71141-151">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="71141-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="71141-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="71141-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="71141-153">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="71141-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="71141-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="71141-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="71141-155">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="71141-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="71141-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71141-156">RELATED LINKS</span></span>

