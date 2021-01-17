---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427092"
---
# <span data-ttu-id="45909-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="45909-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="45909-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45909-102">SYNOPSIS</span></span>
<span data-ttu-id="45909-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="45909-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45909-104">SYNTAX</span></span>

### <span data-ttu-id="45909-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="45909-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45909-106">Obter</span><span class="sxs-lookup"><span data-stu-id="45909-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45909-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45909-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="45909-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45909-108">DESCRIPTION</span></span>
<span data-ttu-id="45909-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="45909-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45909-110">EXAMPLES</span></span>

### <span data-ttu-id="45909-111">Exemplo 1: listar todas as configurações no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="45909-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="45909-112">Esse cmdlet lista todas as configurações do servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="45909-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="45909-113">Exemplo 2: obter a configuração do MySql especificado por nome</span><span class="sxs-lookup"><span data-stu-id="45909-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="45909-114">Este cmdlet obtém a configuração de MySql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="45909-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="45909-115">Exemplo 3: listar a configuração por identidade</span><span class="sxs-lookup"><span data-stu-id="45909-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="45909-116">Esse cmdlet obtém a configuração do MySql especificado por identidade.</span><span class="sxs-lookup"><span data-stu-id="45909-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="45909-117">OS</span><span class="sxs-lookup"><span data-stu-id="45909-117">PARAMETERS</span></span>

### <span data-ttu-id="45909-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45909-118">-DefaultProfile</span></span>
<span data-ttu-id="45909-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45909-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45909-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45909-120">-InputObject</span></span>
<span data-ttu-id="45909-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="45909-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45909-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="45909-122">-Name</span></span>
<span data-ttu-id="45909-123">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="45909-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45909-124">-ResourceGroupName</span></span>
<span data-ttu-id="45909-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45909-125">The name of the resource group.</span></span>
<span data-ttu-id="45909-126">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="45909-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="45909-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="45909-127">-ServerName</span></span>
<span data-ttu-id="45909-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-128">The name of the server.</span></span>

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

### <span data-ttu-id="45909-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45909-129">-SubscriptionId</span></span>
<span data-ttu-id="45909-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="45909-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="45909-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45909-131">CommonParameters</span></span>
<span data-ttu-id="45909-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45909-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45909-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45909-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45909-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45909-134">INPUTS</span></span>

### <span data-ttu-id="45909-135">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="45909-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="45909-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45909-136">OUTPUTS</span></span>

### <span data-ttu-id="45909-137">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20200701Preview. IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="45909-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="45909-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45909-138">NOTES</span></span>

<span data-ttu-id="45909-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45909-139">ALIASES</span></span>

<span data-ttu-id="45909-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="45909-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45909-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="45909-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45909-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45909-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45909-143">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="45909-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45909-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="45909-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="45909-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="45909-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="45909-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="45909-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45909-148">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="45909-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="45909-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="45909-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45909-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="45909-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="45909-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="45909-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="45909-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="45909-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="45909-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="45909-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="45909-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="45909-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="45909-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="45909-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45909-156">RELATED LINKS</span></span>

