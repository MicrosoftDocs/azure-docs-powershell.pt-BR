---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerFirewallRule.md
ms.openlocfilehash: 7f2a3e567da4df9a004c5dac642f480a4cd7388a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262476"
---
# <span data-ttu-id="bb719-101">Get-AzMySqlFlexibleServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb719-101">Get-AzMySqlFlexibleServerFirewallRule</span></span>

## <span data-ttu-id="bb719-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb719-102">SYNOPSIS</span></span>
<span data-ttu-id="bb719-103">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="bb719-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb719-104">SYNTAX</span></span>

### <span data-ttu-id="bb719-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb719-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb719-106">Obter</span><span class="sxs-lookup"><span data-stu-id="bb719-106">Get</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bb719-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bb719-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb719-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb719-108">DESCRIPTION</span></span>
<span data-ttu-id="bb719-109">Obtém informações sobre uma regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="bb719-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb719-110">EXAMPLES</span></span>

### <span data-ttu-id="bb719-111">Exemplo 1: obter regras de firewall por nome</span><span class="sxs-lookup"><span data-stu-id="bb719-111">Example 1: Get firewall rules by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -Name firewallrule-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="bb719-112">Este cmdlet obtém regras de firewall por nome.</span><span class="sxs-lookup"><span data-stu-id="bb719-112">This cmdlet gets firewall rules by name.</span></span>

### <span data-ttu-id="bb719-113">Exemplo 2: obter regras de firewall por identidade</span><span class="sxs-lookup"><span data-stu-id="bb719-113">Example 2: Get firewall rules by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/firewallRules/firewallrule-test"
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -InputObject $ID

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
```

<span data-ttu-id="bb719-114">Este cmdlet obtém regras de firewall por identidade.</span><span class="sxs-lookup"><span data-stu-id="bb719-114">This cmdlet gets firewall rules by identity.</span></span>

### <span data-ttu-id="bb719-115">Exemplo 3: lista todas as regras de firewall no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="bb719-115">Example 3: Lists all the firewall rules in the specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

FirewallRuleName   StartIPAddress   EndIPAddress
-----------------  ---------------  ---------------
firewallrule-test   12.12.12.12     23.23.23.23
firewallrule-test2  12.12.12.15     23.23.23.25
```

<span data-ttu-id="bb719-116">Esse cmdlet lista todas as regras de firewall no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="bb719-116">This cmdlet lists all the firewall rule in specified MySql server.</span></span>

## <span data-ttu-id="bb719-117">OS</span><span class="sxs-lookup"><span data-stu-id="bb719-117">PARAMETERS</span></span>

### <span data-ttu-id="bb719-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb719-118">-DefaultProfile</span></span>
<span data-ttu-id="bb719-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb719-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb719-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb719-120">-InputObject</span></span>
<span data-ttu-id="bb719-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="bb719-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bb719-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb719-122">-Name</span></span>
<span data-ttu-id="bb719-123">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="bb719-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb719-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb719-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb719-125">The name of the resource group.</span></span>
<span data-ttu-id="bb719-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bb719-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bb719-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="bb719-127">-ServerName</span></span>
<span data-ttu-id="bb719-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-128">The name of the server.</span></span>

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

### <span data-ttu-id="bb719-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bb719-129">-SubscriptionId</span></span>
<span data-ttu-id="bb719-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="bb719-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bb719-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb719-131">CommonParameters</span></span>
<span data-ttu-id="bb719-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb719-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb719-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb719-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb719-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb719-134">INPUTS</span></span>

### <span data-ttu-id="bb719-135">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="bb719-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="bb719-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb719-136">OUTPUTS</span></span>

### <span data-ttu-id="bb719-137">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb719-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="bb719-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb719-138">NOTES</span></span>

<span data-ttu-id="bb719-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bb719-139">ALIASES</span></span>

<span data-ttu-id="bb719-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="bb719-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bb719-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="bb719-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bb719-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bb719-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bb719-143">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="bb719-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bb719-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="bb719-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bb719-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="bb719-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="bb719-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="bb719-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bb719-148">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="bb719-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="bb719-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="bb719-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb719-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bb719-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bb719-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="bb719-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="bb719-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="bb719-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="bb719-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="bb719-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="bb719-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bb719-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="bb719-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="bb719-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb719-156">RELATED LINKS</span></span>

