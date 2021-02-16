---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404166"
---
# <span data-ttu-id="6d28e-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="6d28e-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="6d28e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d28e-102">SYNOPSIS</span></span>
<span data-ttu-id="6d28e-103">Cria um contexto de conexão do servidor.</span><span class="sxs-lookup"><span data-stu-id="6d28e-103">Creates a server connection context.</span></span>

## <span data-ttu-id="6d28e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d28e-104">SYNTAX</span></span>

### <span data-ttu-id="6d28e-105">ByServerNameWithSqlAuth (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6d28e-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d28e-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="6d28e-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6d28e-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="6d28e-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6d28e-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="6d28e-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6d28e-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="6d28e-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6d28e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d28e-110">DESCRIPTION</span></span>
<span data-ttu-id="6d28e-111">O **cmdlet New-AzureSqlDatabaseServerContext** cria um contexto de conexão do servidor do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d28e-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="6d28e-112">Use a autenticação do SQL Server para criar um contexto de conexão com um servidor de banco de dados SQL usando as credenciais especificadas.</span><span class="sxs-lookup"><span data-stu-id="6d28e-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="6d28e-113">Você pode especificar o servidor de banco de dados SQL por nome, pelo nome totalmente qualificado ou por URL.</span><span class="sxs-lookup"><span data-stu-id="6d28e-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="6d28e-114">Para obter uma credencial, use o cmdlet Get-Credential que solicita que você especifique o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="6d28e-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="6d28e-115">Use o cmdlet **New-AzureSqlDatabaseServerContext** com autenticação baseada em certificado para criar um contexto de conexão para o servidor de banco de dados SQL especificado usando os dados de assinatura especificados do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d28e-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="6d28e-116">Você pode especificar o servidor de banco de dados SQL por nome ou pelo nome totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6d28e-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="6d28e-117">Você pode especificar os dados da assinatura como um parâmetro ou recuperá-los da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d28e-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="6d28e-118">Use o cmdlet Select-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx para selecionar a assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d28e-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="6d28e-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6d28e-119">EXAMPLES</span></span>

### <span data-ttu-id="6d28e-120">Exemplo 1: Criar um contexto usando a autenticação do SQL Server</span><span class="sxs-lookup"><span data-stu-id="6d28e-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="6d28e-121">Este exemplo usa a autenticação do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d28e-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="6d28e-122">O primeiro comando solicita credenciais de administrador do servidor e armazena as credenciais na variável $Credential servidor.</span><span class="sxs-lookup"><span data-stu-id="6d28e-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="6d28e-123">O segundo comando se conecta ao servidor de banco de dados SQL chamado lpqd0zbr8y usando $Credential.</span><span class="sxs-lookup"><span data-stu-id="6d28e-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="6d28e-124">O comando final cria um banco de dados chamado Banco de Dados17 no servidor que faz parte do contexto no $Context.</span><span class="sxs-lookup"><span data-stu-id="6d28e-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="6d28e-125">Exemplo 2: Criar um contexto usando autenticação baseada em certificado</span><span class="sxs-lookup"><span data-stu-id="6d28e-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="6d28e-126">Este exemplo usa a autenticação baseada em certificado.</span><span class="sxs-lookup"><span data-stu-id="6d28e-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="6d28e-127">Os dois primeiros comandos atribuem valores às $SubscriptionId e $Thumbprint variáveis.</span><span class="sxs-lookup"><span data-stu-id="6d28e-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="6d28e-128">O terceiro comando obtém o certificado identificado pela impressão $Thumbprint e armazena-o $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6d28e-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="6d28e-129">O quarto comando define a assinatura como Assinatura07 e o quinto comando seleciona essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="6d28e-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="6d28e-130">O comando final cria um contexto na assinatura atual do servidor chamado lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="6d28e-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="6d28e-131">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d28e-131">PARAMETERS</span></span>

### <span data-ttu-id="6d28e-132">-Credencial</span><span class="sxs-lookup"><span data-stu-id="6d28e-132">-Credential</span></span>
<span data-ttu-id="6d28e-133">Especifica um objeto de credencial que fornece a autenticação do SQL Server para você acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="6d28e-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="6d28e-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="6d28e-135">Especifica o nome de domínio totalmente qualificado (FQDN) para o servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="6d28e-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="6d28e-136">Por exemplo, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="6d28e-136">For example, Server02.database.windows.net.</span></span>

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="6d28e-137">-ManageUrl</span></span>
<span data-ttu-id="6d28e-138">Especifica a URL que esse cmdlet usa para acessar o Portal de Gerenciamento de Banco de Dados SQL do Azure para o servidor.</span><span class="sxs-lookup"><span data-stu-id="6d28e-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-139">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6d28e-139">-Profile</span></span>
<span data-ttu-id="6d28e-140">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="6d28e-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6d28e-141">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6d28e-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6d28e-142">-ServerName</span></span>
<span data-ttu-id="6d28e-143">Especifica o nome do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="6d28e-143">Specifies the name of the database server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6d28e-144">-SubscriptionName</span></span>
<span data-ttu-id="6d28e-145">Especifica o nome da assinatura do Azure que este cmdlet usa para criar o contexto de conexão.</span><span class="sxs-lookup"><span data-stu-id="6d28e-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="6d28e-146">Se você não especificar um valor para esse parâmetro, o cmdlet usará a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6d28e-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="6d28e-147">Execute o Select-AzureSubscription cmdlet para alterar a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6d28e-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="6d28e-148">-UseSubscription</span></span>
<span data-ttu-id="6d28e-149">Indica que esse cmdlet usa a assinatura do Azure para criar o contexto de conexão.</span><span class="sxs-lookup"><span data-stu-id="6d28e-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d28e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d28e-150">CommonParameters</span></span>
<span data-ttu-id="6d28e-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d28e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d28e-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d28e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d28e-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="6d28e-153">INPUTS</span></span>

## <span data-ttu-id="6d28e-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="6d28e-154">OUTPUTS</span></span>

### <span data-ttu-id="6d28e-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="6d28e-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="6d28e-156">Notas</span><span class="sxs-lookup"><span data-stu-id="6d28e-156">NOTES</span></span>
* <span data-ttu-id="6d28e-157">Se você autenticar sem especificar um domínio e usar o Windows PowerShell 2.0, o cmdlet Get-Credential retornará uma invertida ( ) antes do nome de usuário, por \\ exemplo, \usuário.</span><span class="sxs-lookup"><span data-stu-id="6d28e-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="6d28e-158">O Windows PowerShell 3.0 não adiciona a faixa invertida.</span><span class="sxs-lookup"><span data-stu-id="6d28e-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="6d28e-159">Essa invertida não é  reconhecida pelo parâmetro Credencial do cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="6d28e-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="6d28e-160">Para removê-lo, use comandos semelhantes aos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6d28e-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="6d28e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d28e-161">RELATED LINKS</span></span>



[<span data-ttu-id="6d28e-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d28e-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="6d28e-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d28e-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="6d28e-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d28e-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="6d28e-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d28e-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


