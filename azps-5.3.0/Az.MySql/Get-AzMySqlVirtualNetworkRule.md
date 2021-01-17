---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433520"
---
# <span data-ttu-id="b61f3-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b61f3-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="b61f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b61f3-102">SYNOPSIS</span></span>
<span data-ttu-id="b61f3-103">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b61f3-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="b61f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b61f3-104">SYNTAX</span></span>

### <span data-ttu-id="b61f3-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b61f3-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b61f3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b61f3-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b61f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b61f3-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b61f3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b61f3-108">DESCRIPTION</span></span>
<span data-ttu-id="b61f3-109">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b61f3-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="b61f3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b61f3-110">EXAMPLES</span></span>

### <span data-ttu-id="b61f3-111">Exemplo 1: lista todas as regras de rede virtual no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="b61f3-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="b61f3-112">Esse cmdlet lista todas as regras de rede virtual no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="b61f3-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="b61f3-113">Exemplo 2: obter uma regra de rede virtual por nome</span><span class="sxs-lookup"><span data-stu-id="b61f3-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="b61f3-114">Este cmdlet obtém uma regra de rede virtual por nome.</span><span class="sxs-lookup"><span data-stu-id="b61f3-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="b61f3-115">Exemplo 3: obter regra de rede virtual por identidade</span><span class="sxs-lookup"><span data-stu-id="b61f3-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="b61f3-116">Este cmdlet obtém a regra de rede virtual por identidade.</span><span class="sxs-lookup"><span data-stu-id="b61f3-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="b61f3-117">OS</span><span class="sxs-lookup"><span data-stu-id="b61f3-117">PARAMETERS</span></span>

### <span data-ttu-id="b61f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61f3-118">-DefaultProfile</span></span>
<span data-ttu-id="b61f3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b61f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b61f3-120">-InputObject</span></span>
<span data-ttu-id="b61f3-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b61f3-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b61f3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b61f3-122">-Name</span></span>
<span data-ttu-id="b61f3-123">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b61f3-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b61f3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b61f3-124">-PassThru</span></span>
<span data-ttu-id="b61f3-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="b61f3-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b61f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="b61f3-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b61f3-127">The name of the resource group.</span></span>
<span data-ttu-id="b61f3-128">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b61f3-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b61f3-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b61f3-129">-ServerName</span></span>
<span data-ttu-id="b61f3-130">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b61f3-130">The name of the server.</span></span>

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

### <span data-ttu-id="b61f3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b61f3-131">-SubscriptionId</span></span>
<span data-ttu-id="b61f3-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b61f3-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b61f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61f3-133">CommonParameters</span></span>
<span data-ttu-id="b61f3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61f3-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b61f3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61f3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b61f3-136">INPUTS</span></span>

### <span data-ttu-id="b61f3-137">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b61f3-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b61f3-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b61f3-138">OUTPUTS</span></span>

### <span data-ttu-id="b61f3-139">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b61f3-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b61f3-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b61f3-140">NOTES</span></span>

<span data-ttu-id="b61f3-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b61f3-141">ALIASES</span></span>

<span data-ttu-id="b61f3-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b61f3-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b61f3-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b61f3-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b61f3-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b61f3-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b61f3-145">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b61f3-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b61f3-146">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b61f3-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b61f3-147">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b61f3-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b61f3-148">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b61f3-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b61f3-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b61f3-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b61f3-150">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="b61f3-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b61f3-151">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b61f3-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b61f3-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b61f3-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b61f3-153">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b61f3-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="b61f3-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b61f3-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b61f3-155">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b61f3-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b61f3-156">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b61f3-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b61f3-157">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b61f3-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b61f3-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b61f3-158">RELATED LINKS</span></span>

