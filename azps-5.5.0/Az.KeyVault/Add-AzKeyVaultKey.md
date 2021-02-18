---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405390"
---
# Add-AzKeyVaultKey

## Sinopse
Cria uma chave em um cofre de chave ou importa uma chave para um cofre de chave.

## Sintaxe

### InteractiveCreate (Padrão)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Add-AzKeyVaultKey** cria uma chave em um cofre de chave no Cofre de Teclas do Azure ou importa uma chave para um cofre de chave.
Use este cmdlet para adicionar teclas usando qualquer um dos seguintes métodos:
- Crie uma chave em um módulo de segurança de hardware (HSM) no serviço Cofre de Teclas.
- Crie uma chave no software no serviço Cofre de Chave.
- Importe uma chave do seu próprio módulo de segurança de hardware (HSM) para HSMs no serviço Cofre de Teclas.
- Importe uma chave de um arquivo .pfx no computador.
- Importe uma chave de um arquivo .pfx no seu computador para módulos de segurança de hardware (HSMs) no serviço Cofre de Teclas.
Para qualquer uma dessas operações, você pode fornecer atributos principais ou aceitar configurações padrão.
Se você criar ou importar uma chave com o mesmo nome de uma chave existente no seu cofre de chaves, a chave original será atualizada com os valores especificados para a nova chave. Você pode acessar os valores anteriores usando o URI específico de versão para essa versão da chave. Para saber mais sobre as principais versões e a estrutura do URI, consulte [Sobre](http://go.microsoft.com/fwlink/?linkid=518560) Chaves e Segredos na documentação da API REST do Cofre de Chaves.
Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo .byok) usando o conjunto de ferramentas BYOK do Azure Key Vault. Para obter mais informações, consulte Como gerar e transferir HSM-Protected chaves do Cofre de Teclas [do Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)
Como prática ideal, fazer o back up da chave depois que ela for criada ou atualizada usando o cmdlet Backup-AzKeyVaultKey usuário. Não há funcionalidade de preenchimento indefinível, portanto, se você excluir acidentalmente sua chave ou excluí-la e mudar de ideia, a chave não poderá ser recuperada, a menos que você tenha um backup dela que possa restaurar.

## Exemplos

### Exemplo 1: Criar uma chave
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado Contoso.

### Exemplo 2: Criar uma chave protegida por HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Esse comando cria uma chave protegida por HSM no cofre de chaves chamado Contoso.

### Exemplo 3: Criar uma chave com valores não padrão
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

O primeiro comando armazena os valores descriptografar e verificar na variável $KeyOperations dados.
O segundo comando cria um **objeto DateTime,** definido em UTC, usando o cmdlet **Get-Date.**
Esse objeto especifica um período de dois anos no futuro. O comando armazena essa data na variável $Expires dados. Para obter mais informações, digite `Get-Help Get-Date` .
O terceiro comando cria um **objeto DateTime** usando o cmdlet **Get-Date.** Esse objeto especifica a hora UTC atual. O comando armazena essa data na variável $NotBefore dados.
O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida por HSM. O comando especifica valores para operações de teclas permitidas armazenadas $KeyOperations. O comando especifica horas para os *parâmetros Expires* e *NotBefore* criados nos comandos anteriores e marcas para alta gravidade e IT. A nova chave está desabilitada. Você pode habilita-lo usando **o cmdlet Set-AzKeyVaultKey.**

### Exemplo 4: Importar uma chave protegida por HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Esse comando importa a chave chamada ITByok do local especificado pelo parâmetro *KeyFilePath.* A chave importada é uma chave protegida por HSM.
Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo .byok) usando o conjunto de ferramentas BYOK do Cofre de Teclas do Azure.
Para obter mais informações, consulte Como gerar e transferir HSM-Protected chaves do Cofre de Teclas [do Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)

### Exemplo 5: Importar uma chave protegida por software
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Password. Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .
O segundo comando cria uma senha de software no cofre de teclas contoso. O comando especifica o local da chave e a senha armazenadas $Password.

### Exemplo 6: importar uma chave e atribuir atributos
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Password.
O segundo comando cria um **objeto DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires dados.
O terceiro comando cria a $tags variável para definir marcas para alta gravidade e IT.
O comando final importa uma chave como uma tecla HSM do local especificado. O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenadas no $Password e aplica as marcas armazenadas no $tags.

### Exemplo 7: Gerar uma chave do exchange (KEK) para o recurso "traga sua própria chave" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Gera uma chave (chamada de chave do exchange (KEK)). O KEK deve ser uma chave RSA-HSM que tenha apenas a operação de chave de importação. Somente a SKU Premium do Cofre de Teclas é compatível com as teclas RSA-HSM.
Para obter mais detalhes, consulte https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## Parâmetros

### -CurveName
Especifica o nome da curva da criptografia de curva elíptica, esse valor é válido quando KeyType é EC.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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

### -Destino
Especifica se você deve adicionar a chave como uma chave protegida por software ou uma chave protegida por HSM no serviço do Cofre de Teclas.
Os valores válidos são: HSM e Software.
Observação: para usar o HSM como seu destino, você deve ter um cofre de chave compatível com HSMs. Para obter mais informações sobre os níveis de serviço e os recursos do Cofre de Teclas do Azure, consulte o site de preços do Cofre de Chave do [Azure.](http://go.microsoft.com/fwlink/?linkid=512521)
Esse parâmetro é necessário quando você cria uma nova chave. Se você importar uma chave usando o parâmetro *KeyFilePath,* este parâmetro será opcional:
- Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tenha a extensão de nome de arquivo .byok, ela será importada como uma chave protegida por HSM. O cmdlet não pode importar essa chave como chave protegida por software.
- Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tenha uma extensão de nome de arquivo .pfx, ele importa a chave como uma chave protegida por software.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Desabilitar
Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado. Qualquer tentativa de usar a chave falhará. Use este parâmetro se você estiver pré-carregar as teclas que pretende habilitar mais tarde.

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

### -Expira
Especifica o tempo de expiração, como um objeto **DateTime,** para a chave que este cmdlet adiciona. Este parâmetro usa o Tempo Universal Coordenado (UTC). Para obter um **objeto DateTime,** use o cmdlet **Get-Date.** Para obter mais informações, digite `Get-Help Get-Date` . Se você não especificar esse parâmetro, a chave não expirará.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
Nome HSM. O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
Objeto HSM.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
ID do recurso do HSM.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Objeto do cofre.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Especifica uma senha para o arquivo importado como um objeto **SecureString.** Para obter um **objeto SecureString,** use o cmdlet **ConvertTo-SecureString.** Para obter mais informações, digite `Get-Help ConvertTo-SecureString` . Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo .pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Especifica o caminho de um arquivo local que contém material-chave que este cmdlet importa.
As extensões de nome de arquivo válidas são .byok e .pfx.
- Se o arquivo for um arquivo .byok, a chave será protegida automaticamente por HSMs após a importação e você não poderá substituir esse padrão.
- Se o arquivo for um arquivo .pfx, a chave será protegida automaticamente pelo software após a importação. Para substituir esse padrão, de definir *o* parâmetro Destino como HSM para que a chave seja protegida por HSM.
Quando você especifica esse parâmetro, o *parâmetro* Destino é opcional.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Especifica uma matriz de operações que pode ser executada usando a chave que este cmdlet adiciona.
Se você não especificar esse parâmetro, todas as operações poderão ser executadas.
Os valores aceitáveis para este parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela especificação [JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):
- Criptografar
- Descriptografar
- wrapKey
- unwrapKey
- Sinal
- Verificar
- importar (somente para KEK, consulte o exemplo 7)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Especifica o tipo de chave dessa chave. Ao importar teclas BYOK, ela é padrão para 'RSA'.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da chave a ser adicionar ao cofre de chaves. Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome especificado por esse parâmetro, o nome do cofre de chave e seu ambiente atual. O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com apenas 0 a 9, a-z, A-Z e - (o símbolo de traço).

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

### -NotBefore
Especifica a hora, como um objeto **DateTime,** antes do qual a chave não pode ser usada. Este parâmetro usa UTC. Para obter um **objeto DateTime,** use o cmdlet **Get-Date.** Se você não especificar esse parâmetro, a chave poderá ser usada imediatamente.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do Recurso do Cofre.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tamanho
Tamanho da tecla RSA, em bits. Se não especificado, o serviço fornecerá um padrão seguro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Pares de valor-chave na forma de uma tabela hash. Por exemplo: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nomedo Cofre
Especifica o nome do cofre de chave ao qual este cmdlet adiciona a chave. Este cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
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

### -WhatIf
Mostra o que acontece se o cmdlet for executado.
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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## Saídas

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## Notas

## LINKS RELACIONADOS

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

