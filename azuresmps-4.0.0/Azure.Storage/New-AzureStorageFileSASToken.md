---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BB139312-A536-4B61-A005-6CAF02BE1637
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19d3017ffdff2ebc0f0c8d614b5b9c4d4b0514d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425978"
---
# New-AzureStorageFileSASToken

## Sinopse
Gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento.

## SYNTAX

### NameSasPermission
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### NameSasPolicy
```
New-AzureStorageFileSASToken [-ShareName] <String> [-Path] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### FileSasPermission
```
New-AzureStorageFileSASToken -File <CloudFile> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

### FileSasPolicy
```
New-AzureStorageFileSASToken -File <CloudFile> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageFileSASToken** gera um token de assinatura de acesso compartilhado para um arquivo de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: gerar um token de assinatura de acesso compartilhado com permissões de arquivo completas
```
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd"
```

Esse comando gera um token de assinatura de acesso compartilhado que tem permissões completas para o arquivo chamado FilePath.

### Exemplo 2: gerar um token de assinatura de acesso compartilhado que tenha um limite de tempo
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $StartTime.AddHours(2.0)
PS C:\> New-AzureStorageFileSASToken -ShareName "ContosoShare" -Path "FilePath" -Permission "rwd" -StartTime $StartTime -ExpiryTime $EndTime
```

O primeiro comando cria um objeto **DateTime** usando o cmdlet Get-Date.
O comando armazena a hora atual na variável $StartTime.

O segundo comando adiciona duas horas ao objeto no $StartTime e armazena o resultado na variável $EndTime.
Esse objeto é uma hora de duas horas no futuro.

O terceiro comando gera um token de assinatura de acesso compartilhado que tem as permissões especificadas.
Esse token se torna válido no momento atual.
O token permanecerá válido até o tempo ser armazenado em $EndTime.

## OS

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto, use o cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ExpiryTime
Especifica o tempo em que a assinatura de acesso compartilhado se torna inválida.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Arquivo
Especifica um objeto **cloudfile** .
Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.

```yaml
Type: CloudFile
Parameter Sets: FileSasPermission, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FullUri
Indica que esse cmdlet retorna o URI de blob completo e o token de assinatura de acesso compartilhado.

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

### -IPAddressOrRange
Especifica o endereço IP ou o intervalo de endereços IP do qual aceitar solicitações, como 168.1.5.65 ou 168.1.5.60-168.1.5.70.
O intervalo é inclusivo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento.

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Permissão
Especifica as permissões para um arquivo de armazenamento.

```yaml
Type: String
Parameter Sets: NameSasPermission, FileSasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Política
Especifica a política de acesso armazenada para um arquivo.

```yaml
Type: String
Parameter Sets: NameSasPolicy, FileSasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocolo
Especifica o protocolo permitido para uma solicitação.
Os valores aceitáveis para esse parâmetro são:
* HttpsOnly
* HttpsOrHttp

O valor padrão é HttpsOrHttp.

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
Especifica o nome do compartilhamento de armazenamento.

```yaml
Type: String
Parameter Sets: NameSasPermission, NameSasPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -StartTime
Especifica a hora em que a assinatura de acesso compartilhado se torna válida.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

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

## INFORMA

## LINKS RELACIONADOS

[New-AzureStorageContext](./New-AzureStorageContext.md)

[New-AzureStorageShareSASToken](./New-AzureStorageShareSASToken.md)
