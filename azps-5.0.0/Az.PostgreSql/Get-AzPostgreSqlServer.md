---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283852"
---
# <span data-ttu-id="3a0ab-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="3a0ab-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="3a0ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0ab-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-103">Gets information about a server.</span></span>

## <span data-ttu-id="3a0ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a0ab-104">SYNTAX</span></span>

### <span data-ttu-id="3a0ab-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="3a0ab-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a0ab-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3a0ab-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a0ab-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a0ab-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3a0ab-108">Programação</span><span class="sxs-lookup"><span data-stu-id="3a0ab-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a0ab-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a0ab-109">DESCRIPTION</span></span>
<span data-ttu-id="3a0ab-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-110">Gets information about a server.</span></span>

## <span data-ttu-id="3a0ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a0ab-111">EXAMPLES</span></span>

### <span data-ttu-id="3a0ab-112">Exemplo 1: obter servidor PostgreSql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="3a0ab-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3a0ab-113">Este cmdlet obtém um servidor PostgreSql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="3a0ab-114">Exemplo 2: obter servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="3a0ab-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3a0ab-115">Este cmdlet obtém um servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="3a0ab-116">Exemplo 3: lista todos os servidores PostgreSql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="3a0ab-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3a0ab-117">Esse cmdlet lista todos os servidores PostgreSql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="3a0ab-118">Exemplo 4: obter servidor PostgreSql por identidade</span><span class="sxs-lookup"><span data-stu-id="3a0ab-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="3a0ab-119">Esta lista de cmdlets Obtém servidor PostgreSql por identidade.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="3a0ab-120">OS</span><span class="sxs-lookup"><span data-stu-id="3a0ab-120">PARAMETERS</span></span>

### <span data-ttu-id="3a0ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0ab-121">-DefaultProfile</span></span>
<span data-ttu-id="3a0ab-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a0ab-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a0ab-123">-InputObject</span></span>
<span data-ttu-id="3a0ab-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a0ab-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a0ab-125">-Name</span></span>
<span data-ttu-id="3a0ab-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-126">The name of the server.</span></span>

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

### <span data-ttu-id="3a0ab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a0ab-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a0ab-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-128">The name of the resource group.</span></span>
<span data-ttu-id="3a0ab-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="3a0ab-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a0ab-130">-SubscriptionId</span></span>
<span data-ttu-id="3a0ab-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="3a0ab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0ab-132">CommonParameters</span></span>
<span data-ttu-id="3a0ab-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0ab-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a0ab-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0ab-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a0ab-135">INPUTS</span></span>

### <span data-ttu-id="3a0ab-136">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3a0ab-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="3a0ab-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a0ab-137">OUTPUTS</span></span>

### <span data-ttu-id="3a0ab-138">Microsoft. Azure. PowerShell. cmdlets. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="3a0ab-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="3a0ab-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a0ab-139">NOTES</span></span>

<span data-ttu-id="3a0ab-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3a0ab-140">ALIASES</span></span>

<span data-ttu-id="3a0ab-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="3a0ab-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a0ab-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a0ab-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a0ab-144">INPUTobject <IPostgreSqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="3a0ab-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a0ab-145">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3a0ab-146">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3a0ab-147">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3a0ab-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3a0ab-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a0ab-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3a0ab-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3a0ab-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="3a0ab-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3a0ab-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3a0ab-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3a0ab-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3a0ab-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3a0ab-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a0ab-156">RELATED LINKS</span></span>

