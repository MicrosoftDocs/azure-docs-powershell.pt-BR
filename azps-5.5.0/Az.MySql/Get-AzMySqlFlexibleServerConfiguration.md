---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0579220e372a937dd25d5956735a321e84523f69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117508"
---
# <span data-ttu-id="4b12a-101">Get-AzMySqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b12a-101">Get-AzMySqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="4b12a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b12a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b12a-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="4b12a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b12a-104">SYNTAX</span></span>

### <span data-ttu-id="4b12a-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b12a-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b12a-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4b12a-106">Get</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4b12a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b12a-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b12a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b12a-108">DESCRIPTION</span></span>
<span data-ttu-id="4b12a-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="4b12a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4b12a-110">EXAMPLES</span></span>

### <span data-ttu-id="4b12a-111">Exemplo 1: Listar todas as configurações no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="4b12a-111">Example 1: List all configurations in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
archive        OFF    OFF           system-default ON, OFF      Enumeration
...
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="4b12a-112">Este cmdlet lista todas as configurações no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="4b12a-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="4b12a-113">Exemplo 2: Obter configuração MySql especificada por nome</span><span class="sxs-lookup"><span data-stu-id="4b12a-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="4b12a-114">Este cmdlet recebe uma configuração MySql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="4b12a-114">This cmdlet gets specified MySql configuration by name.</span></span>

### <span data-ttu-id="4b12a-115">Exemplo 3: Configuração da lista por identidade</span><span class="sxs-lookup"><span data-stu-id="4b12a-115">Example 3: List configuration by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/configurations/wait_timeout"
Get-AzMySqlFlexibleServerConfiguration -Name wait_timeout -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
wait_timeout   28800  28800         system-default 1-31536000   Integer
```

<span data-ttu-id="4b12a-116">Este cmdlet obtém configuração MySql especificada por identidade.</span><span class="sxs-lookup"><span data-stu-id="4b12a-116">This cmdlet gets specified MySql configuration by identity.</span></span>

## <span data-ttu-id="4b12a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b12a-117">PARAMETERS</span></span>

### <span data-ttu-id="4b12a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b12a-118">-DefaultProfile</span></span>
<span data-ttu-id="4b12a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b12a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b12a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b12a-120">-InputObject</span></span>
<span data-ttu-id="4b12a-121">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4b12a-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b12a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b12a-122">-Name</span></span>
<span data-ttu-id="4b12a-123">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-123">The name of the server configuration.</span></span>

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

### <span data-ttu-id="4b12a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b12a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b12a-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b12a-125">The name of the resource group.</span></span>
<span data-ttu-id="4b12a-126">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4b12a-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4b12a-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b12a-127">-ServerName</span></span>
<span data-ttu-id="4b12a-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-128">The name of the server.</span></span>

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

### <span data-ttu-id="4b12a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b12a-129">-SubscriptionId</span></span>
<span data-ttu-id="4b12a-130">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4b12a-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4b12a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b12a-131">CommonParameters</span></span>
<span data-ttu-id="4b12a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b12a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b12a-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b12a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b12a-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="4b12a-134">INPUTS</span></span>

### <span data-ttu-id="4b12a-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4b12a-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="4b12a-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="4b12a-136">OUTPUTS</span></span>

### <span data-ttu-id="4b12a-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4b12a-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="4b12a-138">Notas</span><span class="sxs-lookup"><span data-stu-id="4b12a-138">NOTES</span></span>

<span data-ttu-id="4b12a-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="4b12a-139">ALIASES</span></span>

<span data-ttu-id="4b12a-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4b12a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b12a-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4b12a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b12a-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b12a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b12a-143">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4b12a-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b12a-144">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4b12a-145">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4b12a-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4b12a-146">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4b12a-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4b12a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b12a-148">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="4b12a-149">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="4b12a-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4b12a-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4b12a-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4b12a-151">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4b12a-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="4b12a-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4b12a-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4b12a-153">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4b12a-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4b12a-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4b12a-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4b12a-155">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4b12a-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4b12a-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b12a-156">RELATED LINKS</span></span>

