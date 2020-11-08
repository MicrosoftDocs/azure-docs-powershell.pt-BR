---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlConfiguration.md
ms.openlocfilehash: 7fdc31b4a64733ce686b38ccfb176f754f3f84ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112927"
---
# <span data-ttu-id="002c7-101">Get-AzPostgreSqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="002c7-101">Get-AzPostgreSqlConfiguration</span></span>

## <span data-ttu-id="002c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="002c7-102">SYNOPSIS</span></span>
<span data-ttu-id="002c7-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="002c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="002c7-104">SYNTAX</span></span>

### <span data-ttu-id="002c7-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="002c7-105">List (Default)</span></span>
```
Get-AzPostgreSqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="002c7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="002c7-106">Get</span></span>
```
Get-AzPostgreSqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="002c7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="002c7-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="002c7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="002c7-108">DESCRIPTION</span></span>
<span data-ttu-id="002c7-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="002c7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="002c7-110">EXAMPLES</span></span>

### <span data-ttu-id="002c7-111">Exemplo 1: listar todas as configurações no servidor PostgreSql</span><span class="sxs-lookup"><span data-stu-id="002c7-111">Example 1: List all configurations in PostgreSql server</span></span>
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

<span data-ttu-id="002c7-112">Esse cmdlet lista todas as configurações no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="002c7-112">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

### <span data-ttu-id="002c7-113">Exemplo 2: obter a configuração de PostgreSql especificado por nome</span><span class="sxs-lookup"><span data-stu-id="002c7-113">Example 2: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlConfiguration -Name timezone -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name     Value
----     -----
timezone UTC
```

<span data-ttu-id="002c7-114">Este cmdlet obtém a configuração PostgreSql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="002c7-114">This cmdlet gets specified PostgreSql configuration by name.</span></span>

## <span data-ttu-id="002c7-115">OS</span><span class="sxs-lookup"><span data-stu-id="002c7-115">PARAMETERS</span></span>

### <span data-ttu-id="002c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002c7-116">-DefaultProfile</span></span>
<span data-ttu-id="002c7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="002c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="002c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="002c7-118">-InputObject</span></span>
<span data-ttu-id="002c7-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="002c7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="002c7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="002c7-120">-Name</span></span>
<span data-ttu-id="002c7-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="002c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="002c7-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="002c7-123">The name of the resource group.</span></span>
<span data-ttu-id="002c7-124">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="002c7-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="002c7-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="002c7-125">-ServerName</span></span>
<span data-ttu-id="002c7-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-126">The name of the server.</span></span>

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

### <span data-ttu-id="002c7-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="002c7-127">-SubscriptionId</span></span>
<span data-ttu-id="002c7-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="002c7-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="002c7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002c7-129">CommonParameters</span></span>
<span data-ttu-id="002c7-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="002c7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002c7-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="002c7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002c7-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="002c7-132">INPUTS</span></span>

### <span data-ttu-id="002c7-133">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="002c7-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="002c7-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="002c7-134">OUTPUTS</span></span>

### <span data-ttu-id="002c7-135">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="002c7-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="002c7-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="002c7-136">NOTES</span></span>

<span data-ttu-id="002c7-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="002c7-137">ALIASES</span></span>

<span data-ttu-id="002c7-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="002c7-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="002c7-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="002c7-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="002c7-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="002c7-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="002c7-141">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="002c7-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="002c7-142">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="002c7-143">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="002c7-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="002c7-144">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="002c7-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="002c7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="002c7-146">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="002c7-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="002c7-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="002c7-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="002c7-148">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="002c7-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="002c7-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="002c7-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="002c7-150">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="002c7-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="002c7-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="002c7-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="002c7-152">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="002c7-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="002c7-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="002c7-153">RELATED LINKS</span></span>

