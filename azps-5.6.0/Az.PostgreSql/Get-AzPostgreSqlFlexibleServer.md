---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 3354014ed0e6e81b1460da061e75e614bbd5f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893125"
---
# <span data-ttu-id="4d715-101">Get-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="4d715-101">Get-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="4d715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d715-102">SYNOPSIS</span></span>
<span data-ttu-id="4d715-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-103">Gets information about a server.</span></span>

## <span data-ttu-id="4d715-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4d715-104">SYNTAX</span></span>

### <span data-ttu-id="4d715-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d715-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d715-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4d715-106">Get</span></span>
```
Get-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d715-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d715-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d715-108">Listar</span><span class="sxs-lookup"><span data-stu-id="4d715-108">List</span></span>
```
Get-AzPostgreSqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4d715-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4d715-109">DESCRIPTION</span></span>
<span data-ttu-id="4d715-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-110">Gets information about a server.</span></span>

## <span data-ttu-id="4d715-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d715-111">EXAMPLES</span></span>

### <span data-ttu-id="4d715-112">Exemplo 1: Obter servidor PostgreSql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="4d715-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="4d715-113">Este cmdlet obtém servidores PostgreSql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="4d715-113">This cmdlet gets PostgreSql servers with default context.</span></span>

### <span data-ttu-id="4d715-114">Exemplo 2: Obter servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4d715-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

Name            Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----            -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="4d715-115">Este cmdlet obtém servidores PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-115">This cmdlet gets PostgreSql servers by resource group and server name.</span></span>

### <span data-ttu-id="4d715-116">Exemplo 3: lista todos os servidores PostgreSql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="4d715-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest

Name             Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----             -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test  eastus   postgresql-test     12     32768                   Standard_D2s_v3 GeneralPurpose
postgresql-test2 eastus   postgresql-test     12     32768                   Standard_42s_v3 GeneralPurpose
```

<span data-ttu-id="4d715-117">Este cmdlet lista todos os servidores PostgreSql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4d715-117">This cmdlet lists all the PostgreSql servers in the specified resource group.</span></span>

### <span data-ttu-id="4d715-118">Exemplo 4: Obter servidor PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="4d715-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Get-AzPostgreSqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
postgresql-test eastus   postgresql-test         12     32768                    Standard_D2s_v3 GeneralPurpose
```

<span data-ttu-id="4d715-119">Este cmdlet lista servidores PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="4d715-119">This cmdlet lists gets PostgreSql servers by identity.</span></span>

## <span data-ttu-id="4d715-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4d715-120">PARAMETERS</span></span>

### <span data-ttu-id="4d715-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d715-121">-DefaultProfile</span></span>
<span data-ttu-id="4d715-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d715-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d715-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d715-123">-InputObject</span></span>
<span data-ttu-id="4d715-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4d715-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d715-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4d715-125">-Name</span></span>
<span data-ttu-id="4d715-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d715-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d715-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d715-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d715-128">The name of the resource group.</span></span>
<span data-ttu-id="4d715-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d715-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d715-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d715-130">-SubscriptionId</span></span>
<span data-ttu-id="4d715-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d715-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d715-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d715-132">CommonParameters</span></span>
<span data-ttu-id="4d715-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d715-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d715-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d715-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d715-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d715-135">INPUTS</span></span>

### <span data-ttu-id="4d715-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4d715-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4d715-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4d715-137">OUTPUTS</span></span>

### <span data-ttu-id="4d715-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4d715-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="4d715-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="4d715-139">NOTES</span></span>

<span data-ttu-id="4d715-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4d715-140">ALIASES</span></span>

<span data-ttu-id="4d715-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4d715-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d715-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4d715-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d715-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d715-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d715-144">INPUTOBJECT <IPostgreSqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4d715-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d715-145">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4d715-146">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d715-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4d715-147">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4d715-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4d715-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d715-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="4d715-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4d715-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d715-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d715-151">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d715-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d715-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4d715-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4d715-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d715-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4d715-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d715-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d715-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4d715-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4d715-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d715-156">RELATED LINKS</span></span>

