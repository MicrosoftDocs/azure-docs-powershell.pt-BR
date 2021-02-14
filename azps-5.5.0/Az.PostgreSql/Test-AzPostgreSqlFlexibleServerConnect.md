---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/test-azpostgresqlflexibleserverconnect
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Test-AzPostgreSqlFlexibleServerConnect.md
ms.openlocfilehash: 1cbc4b8274a619514268e8412f7f9123a5e9e58a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117263"
---
# <span data-ttu-id="76fae-101">Test-AzPostgreSqlFlexibleServerConnect</span><span class="sxs-lookup"><span data-stu-id="76fae-101">Test-AzPostgreSqlFlexibleServerConnect</span></span>

## <span data-ttu-id="76fae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76fae-102">SYNOPSIS</span></span>
<span data-ttu-id="76fae-103">Testar a conexão com o servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="76fae-103">Test out the connection to the database server</span></span>

## <span data-ttu-id="76fae-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76fae-104">SYNTAX</span></span>

### <span data-ttu-id="76fae-105">Teste (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76fae-105">Test (Default)</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76fae-106">TestAndQuery</span><span class="sxs-lookup"><span data-stu-id="76fae-106">TestAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -Name <String> -QueryText <String> -ResourceGroupName <String>
 -AdministratorLoginPassword <SecureString> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76fae-107">TestViaIdentity</span><span class="sxs-lookup"><span data-stu-id="76fae-107">TestViaIdentity</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76fae-108">TestViaIdentityAndQuery</span><span class="sxs-lookup"><span data-stu-id="76fae-108">TestViaIdentityAndQuery</span></span>
```
Test-AzPostgreSqlFlexibleServerConnect -QueryText <String> -AdministratorLoginPassword <SecureString>
 -InputObject <IPostgreSqlIdentity> [-DatabaseName <String>] [-AdministratorUserName <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76fae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="76fae-109">DESCRIPTION</span></span>
<span data-ttu-id="76fae-110">Testar a conexão com o servidor de banco de dados</span><span class="sxs-lookup"><span data-stu-id="76fae-110">Test out the connection to the database server</span></span>

## <span data-ttu-id="76fae-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76fae-111">EXAMPLES</span></span>

### <span data-ttu-id="76fae-112">Exemplo 1: Testar conexão por nome</span><span class="sxs-lookup"><span data-stu-id="76fae-112">Example 1: Test connection by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="76fae-113">Testar a conexão pelo grupo de recursos e pelo nome do servidor</span><span class="sxs-lookup"><span data-stu-id="76fae-113">Test connection by the resource group and the server name</span></span>

### <span data-ttu-id="76fae-114">Exemplo 2: Testar conexão por identidade</span><span class="sxs-lookup"><span data-stu-id="76fae-114">Example 2: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -AdministratorLoginPassword $password

The connection testing to postgresql-test.database.azure.com was successful!
```

<span data-ttu-id="76fae-115">Testar a conexão pela identidade</span><span class="sxs-lookup"><span data-stu-id="76fae-115">Test connection by the identity</span></span>

### <span data-ttu-id="76fae-116">Exemplo 3: Testar consulta por nome</span><span class="sxs-lookup"><span data-stu-id="76fae-116">Example 3: Test query by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerConnect -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test -AdministratorLoginPassword $password -Query "SELECT * FROM test"

col
-----
1
2
3
```

<span data-ttu-id="76fae-117">Testar uma consulta pelo grupo de recursos e pelo nome do servidor</span><span class="sxs-lookup"><span data-stu-id="76fae-117">Test a query by the resource group and the server name</span></span>

### <span data-ttu-id="76fae-118">Exemplo 4: Testar conexão por identidade</span><span class="sxs-lookup"><span data-stu-id="76fae-118">Example 4: Test connection by identity</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -ServerName postgresql-test | Get-AzPostgreSqlFlexibleServerConnect -Query "SELECT * FROM test" -AdministratorLoginPassword $password

col
-----
1
2
3
```

<span data-ttu-id="76fae-119">Testar uma consulta pela identidade</span><span class="sxs-lookup"><span data-stu-id="76fae-119">Test a query by the identity</span></span>

## <span data-ttu-id="76fae-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76fae-120">PARAMETERS</span></span>

### <span data-ttu-id="76fae-121">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="76fae-121">-AdministratorLoginPassword</span></span>
<span data-ttu-id="76fae-122">A senha do administrador.</span><span class="sxs-lookup"><span data-stu-id="76fae-122">The password of the administrator.</span></span>
<span data-ttu-id="76fae-123">Mínimo de 8 caracteres e máximo de 128 caracteres.</span><span class="sxs-lookup"><span data-stu-id="76fae-123">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="76fae-124">A senha deve conter caracteres de três das seguintes categorias: letras maiúsculas em inglês, letras minúsculas em inglês, números e caracteres não alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="76fae-124">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-125">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="76fae-125">-AdministratorUserName</span></span>
<span data-ttu-id="76fae-126">Nome de usuário do administrador para o servidor.</span><span class="sxs-lookup"><span data-stu-id="76fae-126">Administrator username for the server.</span></span>
<span data-ttu-id="76fae-127">Depois de definido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="76fae-127">Once set, it cannot be changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-128">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="76fae-128">-DatabaseName</span></span>
<span data-ttu-id="76fae-129">O nome do banco de dados para se conectar.</span><span class="sxs-lookup"><span data-stu-id="76fae-129">The database name to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76fae-130">-DefaultProfile</span></span>
<span data-ttu-id="76fae-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76fae-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76fae-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76fae-132">-InputObject</span></span>
<span data-ttu-id="76fae-133">O servidor para se conectar.</span><span class="sxs-lookup"><span data-stu-id="76fae-133">The server to connect.</span></span>
<span data-ttu-id="76fae-134">Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="76fae-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: TestViaIdentity, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="76fae-135">-Name</span></span>
<span data-ttu-id="76fae-136">O nome do servidor para se conectar.</span><span class="sxs-lookup"><span data-stu-id="76fae-136">The name of the server to connect.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-137">-QueryText</span><span class="sxs-lookup"><span data-stu-id="76fae-137">-QueryText</span></span>
<span data-ttu-id="76fae-138">A consulta para o banco de dados a ser testado</span><span class="sxs-lookup"><span data-stu-id="76fae-138">The query for the database to test</span></span>

```yaml
Type: System.String
Parameter Sets: TestAndQuery, TestViaIdentityAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76fae-139">-ResourceGroupName</span></span>
<span data-ttu-id="76fae-140">O nome do grupo de recursos que contém o recurso, Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="76fae-140">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Test, TestAndQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76fae-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76fae-141">CommonParameters</span></span>
<span data-ttu-id="76fae-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76fae-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76fae-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76fae-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76fae-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="76fae-144">INPUTS</span></span>

### <span data-ttu-id="76fae-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="76fae-145">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="76fae-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="76fae-146">OUTPUTS</span></span>

### <span data-ttu-id="76fae-147">System.String</span><span class="sxs-lookup"><span data-stu-id="76fae-147">System.String</span></span>

## <span data-ttu-id="76fae-148">Notas</span><span class="sxs-lookup"><span data-stu-id="76fae-148">NOTES</span></span>

<span data-ttu-id="76fae-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="76fae-149">ALIASES</span></span>

<span data-ttu-id="76fae-150">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="76fae-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="76fae-151">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="76fae-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="76fae-152">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="76fae-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="76fae-153">INPUTOBJECT: <IPostgreSqlIdentity> O servidor a ser conectado.</span><span class="sxs-lookup"><span data-stu-id="76fae-153">INPUTOBJECT <IPostgreSqlIdentity>: The server to connect.</span></span>
  - <span data-ttu-id="76fae-154">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="76fae-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="76fae-155">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="76fae-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="76fae-156">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="76fae-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="76fae-157">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="76fae-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="76fae-158">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="76fae-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="76fae-159">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="76fae-159">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="76fae-160">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="76fae-160">The name is case insensitive.</span></span>
  - <span data-ttu-id="76fae-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="76fae-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="76fae-162">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="76fae-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="76fae-163">`[SubscriptionId <String>]`: A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="76fae-163">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="76fae-164">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76fae-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="76fae-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76fae-165">RELATED LINKS</span></span>

