---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 6cea7f2584de3a27be2cee36c3f32fd792564160
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260492"
---
# Add-AzKeyVaultKey

## Sinopse
Cria uma chave em um cofre de chaves ou importa uma chave para um cofre de chaves.

## SYNTAX

### InteractiveCreate (padrão)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

## DESCRITIVO
O cmdlet **Add-AzKeyVaultKey** cria uma chave em um cofre de chaves do Azure Key Vault ou importa uma chave para um cofre de chaves.
Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:
- Crie uma chave em um HSM (módulo de segurança de hardware) no serviço do cofre de chaves.
- Crie uma chave no software no serviço de compartimentação de chave.
- Importe uma chave do seu próprio HSM (módulo de segurança de hardware) para HSMs no serviço de compartimento de chave.
- Importar uma chave de um arquivo. pfx em seu computador.
- Importar uma chave de um arquivo. pfx no computador para módulos de segurança de hardware (HSMs) no serviço de cofre de chaves.
Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.
Se você criar ou importar uma chave com o mesmo nome de uma chave existente em seu cofre de chaves, a chave original será atualizada com os valores que você especificar para a nova chave. Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave. Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre chaves e segredos](http://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do cofre de chaves.
Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK. Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](http://go.microsoft.com/fwlink/?LinkId=522252).
Como prática recomendada, faça backup da chave após criá-la ou atualizá-la usando o cmdlet Backup-AzKeyVaultKey. Não há nenhuma funcionalidade de cantais exclusões, portanto, se você excluir acidentalmente a chave ou excluí-la e, em seguida, mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.

## EXEMPLOS

### Exemplo 1: criar uma chave
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

Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado contoso.

### Exemplo 2: criar uma chave protegida pelo HSM
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

Esse comando cria uma chave protegida pelo HSM no cofre de chaves chamado contoso.

### Exemplo 3: criar uma chave com valores não padrão
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

O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.
O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .
Esse objeto especifica um tempo dois anos no futuro. O comando armazena essa data na variável $Expires. Para obter mais informações, digite `Get-Help Get-Date` .
O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** . Esse objeto especifica a hora UTC atual. O comando armazena essa data na variável $NotBefore.
O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida pelo HSM. O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations. O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e. A nova chave está desativada. Você pode habilitá-lo usando o cmdlet **set-AzKeyVaultKey** .

### Exemplo 4: importar uma chave protegida pelo HSM
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

Esse comando importa a chave chamada ITByok do local que o parâmetro *keyFilePath* especifica. A chave importada é uma chave protegida pelo HSM.
Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.
Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](http://go.microsoft.com/fwlink/?LinkId=522252).

### Exemplo 5: importar uma chave protegida por software
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

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password. Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .
O segundo comando cria uma senha de software no cofre de chaves da contoso. O comando especifica o local para a chave e a senha armazenadas em $Password.

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

O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.
O segundo comando cria um objeto **DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires.
O terceiro comando cria a variável $tags para definir marcas para alta severidade e para isso.
O comando final importa uma chave como uma chave HSM do local especificado. O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenados $Password e aplica as marcas armazenadas em $tags.

### Exemplo 7: gerar uma chave de troca de chave (KEK) para "trazer seu próprio recurso de chave" (BYOK)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Gera uma chave (referida como chave de troca de chave (KEK)). O KEK deve ser uma chave RSA-HSM que tem apenas a operação de chave de importação. Somente a SKU do Key Vault Premium é compatível com as chaves RSA-HSM.
Para obter mais detalhes, consulte https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## OS

### -Curvename
Especifica o nome da curva da criptografia de curva elíptica, esse valor é válido quando KeyType é EC.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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
Especifica se a chave deve ser adicionada como uma chave protegida por software ou uma chave protegida pelo HSM no serviço do cofre de chaves.
Os valores válidos são: HSM e software.
Observação: para usar o HSM como destino, você deve ter um cofre de chaves com suporte para HSMs. Para obter mais informações sobre os níveis de serviço e os recursos do cofre de chaves do Azure, consulte o [site de preços do Azure Key Vault](http://go.microsoft.com/fwlink/?linkid=512521).
Esse parâmetro é necessário quando você cria uma nova chave. Se você importar uma chave usando o parâmetro *keyFilePath* , esse parâmetro será opcional:
- Se você não especificar esse parâmetro, e esse cmdlet importar uma chave que tenha extensão de nome de arquivo. byok, ele importa essa chave como uma chave protegida pelo HSM. O cmdlet não pode importar essa chave como chave protegida por software.
- Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tem uma extensão de nome de arquivo. pfx, ele importa a chave como uma chave protegida por software.

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
Nome do HSM. O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.

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
Especifica uma senha para o arquivo importado como um objeto **SecureString** . Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** . Para obter mais informações, digite `Get-Help ConvertTo-SecureString` . Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo. pfx.

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
Especifica o caminho de um arquivo local que contém o material da chave que este cmdlet importa.
As extensões de nome de arquivo válidas são. byok e. pfx.
- Se o arquivo for um arquivo. byok, a chave será automaticamente protegida por HSMs após a importação, e você não poderá substituir esse padrão.
- Se o arquivo for um arquivo. pfx, a chave será automaticamente protegida pelo software após a importação. Para substituir esse padrão, defina o parâmetro *Destination* como HSM para que a chave seja protegida pelo HSM.
Quando você especifica esse parâmetro, o parâmetro *Destination* é opcional.

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
Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.
Se você não especificar esse parâmetro, todas as operações poderão ser executadas.
Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela [especificação JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):
- com
- criptografá
- wrapKey
- unwrapKey
- designa
- verificar
- importar (apenas para KEK, consulte o exemplo 7)

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
Especifica o tipo de chave dessa chave.

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso do cofre.

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
Tamanho da chave RSA, em bits. Se não for especificado, o serviço fornecerá um padrão seguro.

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

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

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

### -Cofrename
Especifica o nome do cofre de chaves para o qual esse cmdlet adiciona a chave. Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVault

### System. String

## EXIBE

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey

## INFORMA

## LINKS RELACIONADOS

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-AzKeyVaultKeyAttribute](./Set-AzKeyVaultKeyAttribute.md)
