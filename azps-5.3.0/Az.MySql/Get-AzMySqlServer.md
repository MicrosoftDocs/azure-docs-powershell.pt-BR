---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: 4308f2ec3da458f03e53d17a873d92ea5d775ff4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433521"
---
# <span data-ttu-id="c6e45-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="c6e45-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="c6e45-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6e45-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e45-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-103">Gets information about a server.</span></span>

## <span data-ttu-id="c6e45-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6e45-104">SYNTAX</span></span>

### <span data-ttu-id="c6e45-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6e45-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6e45-106">Obter</span><span class="sxs-lookup"><span data-stu-id="c6e45-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6e45-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e45-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c6e45-108">Programação</span><span class="sxs-lookup"><span data-stu-id="c6e45-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6e45-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6e45-109">DESCRIPTION</span></span>
<span data-ttu-id="c6e45-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-110">Gets information about a server.</span></span>

## <span data-ttu-id="c6e45-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6e45-111">EXAMPLES</span></span>

### <span data-ttu-id="c6e45-112">Exemplo 1: obter servidor MySql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="c6e45-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c6e45-113">Este cmdlet obtém o servidor MySql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="c6e45-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="c6e45-114">Exemplo 2: obter o MySql Server por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="c6e45-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c6e45-115">Este cmdlet obtém o MySql Server por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="c6e45-116">Exemplo 3: lista todos os servidores MySql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="c6e45-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c6e45-117">Esse cmdlet lista todos os servidores MySql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c6e45-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="c6e45-118">Exemplo 4: obter o servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="c6e45-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c6e45-119">Essas listas de cmdlets obtêm o servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="c6e45-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="c6e45-120">OS</span><span class="sxs-lookup"><span data-stu-id="c6e45-120">PARAMETERS</span></span>

### <span data-ttu-id="c6e45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e45-121">-DefaultProfile</span></span>
<span data-ttu-id="c6e45-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e45-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e45-123">-InputObject</span></span>
<span data-ttu-id="c6e45-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c6e45-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6e45-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6e45-125">-Name</span></span>
<span data-ttu-id="c6e45-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-126">The name of the server.</span></span>

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

### <span data-ttu-id="c6e45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e45-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6e45-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6e45-128">The name of the resource group.</span></span>
<span data-ttu-id="c6e45-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c6e45-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c6e45-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6e45-130">-SubscriptionId</span></span>
<span data-ttu-id="c6e45-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c6e45-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c6e45-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e45-132">CommonParameters</span></span>
<span data-ttu-id="c6e45-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e45-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e45-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6e45-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e45-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6e45-135">INPUTS</span></span>

### <span data-ttu-id="c6e45-136">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="c6e45-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="c6e45-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6e45-137">OUTPUTS</span></span>

### <span data-ttu-id="c6e45-138">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="c6e45-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="c6e45-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6e45-139">NOTES</span></span>

<span data-ttu-id="c6e45-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c6e45-140">ALIASES</span></span>

<span data-ttu-id="c6e45-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="c6e45-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6e45-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="c6e45-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6e45-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6e45-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6e45-144">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="c6e45-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6e45-145">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="c6e45-146">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c6e45-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c6e45-147">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="c6e45-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="c6e45-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6e45-149">`[KeyName <String>]`: O nome da tecla do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="c6e45-150">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="c6e45-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="c6e45-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6e45-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c6e45-152">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c6e45-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="c6e45-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="c6e45-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="c6e45-154">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c6e45-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="c6e45-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="c6e45-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c6e45-156">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="c6e45-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="c6e45-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6e45-157">RELATED LINKS</span></span>

