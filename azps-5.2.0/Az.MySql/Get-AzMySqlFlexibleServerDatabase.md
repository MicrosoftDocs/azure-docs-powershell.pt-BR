---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262478"
---
# <span data-ttu-id="b8c5c-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c5c-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="b8c5c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c5c-103">Obtém informações sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-103">Gets information about a database.</span></span>

## <span data-ttu-id="b8c5c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8c5c-104">SYNTAX</span></span>

### <span data-ttu-id="b8c5c-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8c5c-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b8c5c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="b8c5c-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b8c5c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c5c-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c5c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8c5c-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c5c-109">Obtém informações sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-109">Gets information about a database.</span></span>

## <span data-ttu-id="b8c5c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8c5c-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c5c-111">Exemplo 1: obter um banco de dados MySql por nome do recurso</span><span class="sxs-lookup"><span data-stu-id="b8c5c-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="b8c5c-112">Este cmdlet obtém o MySql Server por nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="b8c5c-113">Exemplo 2: obter bancos de dados MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="b8c5c-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="b8c5c-114">Esse cmdlet obtém um servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="b8c5c-115">Exemplo 3: lista todos os bancos de dados MySql no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="b8c5c-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="b8c5c-116">Esse cmdlet lista todos os servidores MySql em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="b8c5c-117">OS</span><span class="sxs-lookup"><span data-stu-id="b8c5c-117">PARAMETERS</span></span>

### <span data-ttu-id="b8c5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c5c-118">-DefaultProfile</span></span>
<span data-ttu-id="b8c5c-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c5c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c5c-120">-InputObject</span></span>
<span data-ttu-id="b8c5c-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b8c5c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c5c-122">-Name</span></span>
<span data-ttu-id="b8c5c-123">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c5c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c5c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8c5c-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-125">The name of the resource group.</span></span>
<span data-ttu-id="b8c5c-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b8c5c-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b8c5c-127">-ServerName</span></span>
<span data-ttu-id="b8c5c-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-128">The name of the server.</span></span>

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

### <span data-ttu-id="b8c5c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8c5c-129">-SubscriptionId</span></span>
<span data-ttu-id="b8c5c-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b8c5c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c5c-131">CommonParameters</span></span>
<span data-ttu-id="b8c5c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c5c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c5c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c5c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8c5c-134">INPUTS</span></span>

### <span data-ttu-id="b8c5c-135">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="b8c5c-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="b8c5c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8c5c-136">OUTPUTS</span></span>

### <span data-ttu-id="b8c5c-137">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c5c-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="b8c5c-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8c5c-138">NOTES</span></span>

<span data-ttu-id="b8c5c-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b8c5c-139">ALIASES</span></span>

<span data-ttu-id="b8c5c-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b8c5c-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b8c5c-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b8c5c-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b8c5c-143">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b8c5c-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b8c5c-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b8c5c-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b8c5c-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b8c5c-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b8c5c-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b8c5c-148">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="b8c5c-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b8c5c-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b8c5c-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="b8c5c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b8c5c-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b8c5c-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b8c5c-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="b8c5c-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b8c5c-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8c5c-156">RELATED LINKS</span></span>

