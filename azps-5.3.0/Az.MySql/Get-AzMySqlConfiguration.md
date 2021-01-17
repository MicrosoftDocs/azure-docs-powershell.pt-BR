---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427094"
---
# <span data-ttu-id="8e9a6-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9a6-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="8e9a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9a6-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e9a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e9a6-104">SYNTAX</span></span>

### <span data-ttu-id="8e9a6-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e9a6-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e9a6-106">Obter</span><span class="sxs-lookup"><span data-stu-id="8e9a6-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8e9a6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8e9a6-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8e9a6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e9a6-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9a6-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="8e9a6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e9a6-110">EXAMPLES</span></span>

### <span data-ttu-id="8e9a6-111">Exemplo 1: listar todas as configurações no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="8e9a6-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name                                     Type
----                                     ----
audit_log_enabled                        Microsoft.DBforMySQL/servers/configurations
audit_log_events                         Microsoft.DBforMySQL/servers/configurations
audit_log_exclude_users                  Microsoft.DBforMySQL/servers/configurations
audit_log_include_users                  Microsoft.DBforMySQL/servers/configurations
...
transaction_prealloc_size                Microsoft.DBforMySQL/servers/configurations
tx_isolation                             Microsoft.DBforMySQL/servers/configurations
updatable_views_with_limit               Microsoft.DBforMySQL/servers/configurations
wait_timeout                             Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="8e9a6-112">Esse cmdlet lista todas as configurações do servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="8e9a6-113">Exemplo 2: obter a configuração do MySql especificado por nome</span><span class="sxs-lookup"><span data-stu-id="8e9a6-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="8e9a6-114">Este cmdlet obtém a configuração de MySql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="8e9a6-115">OS</span><span class="sxs-lookup"><span data-stu-id="8e9a6-115">PARAMETERS</span></span>

### <span data-ttu-id="8e9a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9a6-116">-DefaultProfile</span></span>
<span data-ttu-id="8e9a6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e9a6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e9a6-118">-InputObject</span></span>
<span data-ttu-id="8e9a6-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8e9a6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e9a6-120">-Name</span></span>
<span data-ttu-id="8e9a6-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="8e9a6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9a6-122">-ResourceGroupName</span></span>
<span data-ttu-id="8e9a6-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-123">The name of the resource group.</span></span>
<span data-ttu-id="8e9a6-124">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8e9a6-125">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="8e9a6-125">-ServerName</span></span>
<span data-ttu-id="8e9a6-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-126">The name of the server.</span></span>

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

### <span data-ttu-id="8e9a6-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e9a6-127">-SubscriptionId</span></span>
<span data-ttu-id="8e9a6-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8e9a6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9a6-129">CommonParameters</span></span>
<span data-ttu-id="8e9a6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9a6-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e9a6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9a6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e9a6-132">INPUTS</span></span>

### <span data-ttu-id="8e9a6-133">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8e9a6-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8e9a6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e9a6-134">OUTPUTS</span></span>

### <span data-ttu-id="8e9a6-135">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9a6-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="8e9a6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e9a6-136">NOTES</span></span>

<span data-ttu-id="8e9a6-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8e9a6-137">ALIASES</span></span>

<span data-ttu-id="8e9a6-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8e9a6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8e9a6-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8e9a6-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8e9a6-141">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8e9a6-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8e9a6-142">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8e9a6-143">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8e9a6-144">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8e9a6-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8e9a6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8e9a6-146">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8e9a6-147">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8e9a6-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8e9a6-149">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="8e9a6-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8e9a6-151">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8e9a6-152">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8e9a6-153">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8e9a6-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8e9a6-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e9a6-154">RELATED LINKS</span></span>

