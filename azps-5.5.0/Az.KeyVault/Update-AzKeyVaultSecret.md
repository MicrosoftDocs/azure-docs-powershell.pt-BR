---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113058"
---
# Update-AzKeyVaultSecret

## Sinopse
Atualiza os atributos de um segredo em um cofre de chaves.

## Sintaxe

### Padrão (Padrão)
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobject
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Update-AzKeyVaultSec ltd atualiza** os atributos editáveis de um segredo em um cofre de chave.

## Exemplos

### Exemplo 1: modificar os atributos de um segredo
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

Os quatro primeiros comandos definem atributos para a data de vencimento, a data de NotBefore, as marcas e o tipo de contexto, e armazenam os atributos em variáveis.
O comando final modifica os atributos do segredo CHAMADO RH no cofre de chaves chamado ContosoVault, usando as variáveis armazenadas.

### Exemplo 2: Excluir as marcas e o tipo de conteúdo de um segredo
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Esse comando exclui as marcas e o tipo de conteúdo para a versão especificada do segredo CHAMADO RH no cofre de chaves chamado Contoso.

### Exemplo 3: Desabilitar a versão atual dos segredos cujo nome começa com a INFORMAÇÃO
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

O primeiro comando armazena o valor da cadeia de caracteres Contoso na $Vault variável.
O segundo comando armazena o valor da cadeia de caracteres IT na variável $Prefix dados.
O terceiro comando usa o cmdlet Get-AzKeyVaultSecret para obter os segredos no cofre de teclas especificado e passa esses segredos para o cmdlet **Where-Object.** O **cmdlet Where-Object** filtra os segredos dos nomes que começam com os caracteres IT. O comando filtra os segredos que combinam o filtro com o Update-AzKeyVaultSecret cmdlet, o que os desabilita.

### Exemplo 4: Definir o ContentType para todas as versões de um segredo
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

Os três primeiros comandos definem variáveis de cadeia de caracteres a ser usadas para os parâmetros *VaultName,* *Name* e *ContentType.* O quarto comando usa o cmdlet Get-AzKeyVaultKey para obter as teclas especificadas e coloca as teclas no cmdlet Update-AzKeyVaultSecret para definir seu tipo de conteúdo como XML.

## Parâmetros

### -ContentType
Tipo de conteúdo do Secret.
Se não especificado, o valor existente do tipo de conteúdo do segredo permanecerá inalterado.
Remova o valor de tipo de conteúdo existente especificando uma cadeia de caracteres vazia.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -Habilitar
Se estiver presente, habilita um segredo se o valor for verdadeiro.
Desabilitar um segredo se o valor for falso.
Se não especificado, o valor existente do estado habilitado/desabilitado do segredo permanecerá inalterado.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expira
O tempo de expiração de um segredo no horário UTC.
Se não especificado, o valor existente do tempo de expiração do segredo permanecerá inalterado.

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

### -InputObject
Objeto secreto

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome secreto.
O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
O horário UTC antes de qual segredo não pode ser usado.
Se não especificado, o valor existente do atributo NotBefore do segredo permanecerá inalterado.

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

### -PassThru
O Cmdlet não retorna objeto por padrão.
Se essa opção for especificada, retorne o objeto Secret.

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

### -Tag
Uma tabela hash que representa marcas secretas.
Se não especificado, as marcas existentes do segredo permanecerão inalteradas.
Remova uma marca especificando uma Hashtable vazia.

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
Nome do cofre.
O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Versão
Versão secreta.
O Cmdlet constrói o FQDN de um segredo do nome do cofre, ambiente atualmente selecionado, nome secreto e versão secreta.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecibleIdentityItem

## Saídas

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSec cue

## Notas

## LINKS RELACIONADOS
