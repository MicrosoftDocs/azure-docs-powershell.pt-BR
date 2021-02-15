---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116112"
---
# Get-AzStorageAccountKey

## Sinopse
Obtém as chaves de acesso de uma conta de Armazenamento do Azure.

## Sintaxe

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzStorageAccountKey** obtém as teclas de acesso de uma conta de Armazenamento do Azure.

## Exemplos

### Exemplo 1: Obter as teclas de acesso de uma conta de armazenamento
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

Esse comando obtém as chaves da conta de Armazenamento do Azure especificada.

### Exemplo 2: Obter uma chave de acesso específica para uma conta de armazenamento
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### Exemplo 3: Lista as teclas de acesso de uma conta de armazenamento, incluindo as teclas Kerberos (se o Active Directory estiver habilitado)
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

Esse comando obtém as chaves da conta de Armazenamento do Azure especificada.

## Parâmetros

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

### -ListKerbKey
Lista as teclas Kerberos (se o Active Directory estiver habilitado) para a conta de armazenamento especificada.
A chave Kerberos é gerada por conta de armazenamento para autenticação baseada em identidade de Arquivos do Azure com o Azure Active Directory Domain Service (Azure AD DS) ou o AD DS (Active Directory Domain Service). Ele é usado como a senha da identidade registrada no serviço de domínio que representa a conta de armazenamento. A tecla Kerberos não fornece permissão de acesso para executar quaisquer operações de leitura ou gravação de plano de dados em relação à conta de armazenamento.

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

### -Nome
Especifica o nome da conta de Armazenamento para a qual este cmdlet obtém chaves.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a conta de Armazenamento.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Management.Storage.Models.StorageAccountKey

## Notas

## LINKS RELACIONADOS

[New-AzStorageAccountKey](./New-AzStorageAccountKey.md)


