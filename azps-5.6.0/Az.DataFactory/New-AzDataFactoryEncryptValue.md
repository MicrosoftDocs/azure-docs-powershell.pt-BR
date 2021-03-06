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
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Criptografa dados confidenciais.

## SINTAXE

### ByFactoryName (Padrão)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzDataFactoryEncryptValue** criptografa dados confidenciais, como uma senha ou uma cadeia de Microsoft SQL Server de conexão, e retorna um valor criptografado.

## EXEMPLOS

### Exemplo 1: criptografar uma cadeia de conexão não-ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

O primeiro comando usa o cmdlet ConvertTo-SecureString para converter a cadeia de caracteres de conexão especificada em **um objeto SecureString** e, em seguida, armazena esse objeto na variável $Value.
Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .
Valores permitidos: SQL Server ou cadeia de conexão Oracle.
O segundo comando cria um valor criptografado para o objeto armazenado no $Value para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.

### Exemplo 2: criptografar uma cadeia de conexão não ODBC que usa autenticação do Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de caracteres de conexão especificada em um objeto de cadeia de caracteres seguro e, em seguida, armazena esse objeto na variável $Value segurança.
O segundo comando usa o cmdlet Get-Credential para coletar a autenticação do windows (nome de usuário e senha) e armazena esse objeto **PSCredential** na variável $Credential.
Para obter mais informações, digite `Get-Help Get-Credential` .
O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.

### Exemplo 3: criptografar o nome do servidor e as credenciais do serviço vinculado ao sistema de arquivos
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de caracteres especificada em uma cadeia de caracteres segura e armazena esse objeto na variável $Value.
O segundo comando usa **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazena esse objeto **PSCredential** na variável $Credential.
O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.

### Exemplo 4: criptografar credenciais para serviço vinculado HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

O **comando ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.
O **comando New-Object** cria um objeto PSCredential usando as cadeias de caracteres de nome de usuário e senha seguras.
Em vez disso, você pode usar o comando **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazenar o objeto **PSCredential** retornado na variável $credential como mostrado em exemplos anteriores.
O **comando New-AzDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado no $Credential para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.

### Exemplo 5: criptografar credenciais para o serviço vinculado ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

O **comando ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.
O **comando New-AzDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado no $Value para o fábrica de dados especificado, gateway, grupo de recursos e tipo de serviço vinculado.

## PARÂMETROS

### -AuthenticationType
Especifica o tipo de autenticação a ser usada para se conectar à fonte de dados.
Os valores aceitáveis para este parâmetro são:
- Windows
- Básico
- Anônimo.

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

### -Credential
Especifica as credenciais de autenticação do Windows (nome de usuário e senha) a serem usadas.
Este cmdlet criptografa os dados de credenciais especificados aqui.

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

### -Database
Especifica o nome do banco de dados do serviço vinculado.

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

### -DataFactory
Especifica um **objeto PSDataFactory.**
Este cmdlet criptografa dados para o fábrica de dados especificado por esse parâmetro.

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

### -DataFactoryName
Especifica o nome de uma fábrica de dados.
Este cmdlet criptografa dados para o fábrica de dados especificado por esse parâmetro.

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

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -GatewayName
Especifica o nome do gateway.
Este cmdlet criptografa dados para o gateway especificado por esse parâmetro.

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

### -NonCredentialValue
Especifica a parte não credencial da cadeia de conexão ODBC (Open Database Connectivity).
Esse parâmetro só é aplicável para o serviço vinculado ODBC.

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

### -ResourceGroupName
Especifica o nome de um grupo de recursos do Azure.
Este cmdlet criptografa dados para o grupo especificado por esse parâmetro.

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

### -Server
Especifica o nome do servidor do serviço vinculado.

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

### -Type
Especifica o tipo de serviço vinculado.
Este cmdlet criptografa dados para o tipo de serviço vinculado especificado por esse parâmetro.
Os valores aceitáveis para este parâmetro são:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

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

### -Value
Especifica o valor a ser criptografado.
Para um serviço SQL Server vinculado local e um serviço vinculado à Oracle local, use uma cadeia de caracteres de conexão.
Para um serviço ODBC local vinculado, use a parte de credencial da cadeia de caracteres de conexão.
Para o serviço vinculado ao sistema de arquivos local, se o sistema de arquivos for local para o computador gateway, use Local ou localhost e se o sistema de arquivos estiver em um servidor diferente do computador gateway, use \\ \\ servername.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## SAÍDAS

### System.String

## NOTES
* Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories

## LINKS RELACIONADOS

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


