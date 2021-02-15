---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112942"
---
# <span data-ttu-id="19d82-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="19d82-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="19d82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19d82-102">SYNOPSIS</span></span>
<span data-ttu-id="19d82-103">Recebe uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19d82-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="19d82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="19d82-104">SYNTAX</span></span>

### <span data-ttu-id="19d82-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="19d82-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="19d82-106">Obter</span><span class="sxs-lookup"><span data-stu-id="19d82-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="19d82-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="19d82-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="19d82-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="19d82-108">DESCRIPTION</span></span>
<span data-ttu-id="19d82-109">Recebe uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19d82-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="19d82-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="19d82-110">EXAMPLES</span></span>

### <span data-ttu-id="19d82-111">Exemplo 1: Lista todas as Regras de Rede Virtual no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="19d82-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="19d82-112">Este cmdlet lista todas as Regras de Rede Virtual no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="19d82-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="19d82-113">Exemplo 2: Obter Regra de Rede Virtual por nome</span><span class="sxs-lookup"><span data-stu-id="19d82-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="19d82-114">Este cmdlet obtém a Regra de Rede Virtual por nome.</span><span class="sxs-lookup"><span data-stu-id="19d82-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="19d82-115">Exemplo 3: Obter a Regra de Rede Virtual por identidade</span><span class="sxs-lookup"><span data-stu-id="19d82-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="19d82-116">Este cmdlet obtém a Regra de Rede Virtual por identidade.</span><span class="sxs-lookup"><span data-stu-id="19d82-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="19d82-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19d82-117">PARAMETERS</span></span>

### <span data-ttu-id="19d82-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d82-118">-DefaultProfile</span></span>
<span data-ttu-id="19d82-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19d82-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d82-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19d82-120">-InputObject</span></span>
<span data-ttu-id="19d82-121">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="19d82-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="19d82-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="19d82-122">-Name</span></span>
<span data-ttu-id="19d82-123">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19d82-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19d82-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19d82-124">-PassThru</span></span>
<span data-ttu-id="19d82-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="19d82-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="19d82-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d82-126">-ResourceGroupName</span></span>
<span data-ttu-id="19d82-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19d82-127">The name of the resource group.</span></span>
<span data-ttu-id="19d82-128">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19d82-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="19d82-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="19d82-129">-ServerName</span></span>
<span data-ttu-id="19d82-130">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="19d82-130">The name of the server.</span></span>

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

### <span data-ttu-id="19d82-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19d82-131">-SubscriptionId</span></span>
<span data-ttu-id="19d82-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="19d82-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="19d82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d82-133">CommonParameters</span></span>
<span data-ttu-id="19d82-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19d82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d82-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19d82-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d82-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="19d82-136">INPUTS</span></span>

### <span data-ttu-id="19d82-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="19d82-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="19d82-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="19d82-138">OUTPUTS</span></span>

### <span data-ttu-id="19d82-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="19d82-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="19d82-140">Notas</span><span class="sxs-lookup"><span data-stu-id="19d82-140">NOTES</span></span>

<span data-ttu-id="19d82-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="19d82-141">ALIASES</span></span>

<span data-ttu-id="19d82-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="19d82-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="19d82-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="19d82-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="19d82-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="19d82-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="19d82-145">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="19d82-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="19d82-146">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="19d82-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="19d82-147">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="19d82-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="19d82-148">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="19d82-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="19d82-149">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="19d82-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="19d82-150">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="19d82-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="19d82-151">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="19d82-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="19d82-152">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="19d82-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="19d82-153">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="19d82-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="19d82-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="19d82-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="19d82-155">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="19d82-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="19d82-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="19d82-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="19d82-157">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="19d82-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="19d82-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19d82-158">RELATED LINKS</span></span>

