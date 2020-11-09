---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282230"
---
# <span data-ttu-id="fdaff-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="fdaff-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="fdaff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdaff-102">SYNOPSIS</span></span>
<span data-ttu-id="fdaff-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-103">Gets information about a server.</span></span>

## <span data-ttu-id="fdaff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdaff-104">SYNTAX</span></span>

### <span data-ttu-id="fdaff-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdaff-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fdaff-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fdaff-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fdaff-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fdaff-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fdaff-108">Programação</span><span class="sxs-lookup"><span data-stu-id="fdaff-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="fdaff-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdaff-109">DESCRIPTION</span></span>
<span data-ttu-id="fdaff-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-110">Gets information about a server.</span></span>

## <span data-ttu-id="fdaff-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdaff-111">EXAMPLES</span></span>

### <span data-ttu-id="fdaff-112">Exemplo 1: obter servidor MySql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="fdaff-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fdaff-113">Este cmdlet obtém o servidor MySql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="fdaff-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="fdaff-114">Exemplo 2: obter o MySql Server por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="fdaff-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fdaff-115">Este cmdlet obtém o MySql Server por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="fdaff-116">Exemplo 3: lista todos os servidores MySql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="fdaff-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fdaff-117">Esse cmdlet lista todos os servidores MySql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="fdaff-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="fdaff-118">Exemplo 4: obter o servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="fdaff-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="fdaff-119">Essas listas de cmdlets obtêm o servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="fdaff-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="fdaff-120">OS</span><span class="sxs-lookup"><span data-stu-id="fdaff-120">PARAMETERS</span></span>

### <span data-ttu-id="fdaff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdaff-121">-DefaultProfile</span></span>
<span data-ttu-id="fdaff-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fdaff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdaff-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdaff-123">-InputObject</span></span>
<span data-ttu-id="fdaff-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fdaff-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fdaff-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdaff-125">-Name</span></span>
<span data-ttu-id="fdaff-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-126">The name of the server.</span></span>

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

### <span data-ttu-id="fdaff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdaff-127">-ResourceGroupName</span></span>
<span data-ttu-id="fdaff-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdaff-128">The name of the resource group.</span></span>
<span data-ttu-id="fdaff-129">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fdaff-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="fdaff-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fdaff-130">-SubscriptionId</span></span>
<span data-ttu-id="fdaff-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fdaff-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="fdaff-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdaff-132">CommonParameters</span></span>
<span data-ttu-id="fdaff-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdaff-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdaff-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdaff-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdaff-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdaff-135">INPUTS</span></span>

### <span data-ttu-id="fdaff-136">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="fdaff-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="fdaff-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdaff-137">OUTPUTS</span></span>

### <span data-ttu-id="fdaff-138">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="fdaff-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="fdaff-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdaff-139">NOTES</span></span>

<span data-ttu-id="fdaff-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fdaff-140">ALIASES</span></span>

<span data-ttu-id="fdaff-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fdaff-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fdaff-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fdaff-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fdaff-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fdaff-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fdaff-144">INPUTobject <IMySqlIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fdaff-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fdaff-145">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fdaff-146">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fdaff-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fdaff-147">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fdaff-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fdaff-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fdaff-149">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="fdaff-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fdaff-150">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fdaff-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="fdaff-151">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="fdaff-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="fdaff-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="fdaff-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fdaff-153">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="fdaff-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fdaff-154">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="fdaff-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="fdaff-155">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fdaff-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fdaff-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdaff-156">RELATED LINKS</span></span>

