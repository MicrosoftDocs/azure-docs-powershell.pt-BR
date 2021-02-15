---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlflexibleserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerConfiguration.md
ms.openlocfilehash: 0f65a007a37df559802a134ec5d6d8fc6fb33d01
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111507"
---
# <span data-ttu-id="e91f3-101">Get-AzPostgreSqlFlexibleServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="e91f3-101">Get-AzPostgreSqlFlexibleServerConfiguration</span></span>

## <span data-ttu-id="e91f3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e91f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e91f3-103">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-103">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="e91f3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e91f3-104">SYNTAX</span></span>

### <span data-ttu-id="e91f3-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e91f3-105">List (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e91f3-106">Obter</span><span class="sxs-lookup"><span data-stu-id="e91f3-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e91f3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e91f3-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServerConfiguration -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e91f3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e91f3-108">DESCRIPTION</span></span>
<span data-ttu-id="e91f3-109">Obtém informações sobre uma configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-109">Gets information about a configuration of server.</span></span>

## <span data-ttu-id="e91f3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e91f3-110">EXAMPLES</span></span>

### <span data-ttu-id="e91f3-111">Exemplo 1: Obter configuração PostgreSql especificada por nome</span><span class="sxs-lookup"><span data-stu-id="e91f3-111">Example 1: Get specified PostgreSql configuration by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -Name work_mem -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
work_mem        4096  4096         system-default 4096-2097151   Integer
```

<span data-ttu-id="e91f3-112">Este cmdlet recebe uma configuração PostgreSql especificada por nome.</span><span class="sxs-lookup"><span data-stu-id="e91f3-112">This cmdlet gets specified PostgreSql configuration by name.</span></span>

### <span data-ttu-id="e91f3-113">Exemplo 2: Listar todas as configurações no servidor PostgreSql especificado</span><span class="sxs-lookup"><span data-stu-id="e91f3-113">Example 2: List all configurations in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConfiguration -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test

Name          Value   DefaultValue  Source        AllowedValues DataType
----          ------  ------------  -------       ------------- ---------
application_name  ""    ""           system-default [A-Za-z0-9._-]*      String
...
pgbouncer.enabled   false  false         system-default true, false   Boolean
```

<span data-ttu-id="e91f3-114">Este cmdlet lista todas as configurações no servidor PostgreSql especificado.</span><span class="sxs-lookup"><span data-stu-id="e91f3-114">This cmdlet lists all configurations in specified PostgreSql server.</span></span>

## <span data-ttu-id="e91f3-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e91f3-115">PARAMETERS</span></span>

### <span data-ttu-id="e91f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e91f3-116">-DefaultProfile</span></span>
<span data-ttu-id="e91f3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e91f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e91f3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e91f3-118">-InputObject</span></span>
<span data-ttu-id="e91f3-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="e91f3-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e91f3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e91f3-120">-Name</span></span>
<span data-ttu-id="e91f3-121">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-121">The name of the server configuration.</span></span>

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

### <span data-ttu-id="e91f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e91f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e91f3-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e91f3-123">The name of the resource group.</span></span>
<span data-ttu-id="e91f3-124">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e91f3-124">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e91f3-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e91f3-125">-ServerName</span></span>
<span data-ttu-id="e91f3-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-126">The name of the server.</span></span>

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

### <span data-ttu-id="e91f3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e91f3-127">-SubscriptionId</span></span>
<span data-ttu-id="e91f3-128">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e91f3-128">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e91f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e91f3-129">CommonParameters</span></span>
<span data-ttu-id="e91f3-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e91f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e91f3-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e91f3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e91f3-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="e91f3-132">INPUTS</span></span>

### <span data-ttu-id="e91f3-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="e91f3-133">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="e91f3-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="e91f3-134">OUTPUTS</span></span>

### <span data-ttu-id="e91f3-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="e91f3-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IConfigurationAutoGenerated</span></span>

## <span data-ttu-id="e91f3-136">Notas</span><span class="sxs-lookup"><span data-stu-id="e91f3-136">NOTES</span></span>

<span data-ttu-id="e91f3-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="e91f3-137">ALIASES</span></span>

<span data-ttu-id="e91f3-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="e91f3-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e91f3-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e91f3-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e91f3-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e91f3-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e91f3-141">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="e91f3-141">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e91f3-142">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="e91f3-143">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e91f3-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="e91f3-144">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="e91f3-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="e91f3-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e91f3-146">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="e91f3-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="e91f3-147">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e91f3-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e91f3-148">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e91f3-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="e91f3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="e91f3-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="e91f3-150">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="e91f3-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="e91f3-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="e91f3-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="e91f3-152">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e91f3-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="e91f3-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e91f3-153">RELATED LINKS</span></span>

