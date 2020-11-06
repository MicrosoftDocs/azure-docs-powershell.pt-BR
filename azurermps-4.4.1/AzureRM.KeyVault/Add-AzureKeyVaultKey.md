---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://go.microsoft.com/fwlink/?LinkId=690295
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 0046a1ed2b2580d1cafbdaa31d9fad53a09ea644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441553"
---
# Add-AzureKeyVaultKey

## Sinopse
Cria uma chave em um cofre de chaves ou importa uma chave para um cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Criar (padrão)
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Importações
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureKeyVaultKey** cria uma chave em um cofre de chaves do Azure Key Vault ou importa uma chave para um cofre de chaves.
Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:

- Crie uma chave em um HSM (módulo de segurança de hardware) no serviço do cofre de chaves.
- Crie uma chave no software no serviço de compartimentação de chave.
- Importe uma chave do seu próprio HSM (módulo de segurança de hardware) para HSMs no serviço de compartimento de chave.
- Importar uma chave de um arquivo. pfx em seu computador.
- Importar uma chave de um arquivo. pfx no computador para módulos de segurança de hardware (HSMs) no serviço de cofre de chaves.

Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.

Se você criar ou importar uma chave com o mesmo nome de uma chave existente em seu cofre de chaves, a chave original será atualizada com os valores que você especificar para a nova chave. Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave. Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre as chaves andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do cofre de chaves.

Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK. Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).

Como prática recomendada, faça backup da chave após criá-la ou atualizá-la usando o cmdlet Backup-AzureKeyVaultKey. Não há nenhuma funcionalidade de cantais exclusões, portanto, se você excluir acidentalmente a chave ou excluí-la e, em seguida, mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.

## EXEMPLOS

### Exemplo 1: criar uma chave
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado contoso.

### Exemplo 2: criar uma chave protegida pelo HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

Esse comando cria uma chave protegida pelo HSM no cofre de chaves chamado contoso.

### Exemplo 3: criar uma chave com valores não padrão
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.

O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .
Esse objeto especifica um tempo dois anos no futuro. O comando armazena essa data na variável $Expires. Para obter mais informações, digite `Get-Help Get-Date` .

O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** . Esse objeto especifica a hora UTC atual. O comando armazena essa data na variável $NotBefore.

O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida pelo HSM. O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations. O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e. A nova chave está desativada. Você pode habilitá-lo usando o cmdlet **set-AzureKeyVaultKey** .

### Exemplo 4: importar uma chave protegida pelo HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

Esse comando importa a chave chamada ITByok do local que o parâmetro *keyFilePath* especifica. A chave importada é uma chave protegida pelo HSM.

Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.
Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).

### Exemplo 5: importar uma chave protegida por software
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password. Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .

O segundo comando cria uma senha de software no cofre de chaves da contoso. O comando especifica o local para a chave e a senha armazenadas em $Password.

### Exemplo 6: importar uma chave e atribuir atributos
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.

O segundo comando cria um objeto **DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires.

O terceiro comando cria a variável $tags para definir marcas para alta severidade e para isso.

O comando final importa uma chave como uma chave HSM do local especificado. O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenados $Password e aplica as marcas armazenadas em $tags.

## OS

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Destino
Especifica se a chave deve ser adicionada como uma chave protegida por software ou uma chave protegida pelo HSM no serviço do cofre de chaves.
Os valores válidos são: HSM e software.

Observação: para usar o HSM como destino, você deve ter um cofre de chaves com suporte para HSMs. Para obter mais informações sobre os níveis de serviço e os recursos do cofre de chaves do Azure, consulte o [site de preços do Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).

Esse parâmetro é necessário quando você cria uma nova chave. Se você importar uma chave usando o parâmetro *keyFilePath* , esse parâmetro será opcional:

- Se você não especificar esse parâmetro, e esse cmdlet importar uma chave que tenha extensão de nome de arquivo. byok, ele importa essa chave como uma chave protegida pelo HSM. O cmdlet não pode importar essa chave como chave protegida por software.

- Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tem uma extensão de nome de arquivo. pfx, ele importa a chave como uma chave protegida por software.

```yaml
Type: System.String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado. Qualquer tentativa de usar a chave irá falhar. Use esse parâmetro se você estiver precarregando chaves que pretende habilitar mais tarde.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expira em
Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que esse cmdlet adiciona. Esse parâmetro usa o tempo universal coordenado (UTC). Para obter um objeto **DateTime** , use o cmdlet **Get-Date** . Para obter mais informações, digite `Get-Help Get-Date` . Se você não especificar esse parâmetro, a chave não expira.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyFilePassword
Especifica uma senha para o arquivo importado como um objeto **SecureString** . Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** . Para obter mais informações, digite `Get-Help ConvertTo-SecureString` . Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo. pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Especifica o caminho de um arquivo local que contém o material da chave que este cmdlet importa.
As extensões de nome de arquivo válidas são. byok e. pfx.

- Se o arquivo for um arquivo. byok, a chave será automaticamente protegida por HSMs após a importação, e você não poderá substituir esse padrão.

- Se o arquivo for um arquivo. pfx, a chave será automaticamente protegida pelo software após a importação. Para substituir esse padrão, defina o parâmetro *Destination* como HSM para que a chave seja protegida pelo HSM.

Quando você especifica esse parâmetro, o parâmetro *Destination* é opcional.

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.
Se você não especificar esse parâmetro, todas as operações poderão ser executadas.

Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela [especificação JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):

- Com
- Criptografá
- Quebrada
- Desenvolva
- Designa
- Verificar
- Fazer
- Restaurar

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da chave a ser adicionada ao cofre de chaves. Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual. O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com tamanho que contenha apenas 0-9, a-z, A-Z e-(o símbolo de traço).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Não antes
Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada. Esse parâmetro usa UTC. Para obter um objeto **DateTime** , use o cmdlet **Get-Date** . Se você não especificar esse parâmetro, a chave pode ser usada imediatamente.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves para o qual esse cmdlet adiciona a chave. Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
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

### Microsoft. Azure. Commands. keyvault. Models. keybundle

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)
