---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125124"
---
# <span data-ttu-id="a1653-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a1653-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="a1653-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1653-102">SYNOPSIS</span></span>
<span data-ttu-id="a1653-103">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a1653-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="a1653-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1653-104">SYNTAX</span></span>

### <span data-ttu-id="a1653-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1653-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a1653-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a1653-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a1653-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1653-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a1653-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1653-108">DESCRIPTION</span></span>
<span data-ttu-id="a1653-109">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a1653-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="a1653-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1653-110">EXAMPLES</span></span>

### <span data-ttu-id="a1653-111">Exemplo 1: lista todas as regras de rede virtual no servidor PostgreSql especificado</span><span class="sxs-lookup"><span data-stu-id="a1653-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="a1653-112">Esse cmdlet lista todas as regras de rede virtual no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="a1653-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="a1653-113">Exemplo 2: obter uma regra de rede virtual por nome</span><span class="sxs-lookup"><span data-stu-id="a1653-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="a1653-114">Este cmdlet obtém uma regra de rede virtual por nome.</span><span class="sxs-lookup"><span data-stu-id="a1653-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="a1653-115">Exemplo 3: obter regra de rede virtual por identidade</span><span class="sxs-lookup"><span data-stu-id="a1653-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="a1653-116">Este cmdlet obtém a regra de rede virtual por identidade.</span><span class="sxs-lookup"><span data-stu-id="a1653-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="a1653-117">OS</span><span class="sxs-lookup"><span data-stu-id="a1653-117">PARAMETERS</span></span>

### <span data-ttu-id="a1653-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1653-118">-DefaultProfile</span></span>
<span data-ttu-id="a1653-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1653-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1653-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1653-120">-InputObject</span></span>
<span data-ttu-id="a1653-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a1653-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1653-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1653-122">-Name</span></span>
<span data-ttu-id="a1653-123">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a1653-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a1653-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1653-124">-PassThru</span></span>
<span data-ttu-id="a1653-125">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="a1653-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a1653-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1653-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1653-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1653-127">The name of the resource group.</span></span>
<span data-ttu-id="a1653-128">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a1653-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a1653-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="a1653-129">-ServerName</span></span>
<span data-ttu-id="a1653-130">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a1653-130">The name of the server.</span></span>

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

### <span data-ttu-id="a1653-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1653-131">-SubscriptionId</span></span>
<span data-ttu-id="a1653-132">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a1653-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a1653-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1653-133">CommonParameters</span></span>
<span data-ttu-id="a1653-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1653-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1653-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1653-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1653-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1653-136">INPUTS</span></span>

### <span data-ttu-id="a1653-137">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="a1653-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="a1653-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1653-138">OUTPUTS</span></span>

### <span data-ttu-id="a1653-139">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a1653-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="a1653-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1653-140">NOTES</span></span>

<span data-ttu-id="a1653-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a1653-141">ALIASES</span></span>

<span data-ttu-id="a1653-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="a1653-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1653-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="a1653-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1653-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1653-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1653-145">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="a1653-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1653-146">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="a1653-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="a1653-147">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="a1653-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="a1653-148">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="a1653-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="a1653-149">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a1653-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1653-150">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="a1653-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="a1653-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a1653-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1653-152">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a1653-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1653-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="a1653-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="a1653-154">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="a1653-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="a1653-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a1653-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1653-156">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a1653-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="a1653-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1653-157">RELATED LINKS</span></span>

