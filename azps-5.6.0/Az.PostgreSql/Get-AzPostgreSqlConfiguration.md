---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 97b16f3930eda94e69c3528432ee54927c3eef7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885272"
---
# <span data-ttu-id="41471-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="41471-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="41471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41471-102">SYNOPSIS</span></span>
<span data-ttu-id="41471-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="41471-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="41471-104">SYNTAX</span></span>

### <span data-ttu-id="41471-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="41471-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41471-106">Obter</span><span class="sxs-lookup"><span data-stu-id="41471-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41471-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41471-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="41471-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="41471-108">DESCRIPTION</span></span>
<span data-ttu-id="41471-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="41471-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41471-110">EXAMPLES</span></span>

### <span data-ttu-id="41471-111">Exemplo 1: Listar todas as configurações no servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="41471-111">Example 1: List all configurations in PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                                  Value
----                                  -----
array_nulls                           on
backslash_quote                       safe_encoding
bytea_output                          hex
check_function_bodies                 on
client_encoding                       sql_ascii
...
azure.replication_support             REPLICA
max_wal_senders                       10
max_replication_slots                 10
hot_standby_feedback                  off
logging_collector                     on
```

<span data-ttu-id="41471-112">Este cmdlet lista todas as configurações no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="41471-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="41471-113">Exemplo 2: Obter configuração PostgreSql especificada pelo nome</span><span class="sxs-lookup"><span data-stu-id="41471-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="41471-114">Este cmdlet obtém configuração PostgreSql especificada pelo nome.</span><span class="sxs-lookup"><span data-stu-id="41471-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="41471-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="41471-115">PARAMETERS</span></span>

### <span data-ttu-id="41471-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41471-116">-DefaultProfile</span></span>
<span data-ttu-id="41471-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41471-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41471-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41471-118">-InputObject</span></span>
<span data-ttu-id="41471-119">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="41471-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41471-120">-Name</span><span class="sxs-lookup"><span data-stu-id="41471-120">-Name</span></span>
<span data-ttu-id="41471-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-121">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41471-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41471-122">-ResourceGroupName</span></span>
<span data-ttu-id="41471-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41471-123">The name of the resource group.</span></span>
<span data-ttu-id="41471-124">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="41471-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="41471-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="41471-125">-ServerName</span></span>
<span data-ttu-id="41471-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-126">The name of the server.</span></span>

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

### <span data-ttu-id="41471-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41471-127">-SubscriptionId</span></span>
<span data-ttu-id="41471-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="41471-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="41471-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41471-129">CommonParameters</span></span>
<span data-ttu-id="41471-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41471-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41471-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41471-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41471-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41471-132">INPUTS</span></span>

### <span data-ttu-id="41471-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="41471-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="41471-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="41471-134">OUTPUTS</span></span>

### <span data-ttu-id="41471-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="41471-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="41471-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="41471-136">NOTES</span></span>

<span data-ttu-id="41471-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="41471-137">ALIASES</span></span>

<span data-ttu-id="41471-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="41471-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41471-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="41471-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41471-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41471-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41471-141">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="41471-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41471-142">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="41471-143">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="41471-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="41471-144">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="41471-145">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="41471-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41471-146">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="41471-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="41471-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41471-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41471-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="41471-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="41471-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="41471-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="41471-150">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="41471-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="41471-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="41471-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="41471-152">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="41471-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="41471-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41471-153">RELATED LINKS</span></span>

