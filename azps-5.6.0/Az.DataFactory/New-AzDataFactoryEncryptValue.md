---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 9a1f2bac984b4cad5267775dcbe59e79ed0eb677
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888258"
---
# <span data-ttu-id="49a9a-101">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="49a9a-101">New-AzDataFactoryEncryptValue</span></span>

## <span data-ttu-id="49a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="49a9a-103">Criptografa dados confidenciais.</span><span class="sxs-lookup"><span data-stu-id="49a9a-103">Encrypts sensitive data.</span></span>

## <span data-ttu-id="49a9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="49a9a-104">SYNTAX</span></span>

### <span data-ttu-id="49a9a-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49a9a-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a9a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="49a9a-106">ByFactoryObject</span></span>
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a9a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="49a9a-107">DESCRIPTION</span></span>
<span data-ttu-id="49a9a-108">O cmdlet **New-AzDataFactoryEncryptValue** criptografa dados confidenciais, como uma senha ou uma cadeia de Microsoft SQL Server de conexão, e retorna um valor criptografado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-108">The **New-AzDataFactoryEncryptValue** cmdlet encrypts sensitive data, such as a password or a Microsoft SQL Server connection string, and returns an encrypted value.</span></span>

## <span data-ttu-id="49a9a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49a9a-109">EXAMPLES</span></span>

### <span data-ttu-id="49a9a-110">Exemplo 1: criptografar uma cadeia de conexão não-ODBC</span><span class="sxs-lookup"><span data-stu-id="49a9a-110">Example 1: Encrypt a non-ODBC connection string</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

<span data-ttu-id="49a9a-111">O primeiro comando usa o cmdlet ConvertTo-SecureString para converter a cadeia de caracteres de conexão especificada em **um objeto SecureString** e, em seguida, armazena esse objeto na variável $Value.</span><span class="sxs-lookup"><span data-stu-id="49a9a-111">The first command uses the ConvertTo-SecureString cmdlet to convert the specified connection string to a **SecureString** object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="49a9a-112">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="49a9a-112">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="49a9a-113">Valores permitidos: SQL Server ou cadeia de conexão Oracle.</span><span class="sxs-lookup"><span data-stu-id="49a9a-113">Allowed values: SQL Server or Oracle connection string.</span></span>
<span data-ttu-id="49a9a-114">O segundo comando cria um valor criptografado para o objeto armazenado no $Value para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-114">The second command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="49a9a-115">Exemplo 2: criptografar uma cadeia de conexão não ODBC que usa autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="49a9a-115">Example 2: Encrypt a non-ODBC connection string that uses Windows authentication.</span></span>
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

<span data-ttu-id="49a9a-116">O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de caracteres de conexão especificada em um objeto de cadeia de caracteres seguro e, em seguida, armazena esse objeto na variável $Value segurança.</span><span class="sxs-lookup"><span data-stu-id="49a9a-116">The first command uses **ConvertTo-SecureString** to convert the specified connection string to a secure string object, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="49a9a-117">O segundo comando usa o cmdlet Get-Credential para coletar a autenticação do windows (nome de usuário e senha) e armazena esse objeto **PSCredential** na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="49a9a-117">The second command uses the Get-Credential cmdlet to collect the windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="49a9a-118">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="49a9a-118">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="49a9a-119">O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-119">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="49a9a-120">Exemplo 3: criptografar o nome do servidor e as credenciais do serviço vinculado ao sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="49a9a-120">Example 3: Encrypt server name and credentials for File system linked service</span></span>
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

<span data-ttu-id="49a9a-121">O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de caracteres especificada em uma cadeia de caracteres segura e armazena esse objeto na variável $Value.</span><span class="sxs-lookup"><span data-stu-id="49a9a-121">The first command uses **ConvertTo-SecureString** to convert the specified string to a secure string, and then stores that object in the $Value variable.</span></span>
<span data-ttu-id="49a9a-122">O segundo comando usa **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazena esse objeto **PSCredential** na variável $Credential.</span><span class="sxs-lookup"><span data-stu-id="49a9a-122">The second command uses **Get-Credential** to collect the Windows authentication (user name and password), and then stores that **PSCredential** object in the $Credential variable.</span></span>
<span data-ttu-id="49a9a-123">O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-123">The third command creates an encrypted value for the object stored in $Value and $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="49a9a-124">Exemplo 4: criptografar credenciais para serviço vinculado HDFS</span><span class="sxs-lookup"><span data-stu-id="49a9a-124">Example 4: Encrypt credentials for HDFS linked service</span></span>
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

<span data-ttu-id="49a9a-125">O **comando ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="49a9a-125">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="49a9a-126">O **comando New-Object** cria um objeto PSCredential usando as cadeias de caracteres de nome de usuário e senha seguras.</span><span class="sxs-lookup"><span data-stu-id="49a9a-126">The **New-Object** command creates a PSCredential object using the secure username and password strings.</span></span>
<span data-ttu-id="49a9a-127">Em vez disso, você pode usar o comando **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazenar o objeto **PSCredential** retornado na variável $credential como mostrado em exemplos anteriores.</span><span class="sxs-lookup"><span data-stu-id="49a9a-127">Instead, you could use the **Get-Credential** command to collect Windows authentication (user name and password), and then store the returned **PSCredential** object in the $credential variable as shown in previous examples.</span></span>
<span data-ttu-id="49a9a-128">O **comando New-AzDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado no $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-128">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Credential for the specified data factory, gateway, resource group, and linked service type.</span></span>

### <span data-ttu-id="49a9a-129">Exemplo 5: criptografar credenciais para o serviço vinculado ODBC</span><span class="sxs-lookup"><span data-stu-id="49a9a-129">Example 5: Encrypt credentials for ODBC linked service</span></span>
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

<span data-ttu-id="49a9a-130">O **comando ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.</span><span class="sxs-lookup"><span data-stu-id="49a9a-130">The **ConvertTo-SecureString** command converts the specified string to a secure string.</span></span>
<span data-ttu-id="49a9a-131">O **comando New-AzDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado no $Value para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-131">The **New-AzDataFactoryEncryptValue** command creates an encrypted value for the object stored in $Value for the specified data factory, gateway, resource group, and linked service type.</span></span>

## <span data-ttu-id="49a9a-132">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="49a9a-132">PARAMETERS</span></span>

### <span data-ttu-id="49a9a-133">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="49a9a-133">-AuthenticationType</span></span>
<span data-ttu-id="49a9a-134">Especifica o tipo de autenticação a ser usada para se conectar à fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="49a9a-134">Specifies the type of authentication to be used to connect to the data source.</span></span>
<span data-ttu-id="49a9a-135">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="49a9a-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a9a-136">Windows</span><span class="sxs-lookup"><span data-stu-id="49a9a-136">Windows</span></span>
- <span data-ttu-id="49a9a-137">Básico</span><span class="sxs-lookup"><span data-stu-id="49a9a-137">Basic</span></span>
- <span data-ttu-id="49a9a-138">Anônimo.</span><span class="sxs-lookup"><span data-stu-id="49a9a-138">Anonymous.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-139">-Credential</span><span class="sxs-lookup"><span data-stu-id="49a9a-139">-Credential</span></span>
<span data-ttu-id="49a9a-140">Especifica as credenciais de autenticação do Windows (nome de usuário e senha) a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="49a9a-140">Specifies the Windows authentication credentials (user name and password) to be used.</span></span>
<span data-ttu-id="49a9a-141">Este cmdlet criptografa os dados de credenciais especificados aqui.</span><span class="sxs-lookup"><span data-stu-id="49a9a-141">This cmdlet encrypts the credential data you specify here.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-142">-Database</span><span class="sxs-lookup"><span data-stu-id="49a9a-142">-Database</span></span>
<span data-ttu-id="49a9a-143">Especifica o nome do banco de dados do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-143">Specifies the database name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-144">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="49a9a-144">-DataFactory</span></span>
<span data-ttu-id="49a9a-145">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="49a9a-145">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="49a9a-146">Este cmdlet criptografa dados para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49a9a-146">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-147">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="49a9a-147">-DataFactoryName</span></span>
<span data-ttu-id="49a9a-148">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="49a9a-148">Specifies the name of a data factory.</span></span>
<span data-ttu-id="49a9a-149">Este cmdlet criptografa dados para o fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49a9a-149">This cmdlet encrypts data for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a9a-150">-DefaultProfile</span></span>
<span data-ttu-id="49a9a-151">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="49a9a-151">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-152">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="49a9a-152">-GatewayName</span></span>
<span data-ttu-id="49a9a-153">Especifica o nome do gateway.</span><span class="sxs-lookup"><span data-stu-id="49a9a-153">Specifies the name of the gateway.</span></span>
<span data-ttu-id="49a9a-154">Este cmdlet criptografa dados para o gateway especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49a9a-154">This cmdlet encrypts data for the gateway that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-155">-NonCredentialValue</span><span class="sxs-lookup"><span data-stu-id="49a9a-155">-NonCredentialValue</span></span>
<span data-ttu-id="49a9a-156">Especifica a parte não credencial da cadeia de conexão ODBC (Open Database Connectivity).</span><span class="sxs-lookup"><span data-stu-id="49a9a-156">Specifies the non-credential part of the Open Database Connectivity (ODBC) connection string.</span></span>
<span data-ttu-id="49a9a-157">Esse parâmetro só é aplicável para o serviço vinculado ODBC.</span><span class="sxs-lookup"><span data-stu-id="49a9a-157">This parameter is applicable only for the ODBC linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a9a-158">-ResourceGroupName</span></span>
<span data-ttu-id="49a9a-159">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="49a9a-159">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="49a9a-160">Este cmdlet criptografa dados para o grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49a9a-160">This cmdlet encrypts data for the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-161">-Server</span><span class="sxs-lookup"><span data-stu-id="49a9a-161">-Server</span></span>
<span data-ttu-id="49a9a-162">Especifica o nome do servidor do serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-162">Specifies the server name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-163">-Type</span><span class="sxs-lookup"><span data-stu-id="49a9a-163">-Type</span></span>
<span data-ttu-id="49a9a-164">Especifica o tipo de serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-164">Specifies the linked service type.</span></span>
<span data-ttu-id="49a9a-165">Este cmdlet criptografa dados para o tipo de serviço vinculado especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="49a9a-165">This cmdlet encrypts data for the linked service type that this parameter specifies.</span></span>
<span data-ttu-id="49a9a-166">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="49a9a-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a9a-167">OnPremisesSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-167">OnPremisesSqlLinkedService</span></span> 
- <span data-ttu-id="49a9a-168">OnPremisesFileSystemLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-168">OnPremisesFileSystemLinkedService</span></span> 
- <span data-ttu-id="49a9a-169">OnPremisesOracleLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-169">OnPremisesOracleLinkedService</span></span> 
- <span data-ttu-id="49a9a-170">OnPremisesOdbcLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-170">OnPremisesOdbcLinkedService</span></span> 
- <span data-ttu-id="49a9a-171">OnPremisesPostgreSqlLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-171">OnPremisesPostgreSqlLinkedService</span></span> 
- <span data-ttu-id="49a9a-172">OnPremisesTeradataLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-172">OnPremisesTeradataLinkedService</span></span> 
- <span data-ttu-id="49a9a-173">OnPremisesMySQLLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-173">OnPremisesMySQLLinkedService</span></span> 
- <span data-ttu-id="49a9a-174">OnPremisesDB2LinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-174">OnPremisesDB2LinkedService</span></span> 
- <span data-ttu-id="49a9a-175">OnPremisesSybaseLinkedService</span><span class="sxs-lookup"><span data-stu-id="49a9a-175">OnPremisesSybaseLinkedService</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-176">-Value</span><span class="sxs-lookup"><span data-stu-id="49a9a-176">-Value</span></span>
<span data-ttu-id="49a9a-177">Especifica o valor a ser criptografado.</span><span class="sxs-lookup"><span data-stu-id="49a9a-177">Specifies the value to encrypt.</span></span>
<span data-ttu-id="49a9a-178">Para um serviço SQL Server vinculado local e um serviço vinculado à Oracle local, use uma cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="49a9a-178">For an on-premises SQL Server linked service and an on-premises Oracle linked service, use a connection string.</span></span>
<span data-ttu-id="49a9a-179">Para um serviço ODBC local vinculado, use a parte de credencial da cadeia de caracteres de conexão.</span><span class="sxs-lookup"><span data-stu-id="49a9a-179">For an on-premises ODBC linked service, use the credential part of the connection string.</span></span>
<span data-ttu-id="49a9a-180">Para o serviço vinculado ao sistema de arquivos local, se o sistema de arquivos for local para o computador gateway, use Local ou localhost e se o sistema de arquivos estiver em um servidor diferente do computador gateway, use \\ \\ servername.</span><span class="sxs-lookup"><span data-stu-id="49a9a-180">For on premises file system linked service, if the file system is local to the gateway computer, use Local or localhost, and if the file system is on a server different from the gateway computer, use \\\\servername.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a9a-181">CommonParameters</span></span>
<span data-ttu-id="49a9a-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a9a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a9a-183">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a9a-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a9a-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49a9a-184">INPUTS</span></span>

### <span data-ttu-id="49a9a-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="49a9a-185">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="49a9a-186">System.String</span><span class="sxs-lookup"><span data-stu-id="49a9a-186">System.String</span></span>

## <span data-ttu-id="49a9a-187">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="49a9a-187">OUTPUTS</span></span>

### <span data-ttu-id="49a9a-188">System.String</span><span class="sxs-lookup"><span data-stu-id="49a9a-188">System.String</span></span>

## <span data-ttu-id="49a9a-189">NOTES</span><span class="sxs-lookup"><span data-stu-id="49a9a-189">NOTES</span></span>
* <span data-ttu-id="49a9a-190">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="49a9a-190">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="49a9a-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49a9a-191">RELATED LINKS</span></span>

[<span data-ttu-id="49a9a-192">New-AzDataFactoryEncryptValue</span><span class="sxs-lookup"><span data-stu-id="49a9a-192">New-AzDataFactoryEncryptValue</span></span>](./New-AzDataFactoryEncryptValue.md)


