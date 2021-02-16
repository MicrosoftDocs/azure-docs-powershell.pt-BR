---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113376"
---
# <span data-ttu-id="73d69-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="73d69-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="73d69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73d69-102">SYNOPSIS</span></span>
<span data-ttu-id="73d69-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="73d69-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73d69-104">SYNTAX</span></span>

### <span data-ttu-id="73d69-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73d69-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73d69-106">Obter</span><span class="sxs-lookup"><span data-stu-id="73d69-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73d69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73d69-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73d69-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="73d69-108">DESCRIPTION</span></span>
<span data-ttu-id="73d69-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="73d69-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="73d69-110">EXAMPLES</span></span>

### <span data-ttu-id="73d69-111">Exemplo 1: Listar todas as configurações no servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="73d69-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="73d69-112">Este cmdlet lista todas as configurações no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="73d69-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="73d69-113">Exemplo 2: Obter configuração PostgreSql especificada por nome</span><span class="sxs-lookup"><span data-stu-id="73d69-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="73d69-114">Este cmdlet recebe uma configuração PostgreSql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="73d69-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="73d69-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73d69-115">PARAMETERS</span></span>

### <span data-ttu-id="73d69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d69-116">-DefaultProfile</span></span>
<span data-ttu-id="73d69-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73d69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73d69-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73d69-118">-InputObject</span></span>
<span data-ttu-id="73d69-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="73d69-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73d69-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="73d69-120">-Name</span></span>
<span data-ttu-id="73d69-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="73d69-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d69-122">-ResourceGroupName</span></span>
<span data-ttu-id="73d69-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73d69-123">The name of the resource group.</span></span>
<span data-ttu-id="73d69-124">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73d69-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="73d69-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73d69-125">-ServerName</span></span>
<span data-ttu-id="73d69-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-126">The name of the server.</span></span>

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

### <span data-ttu-id="73d69-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73d69-127">-SubscriptionId</span></span>
<span data-ttu-id="73d69-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="73d69-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="73d69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d69-129">CommonParameters</span></span>
<span data-ttu-id="73d69-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d69-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73d69-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d69-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="73d69-132">INPUTS</span></span>

### <span data-ttu-id="73d69-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="73d69-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="73d69-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="73d69-134">OUTPUTS</span></span>

### <span data-ttu-id="73d69-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="73d69-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="73d69-136">Notas</span><span class="sxs-lookup"><span data-stu-id="73d69-136">NOTES</span></span>

<span data-ttu-id="73d69-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="73d69-137">ALIASES</span></span>

<span data-ttu-id="73d69-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="73d69-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73d69-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="73d69-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73d69-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73d69-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73d69-141">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="73d69-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73d69-142">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="73d69-143">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="73d69-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="73d69-144">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="73d69-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="73d69-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73d69-146">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="73d69-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="73d69-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73d69-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="73d69-148">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="73d69-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="73d69-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="73d69-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="73d69-150">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="73d69-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="73d69-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="73d69-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="73d69-152">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="73d69-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="73d69-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73d69-153">RELATED LINKS</span></span>

