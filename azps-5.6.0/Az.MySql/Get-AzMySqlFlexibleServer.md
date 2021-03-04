---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893153"
---
# <span data-ttu-id="cbe47-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="cbe47-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="cbe47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe47-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe47-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-103">Gets information about a server.</span></span>

## <span data-ttu-id="cbe47-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cbe47-104">SYNTAX</span></span>

### <span data-ttu-id="cbe47-105">List1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cbe47-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbe47-106">Obter</span><span class="sxs-lookup"><span data-stu-id="cbe47-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbe47-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cbe47-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cbe47-108">Listar</span><span class="sxs-lookup"><span data-stu-id="cbe47-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cbe47-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cbe47-109">DESCRIPTION</span></span>
<span data-ttu-id="cbe47-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-110">Gets information about a server.</span></span>

## <span data-ttu-id="cbe47-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbe47-111">EXAMPLES</span></span>

### <span data-ttu-id="cbe47-112">Exemplo 1: Obter servidor MySql com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="cbe47-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cbe47-113">Este cmdlet obtém servidores MySql com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="cbe47-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="cbe47-114">Exemplo 2: Obter servidor MySql por grupo de recursos e nome de servidor</span><span class="sxs-lookup"><span data-stu-id="cbe47-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cbe47-115">Este cmdlet obtém servidores MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="cbe47-116">Exemplo 3: lista todos os servidores MySql no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="cbe47-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cbe47-117">Este cmdlet lista todos os servidores MySql no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cbe47-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="cbe47-118">Exemplo 4: Obter servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="cbe47-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="cbe47-119">Este cmdlet lista servidores MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="cbe47-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="cbe47-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cbe47-120">PARAMETERS</span></span>

### <span data-ttu-id="cbe47-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe47-121">-DefaultProfile</span></span>
<span data-ttu-id="cbe47-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe47-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe47-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbe47-123">-InputObject</span></span>
<span data-ttu-id="cbe47-124">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="cbe47-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cbe47-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cbe47-125">-Name</span></span>
<span data-ttu-id="cbe47-126">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-126">The name of the server.</span></span>

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

### <span data-ttu-id="cbe47-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe47-127">-ResourceGroupName</span></span>
<span data-ttu-id="cbe47-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbe47-128">The name of the resource group.</span></span>
<span data-ttu-id="cbe47-129">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cbe47-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cbe47-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbe47-130">-SubscriptionId</span></span>
<span data-ttu-id="cbe47-131">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cbe47-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cbe47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe47-132">CommonParameters</span></span>
<span data-ttu-id="cbe47-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe47-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbe47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe47-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbe47-135">INPUTS</span></span>

### <span data-ttu-id="cbe47-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cbe47-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="cbe47-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cbe47-137">OUTPUTS</span></span>

### <span data-ttu-id="cbe47-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="cbe47-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="cbe47-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="cbe47-139">NOTES</span></span>

<span data-ttu-id="cbe47-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cbe47-140">ALIASES</span></span>

<span data-ttu-id="cbe47-141">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="cbe47-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cbe47-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="cbe47-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cbe47-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cbe47-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cbe47-144">INPUTOBJECT <IMySqlIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="cbe47-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cbe47-145">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cbe47-146">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cbe47-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cbe47-147">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cbe47-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="cbe47-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cbe47-149">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="cbe47-150">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="cbe47-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cbe47-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cbe47-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cbe47-152">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="cbe47-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="cbe47-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="cbe47-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cbe47-154">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="cbe47-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cbe47-155">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="cbe47-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cbe47-156">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="cbe47-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cbe47-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbe47-157">RELATED LINKS</span></span>

