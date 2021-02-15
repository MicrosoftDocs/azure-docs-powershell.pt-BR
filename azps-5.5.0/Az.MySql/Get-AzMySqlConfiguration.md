---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlConfiguration.md
ms.openlocfilehash: fae355df0b33fa648be1d9043f140123cf9d79a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115230"
---
# <span data-ttu-id="23329-101">Get-AzMySqlConfiguration</span><span class="sxs-lookup"><span data-stu-id="23329-101">Get-AzMySqlConfiguration</span></span>

## <span data-ttu-id="23329-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23329-102">SYNOPSIS</span></span>
<span data-ttu-id="23329-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="23329-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23329-104">SYNTAX</span></span>

### <span data-ttu-id="23329-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="23329-105">List (Default)</span></span>
```
Get-AzMySqlConfiguration -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23329-106">Obter</span><span class="sxs-lookup"><span data-stu-id="23329-106">Get</span></span>
```
Get-AzMySqlConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23329-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="23329-107">GetViaIdentity</span></span>
```
Get-AzMySqlConfiguration -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="23329-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="23329-108">DESCRIPTION</span></span>
<span data-ttu-id="23329-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="23329-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="23329-110">EXAMPLES</span></span>

### <span data-ttu-id="23329-111">Exemplo 1: Listar todas as configurações no servidor MySql especificado</span><span class="sxs-lookup"><span data-stu-id="23329-111">Example 1: List all configurations in specified MySql server</span></span>
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

<span data-ttu-id="23329-112">Este cmdlet lista todas as configurações no servidor MySql especificado.</span><span class="sxs-lookup"><span data-stu-id="23329-112">This cmdlet lists all configurations in specified MySql server.</span></span>

### <span data-ttu-id="23329-113">Exemplo 2: Obter configuração MySql especificada por nome</span><span class="sxs-lookup"><span data-stu-id="23329-113">Example 2: Get specified MySql configuration by name</span></span>
```powershell
PS C:\> Get-AzMySqlConfiguration -Name time_zone -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name      Type
----      ----
time_zone Microsoft.DBforMySQL/servers/configurations
```

<span data-ttu-id="23329-114">Este cmdlet recebe uma configuração MySql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="23329-114">This cmdlet gets specified MySql configuration by name.</span></span>

## <span data-ttu-id="23329-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23329-115">PARAMETERS</span></span>

### <span data-ttu-id="23329-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23329-116">-DefaultProfile</span></span>
<span data-ttu-id="23329-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23329-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23329-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23329-118">-InputObject</span></span>
<span data-ttu-id="23329-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="23329-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23329-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="23329-120">-Name</span></span>
<span data-ttu-id="23329-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="23329-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23329-122">-ResourceGroupName</span></span>
<span data-ttu-id="23329-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23329-123">The name of the resource group.</span></span>
<span data-ttu-id="23329-124">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="23329-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="23329-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="23329-125">-ServerName</span></span>
<span data-ttu-id="23329-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-126">The name of the server.</span></span>

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

### <span data-ttu-id="23329-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23329-127">-SubscriptionId</span></span>
<span data-ttu-id="23329-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23329-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="23329-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23329-129">CommonParameters</span></span>
<span data-ttu-id="23329-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23329-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23329-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23329-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23329-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="23329-132">INPUTS</span></span>

### <span data-ttu-id="23329-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="23329-133">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="23329-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="23329-134">OUTPUTS</span></span>

### <span data-ttu-id="23329-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="23329-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IConfiguration</span></span>

## <span data-ttu-id="23329-136">Notas</span><span class="sxs-lookup"><span data-stu-id="23329-136">NOTES</span></span>

<span data-ttu-id="23329-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="23329-137">ALIASES</span></span>

<span data-ttu-id="23329-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="23329-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23329-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="23329-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23329-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23329-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23329-141">INPUTOBJECT: <IMySqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="23329-141">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23329-142">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="23329-143">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="23329-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="23329-144">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="23329-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="23329-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23329-146">`[KeyName <String>]`: o nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-146">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="23329-147">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="23329-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="23329-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23329-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="23329-149">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="23329-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="23329-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="23329-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="23329-151">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="23329-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="23329-152">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="23329-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="23329-153">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="23329-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="23329-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23329-154">RELATED LINKS</span></span>

