---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893146"
---
# <span data-ttu-id="d336f-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="d336f-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="d336f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d336f-102">SYNOPSIS</span></span>
<span data-ttu-id="d336f-103">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="d336f-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="d336f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d336f-104">SYNTAX</span></span>

### <span data-ttu-id="d336f-105">Get (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d336f-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d336f-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d336f-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d336f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d336f-107">DESCRIPTION</span></span>
<span data-ttu-id="d336f-108">Obter a cadeia de conexão de acordo com o provedor de conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="d336f-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="d336f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d336f-109">EXAMPLES</span></span>

### <span data-ttu-id="d336f-110">Exemplo 1: Obter cadeia de caracteres de conexão por nome</span><span class="sxs-lookup"><span data-stu-id="d336f-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="d336f-111">Este cmdlet mostra a cadeia de conexão de um cliente pelo nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="d336f-112">Exemplo 2: Obter a cadeia de conexão do servidor MySql por identidade</span><span class="sxs-lookup"><span data-stu-id="d336f-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="d336f-113">Este cmdlet obtém a cadeia de conexão do servidor MySql por identidade.</span><span class="sxs-lookup"><span data-stu-id="d336f-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="d336f-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d336f-114">PARAMETERS</span></span>

### <span data-ttu-id="d336f-115">-Client</span><span class="sxs-lookup"><span data-stu-id="d336f-115">-Client</span></span>
<span data-ttu-id="d336f-116">Provedor de conexão de cliente.</span><span class="sxs-lookup"><span data-stu-id="d336f-116">Client connection provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d336f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d336f-117">-DefaultProfile</span></span>
<span data-ttu-id="d336f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d336f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d336f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d336f-119">-InputObject</span></span>
<span data-ttu-id="d336f-120">O servidor para a cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="d336f-120">The server for the connection string.</span></span>
<span data-ttu-id="d336f-121">Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d336f-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d336f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d336f-122">-Name</span></span>
<span data-ttu-id="d336f-123">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-123">The name of the server.</span></span>

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

### <span data-ttu-id="d336f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d336f-124">-ResourceGroupName</span></span>
<span data-ttu-id="d336f-125">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d336f-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d336f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d336f-126">-SubscriptionId</span></span>
<span data-ttu-id="d336f-127">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d336f-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d336f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d336f-128">CommonParameters</span></span>
<span data-ttu-id="d336f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d336f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d336f-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d336f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d336f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d336f-131">INPUTS</span></span>

### <span data-ttu-id="d336f-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d336f-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d336f-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d336f-133">OUTPUTS</span></span>

### <span data-ttu-id="d336f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d336f-134">System.String</span></span>

## <span data-ttu-id="d336f-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d336f-135">NOTES</span></span>

<span data-ttu-id="d336f-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d336f-136">ALIASES</span></span>

<span data-ttu-id="d336f-137">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d336f-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d336f-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d336f-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d336f-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d336f-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d336f-140">INPUTOBJECT <IMySqlIdentity> : o servidor para a cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="d336f-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="d336f-141">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d336f-142">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d336f-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d336f-143">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d336f-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d336f-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d336f-145">`[KeyName <String>]`: O nome da chave do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d336f-146">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="d336f-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d336f-147">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d336f-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d336f-148">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d336f-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="d336f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="d336f-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d336f-150">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="d336f-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d336f-151">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="d336f-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d336f-152">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="d336f-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d336f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d336f-153">RELATED LINKS</span></span>

