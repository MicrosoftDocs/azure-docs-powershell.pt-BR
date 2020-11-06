---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 7cc4af3e849a6cd24c2144c6e92c990da261e9d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609965"
---
# New-AzureRmKeyVault

## Sinopse
Cria um cofre de chaves.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmKeyVault** cria um cofre de chaves no grupo de recursos especificado. Esse cmdlet também concede permissões ao usuário conectado no momento para adicionar, remover ou listar chaves e segredos no cofre de chaves.

Observação: se você vir o erro **a assinatura não está registrada para usar o namespace ' Microsoft. keyvault '** ao tentar criar seu novo cofre de chaves, execute **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. keyvault"** e execute novamente o comando **New-AzureRmKeyVault** . Para obter mais informações, consulte Register-AzureRmResourceProvider.

## EXEMPLOS

### Exemplo 1: criar um cofre de chaves padrão
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

Esse comando cria um cofre de chaves chamado Contoso03Vault, na região do Azure leste dos EUA. O comando adiciona o cofre de chaves ao grupo de recursos chamado Group14. Como o comando não especifica um valor para o parâmetro *SKU* , ele cria um cofre de chaves padrão.

### Exemplo 2: criar um cofre de chave Premium
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

Esse comando cria um cofre de chaves, exatamente como o exemplo anterior. No entanto, ele especifica um valor de Premium para o parâmetro *SKU* para criar um cofre de chave Premium.

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

### -EnabledForDeployment
Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableSoftDelete
Especifica que a funcionalidade de exclusão suave está habilitada para este cofre de chaves. Quando a exclusão suave está habilitada, por um período de cortesia, você pode recuperar esse cofre de chaves e seu conteúdo após a exclusão.

Para obter mais informações sobre essa funcionalidade, consulte [visão geral do Azure Key Vault Soft-Delete](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete). Para obter instruções de como fazer, consulte [como usar o virtual Vault Soft-Delete com o PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica a região do Azure na qual criar o cofre de chaves. Use o comando [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) para ver suas opções.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do cofre de chaves a ser criado. O nome pode ser qualquer combinação de letras, dígitos ou hifens. O nome deve começar e terminar com uma letra ou um dígito. O nome deve ser universalmente exclusivo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Especifica a SKU da instância do cofre de chaves. Para obter informações sobre quais recursos estão disponíveis para cada SKU, consulte o site de preços do Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .

```yaml
Type: SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

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
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. keyvault. Models. PSKeyVault

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Remove-AzureRmKeyVault](./Remove-AzureRmKeyVault.md)
