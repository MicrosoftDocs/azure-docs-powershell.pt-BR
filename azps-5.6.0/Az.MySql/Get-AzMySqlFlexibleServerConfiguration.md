---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 8dca573eb0d527beb08bb591b0c8fa3b2fc6e30a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893147"
---
# <span data-ttu-id="5fab7-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fab7-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="5fab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fab7-102">SYNOPSIS</span></span>
<span data-ttu-id="5fab7-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5fab7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5fab7-104">SYNTAX</span></span>

### <span data-ttu-id="5fab7-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5fab7-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5fab7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="5fab7-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5fab7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5fab7-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fab7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5fab7-108">DESCRIPTION</span></span>
<span data-ttu-id="5fab7-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="5fab7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fab7-110">EXAMPLES</span></span>

### <span data-ttu-id="5fab7-111">Exemplo 1: listar todas as configurações no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="5fab7-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="5fab7-112">Este cmdlet lista todas as configurações no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="5fab7-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="5fab7-113">Exemplo 2: Obter configuração MySql especificada pelo nome</span><span class="sxs-lookup"><span data-stu-id="5fab7-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="5fab7-114">Este cmdlet obtém configuração MySql especificada pelo nome.</span><span class="sxs-lookup"><span data-stu-id="5fab7-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="5fab7-115">Exemplo 3: Listar configuração por identidade</span><span class="sxs-lookup"><span data-stu-id="5fab7-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="5fab7-116">Este cmdlet obtém configuração MySql especificada por identidade.</span><span class="sxs-lookup"><span data-stu-id="5fab7-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="5fab7-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5fab7-117">PARAMETERS</span></span>

### <span data-ttu-id="5fab7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fab7-118">-DefaultProfile</span></span>
<span data-ttu-id="5fab7-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fab7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fab7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fab7-120">-InputObject</span></span>
<span data-ttu-id="5fab7-121">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5fab7-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5fab7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5fab7-122">-Name</span></span>
<span data-ttu-id="5fab7-123">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="5fab7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fab7-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fab7-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fab7-125">The name of the resource group.</span></span>
<span data-ttu-id="5fab7-126">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5fab7-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5fab7-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5fab7-127">-ServerName</span></span>
<span data-ttu-id="5fab7-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-128">The name of the server.</span></span>

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

### <span data-ttu-id="5fab7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fab7-129">-SubscriptionId</span></span>
<span data-ttu-id="5fab7-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5fab7-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5fab7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fab7-131">CommonParameters</span></span>
<span data-ttu-id="5fab7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fab7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fab7-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fab7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fab7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fab7-134">INPUTS</span></span>

### <span data-ttu-id="5fab7-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5fab7-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5fab7-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5fab7-136">OUTPUTS</span></span>

### <span data-ttu-id="5fab7-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5fab7-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="5fab7-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="5fab7-138">NOTES</span></span>

<span data-ttu-id="5fab7-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5fab7-139">ALIASES</span></span>

<span data-ttu-id="5fab7-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="5fab7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fab7-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5fab7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fab7-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fab7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fab7-143">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="5fab7-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fab7-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5fab7-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="5fab7-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5fab7-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5fab7-147">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5fab7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fab7-148">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5fab7-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="5fab7-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5fab7-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5fab7-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5fab7-151">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5fab7-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="5fab7-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="5fab7-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5fab7-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="5fab7-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5fab7-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="5fab7-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5fab7-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="5fab7-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5fab7-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fab7-156">RELATED LINKS</span></span>

