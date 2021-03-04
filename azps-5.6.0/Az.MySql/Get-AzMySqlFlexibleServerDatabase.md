---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: b060657d9e8d69ebddf639847de7718ec626fdb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890384"
---
# <span data-ttu-id="20b5f-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="20b5f-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="20b5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="20b5f-103">Obtém informações sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="20b5f-103">Gets information about a database.</span></span>

## <span data-ttu-id="20b5f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20b5f-104">SYNTAX</span></span>

### <span data-ttu-id="20b5f-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="20b5f-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20b5f-106">Obter</span><span class="sxs-lookup"><span data-stu-id="20b5f-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="20b5f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20b5f-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="20b5f-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20b5f-108">DESCRIPTION</span></span>
<span data-ttu-id="20b5f-109">Obtém informações sobre um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="20b5f-109">Gets information about a database.</span></span>

## <span data-ttu-id="20b5f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20b5f-110">EXAMPLES</span></span>

### <span data-ttu-id="20b5f-111">Exemplo 1: Obter um banco de dados MySql pelo nome do recurso</span><span class="sxs-lookup"><span data-stu-id="20b5f-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="20b5f-112">Este cmdlet obtém servidor MySql pelo nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="20b5f-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="20b5f-113">Exemplo 2: Obter bancos de dados MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="20b5f-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="20b5f-114">Este cmdlet obtém um servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="20b5f-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="20b5f-115">Exemplo 3: lista todos os bancos de dados MySql no servidor especificado</span><span class="sxs-lookup"><span data-stu-id="20b5f-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="20b5f-116">Este cmdlet lista todos os servidores MySql no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="20b5f-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="20b5f-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20b5f-117">PARAMETERS</span></span>

### <span data-ttu-id="20b5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b5f-118">-DefaultProfile</span></span>
<span data-ttu-id="20b5f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20b5f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b5f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20b5f-120">-InputObject</span></span>
<span data-ttu-id="20b5f-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="20b5f-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20b5f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="20b5f-122">-Name</span></span>
<span data-ttu-id="20b5f-123">O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="20b5f-123">The name of the database.</span></span>

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

### <span data-ttu-id="20b5f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b5f-124">-ResourceGroupName</span></span>
<span data-ttu-id="20b5f-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20b5f-125">The name of the resource group.</span></span>
<span data-ttu-id="20b5f-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="20b5f-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="20b5f-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20b5f-127">-ServerName</span></span>
<span data-ttu-id="20b5f-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="20b5f-128">The name of the server.</span></span>

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

### <span data-ttu-id="20b5f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20b5f-129">-SubscriptionId</span></span>
<span data-ttu-id="20b5f-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="20b5f-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="20b5f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b5f-131">CommonParameters</span></span>
<span data-ttu-id="20b5f-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b5f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b5f-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20b5f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b5f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20b5f-134">INPUTS</span></span>

### <span data-ttu-id="20b5f-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="20b5f-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="20b5f-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20b5f-136">OUTPUTS</span></span>

### <span data-ttu-id="20b5f-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="20b5f-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="20b5f-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="20b5f-138">NOTES</span></span>

<span data-ttu-id="20b5f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="20b5f-139">ALIASES</span></span>

<span data-ttu-id="20b5f-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="20b5f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20b5f-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="20b5f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20b5f-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20b5f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20b5f-143">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="20b5f-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20b5f-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="20b5f-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="20b5f-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="20b5f-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="20b5f-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="20b5f-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="20b5f-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="20b5f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20b5f-148">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="20b5f-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="20b5f-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="20b5f-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="20b5f-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20b5f-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="20b5f-151">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="20b5f-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="20b5f-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="20b5f-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="20b5f-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="20b5f-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="20b5f-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="20b5f-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="20b5f-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="20b5f-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="20b5f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20b5f-156">RELATED LINKS</span></span>

