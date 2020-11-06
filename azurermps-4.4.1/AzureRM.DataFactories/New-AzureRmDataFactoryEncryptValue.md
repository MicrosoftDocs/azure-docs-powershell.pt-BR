---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryEncryptValue.md
ms.openlocfilehash: 54a759370f39dcd3844d42d858d23f6c178a4d08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602706"
---
# New-AzureRmDataFactoryEncryptValue

## Sinopse
Criptografa dados confidenciais.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByFactoryName (padrão)
```
New-AzureRmDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzureRmDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>]
 [[-GatewayName] <String>] [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmDataFactoryEncryptValue** criptografa dados confidenciais, como uma senha ou uma cadeia de conexão do Microsoft SQL Server, e retorna um valor criptografado.

## EXEMPLOS

### Exemplo 1: criptografar uma cadeia de conexão não ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzureRmDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

O primeiro comando usa o cmdlet ConvertTo-SecureString para converter a cadeia de conexão especificada em um objeto **SecureString** e armazena esse objeto na variável $value.
Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .
Valores permitidos: cadeia de conexão SQL Server ou Oracle.

O segundo comando cria um valor criptografado para o objeto armazenado em $Value para a fábrica de dados, o gateway, o grupo de recursos e o tipo de serviço vinculado especificado.

### Exemplo 2: criptografe uma cadeia de conexão não ODBC que usa a autenticação do Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catelog;Integrated Security=True' -AsPlainText -Force
```

O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de conexão especificada em um objeto de cadeia de caracteres seguro e armazena esse objeto na variável $value.

O segundo comando usa o cmdlet Get-Credential para coletar a autenticação do Windows (nome de usuário e a senha) e armazena esse objeto **PSCredential** na variável $Credential.
Para obter mais informações, digite `Get-Help Get-Credential` .

O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para a fábrica de dados, o gateway, o grupo de recursos e o tipo de serviço vinculado especificado.

### Exemplo 3: criptografar o nome do servidor e as credenciais do serviço vinculado ao sistema de arquivos
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzureRmDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

O primeiro comando usa **ConvertTo-SecureString** para converter a cadeia de caracteres especificada em uma cadeia de caracteres segura e, em seguida, armazena esse objeto na variável $value.

O segundo comando usa **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazena esse objeto **PSCredential** na variável $Credential.

O terceiro comando cria um valor criptografado para o objeto armazenado em $Value e $Credential para a fábrica de dados, o gateway, o grupo de recursos e o tipo de serviço vinculado especificado.

### Exemplo 4: criptografar credenciais para serviço do HDFS vinculado
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzureRmDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

O comando **ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.
O comando **novo objeto** cria um objeto PSCredential usando as cadeias de nome de usuário e senha seguras.
Em vez disso, você pode usar o comando **Get-Credential** para coletar a autenticação do Windows (nome de usuário e senha) e armazenar o objeto **PSCredential** retornado na variável $Credential conforme mostrado nos exemplos anteriores.

O comando **New-AzureRmDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado em $Credential para a fábrica de dados, o gateway, o grupo de recursos e o tipo de serviço vinculado especificado.

### Exemplo 5: criptografar credenciais para serviço ODBC vinculado
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzureRmDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

O comando **ConvertTo-SecureString** converte a cadeia de caracteres especificada em uma cadeia de caracteres segura.

O comando **New-AzureRmDataFactoryEncryptValue** cria um valor criptografado para o objeto armazenado em $Value para a fábrica de dados, o gateway, o grupo de recursos e o tipo de serviço vinculado especificado.

## OS

### -AuthenticationType
Especifica o tipo de autenticação a ser usado para conexão com a fonte de dados.
Os valores aceitáveis para esse parâmetro são:

- Windows
- Basic
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
Esse cmdlet criptografa os dados de credenciais que você especificar aqui.

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

### -Banco de dados
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

### -Datafactory
Especifica um objeto **PSDataFactory** .
Esse cmdlet criptografa os dados do alocador de dados que esse parâmetro especifica.

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

### -Datafactoryname
Especifica o nome de uma fábrica de dados.
Esse cmdlet criptografa os dados do alocador de dados que esse parâmetro especifica.

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

### -GATEWAYNAME
Especifica o nome do gateway.
Esse cmdlet criptografa os dados do gateway que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Noncredentialvalue
Especifica a parte sem credencial da cadeia de conexão ODBC (conectividade aberta de banco de dados).
Esse parâmetro é aplicável somente para o serviço ODBC vinculado.

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
Esse cmdlet criptografa os dados do grupo que esse parâmetro especifica.

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

### -Servidor
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

### -Digite
Especifica o tipo de serviço vinculado.
Esse cmdlet criptografa dados para o tipo de serviço vinculado que esse parâmetro especifica.
Os valores aceitáveis para esse parâmetro são:

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

### -Valor
Especifica o valor a ser criptografado.
Para um serviço do SQL Server local e um serviço vinculado do Oracle local, use uma cadeia de conexão.
Para um serviço de ODBC vinculado local, use a parte de credenciais da cadeia de conexão.
No serviço vinculado do sistema de arquivos no local, se o sistema de arquivos for local para o computador do gateway, use local ou localhost e se o sistema de arquivos estiver em um servidor diferente do computador do gateway, use o \\ \\ servername.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. String

## INFORMA
* Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas

## LINKS RELACIONADOS

[New-AzureRmDataFactoryEncryptValue](./New-AzureRmDataFactoryEncryptValue.md)


