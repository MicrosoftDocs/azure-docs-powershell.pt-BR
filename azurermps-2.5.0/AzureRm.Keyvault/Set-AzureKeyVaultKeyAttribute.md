---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785928"
---
# Set-AzureKeyVaultKeyAttribute

## Sinopse
Atualiza os atributos de uma chave em um cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureKeyVaultKeyAttribute** atualiza os atributos editáveis de uma chave em um cofre de chaves.

## EXEMPLOS

### Exemplo 1: modificar uma chave para habilitá-la e definir a data de expiração e as marcas
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

O primeiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** . Esse objeto especifica um tempo dois anos no futuro. O comando armazena essa data na variável $Expires.
Para obter mais informações, digite `Get-Help Get-Date` .

O segundo comando cria uma variável para armazenar valores de marca de alta gravidade e contabilidade.

O comando final modifica uma chave chamada ITSoftware. O comando habilita a chave, define seu tempo de expiração para a hora armazenada em $Expires e define as marcas armazenadas no $Tags.

### Exemplo 2: modificar uma tecla para excluir todas as marcas
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

Esses comandos excluem todas as marcas para uma versão específica de uma chave chamada ITSoftware.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Habilitar
Especifica se uma tecla deve ser habilitada ou desabilitada. Um valor de $True habilita a tecla. Um valor de $False desabilita a chave. Se você não especificar esse parâmetro, esse cmdlet não modificará o status da chave.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expira em
Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que este cmdlet atualiza. Esse parâmetro usa o tempo universal coordenado (UTC). Para obter um objeto **DateTime** , use o cmdlet **Get-Date** . Para obter mais informações, digite `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyOps
Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.
Se você não especificar esse parâmetro, todas as operações poderão ser executadas.

Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela especificação de chave da Web JSON. Esses valores (diferenciam maiúsculas de minúsculas) são:

- com
- criptografá
- quebrada
- desenvolva
- designa
- verificar
- fazer
- restaurar

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da chave a ser atualizada. Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Não antes
Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.
Esse parâmetro usa UTC.
Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera nenhuma saída.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Cofrename
Especifica o nome do cofre de chaves no qual esse cmdlet modifica a chave.
Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versão
Especifica a versão da chave.
Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)
