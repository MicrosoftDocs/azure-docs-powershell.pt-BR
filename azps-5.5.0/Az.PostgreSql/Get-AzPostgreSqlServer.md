---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111503"
---
# <span data-ttu-id="4d3e7-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="4d3e7-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="4d3e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3e7-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-103">Gets information about a server.</span></span>

## <span data-ttu-id="4d3e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d3e7-104">SYNTAX</span></span>

### <span data-ttu-id="4d3e7-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4d3e7-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d3e7-106">Obter</span><span class="sxs-lookup"><span data-stu-id="4d3e7-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d3e7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4d3e7-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4d3e7-108">Lista</span><span class="sxs-lookup"><span data-stu-id="4d3e7-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d3e7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d3e7-109">DESCRIPTION</span></span>
<span data-ttu-id="4d3e7-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-110">Gets information about a server.</span></span>

## <span data-ttu-id="4d3e7-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d3e7-111">EXAMPLES</span></span>

### <span data-ttu-id="4d3e7-112">Exemplo 1: Obter servidor PostgreSql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="4d3e7-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4d3e7-113">Este cmdlet obtém o servidor PostgreSql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="4d3e7-114">Exemplo 2: Obter servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4d3e7-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4d3e7-115">Este cmdlet obtém o servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="4d3e7-116">Exemplo 3: Lista todos os servidores PostgreSql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="4d3e7-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4d3e7-117">Este cmdlet lista todos os servidores PostgreSql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="4d3e7-118">Exemplo 4: Obter servidor PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="4d3e7-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4d3e7-119">Essa lista de cmdlets obtém o servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="4d3e7-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d3e7-120">PARAMETERS</span></span>

### <span data-ttu-id="4d3e7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3e7-121">-DefaultProfile</span></span>
<span data-ttu-id="4d3e7-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d3e7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d3e7-123">-InputObject</span></span>
<span data-ttu-id="4d3e7-124">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4d3e7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d3e7-125">-Name</span></span>
<span data-ttu-id="4d3e7-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-126">The name of the server.</span></span>

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

### <span data-ttu-id="4d3e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d3e7-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-128">The name of the resource group.</span></span>
<span data-ttu-id="4d3e7-129">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4d3e7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d3e7-130">-SubscriptionId</span></span>
<span data-ttu-id="4d3e7-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4d3e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3e7-132">CommonParameters</span></span>
<span data-ttu-id="4d3e7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3e7-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d3e7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3e7-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d3e7-135">INPUTS</span></span>

### <span data-ttu-id="4d3e7-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="4d3e7-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="4d3e7-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d3e7-137">OUTPUTS</span></span>

### <span data-ttu-id="4d3e7-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="4d3e7-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="4d3e7-139">Notas</span><span class="sxs-lookup"><span data-stu-id="4d3e7-139">NOTES</span></span>

<span data-ttu-id="4d3e7-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="4d3e7-140">ALIASES</span></span>

<span data-ttu-id="4d3e7-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4d3e7-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4d3e7-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d3e7-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4d3e7-144">INPUTOBJECT: <IPostgreSqlIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4d3e7-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4d3e7-145">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4d3e7-146">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4d3e7-147">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4d3e7-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4d3e7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4d3e7-149">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4d3e7-150">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4d3e7-151">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="4d3e7-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4d3e7-153">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4d3e7-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4d3e7-155">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4d3e7-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4d3e7-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d3e7-156">RELATED LINKS</span></span>

