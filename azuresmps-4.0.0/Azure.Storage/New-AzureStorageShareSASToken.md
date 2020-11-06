---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: ''
schema: 2.0.0
ms.openlocfilehash: 427276a496108a48b69fd81cb5835d74859c25b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425924"
---
# New-AzureStorageShareSASToken

## Sinopse
Gerar token de assinatura de acesso compartilhado para compartilhamento de armazenamento do Azure.

## SYNTAX

### SasPolicy
```
New-AzureStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### SasPermission
```
New-AzureStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureStorageShareSASToken** gera um token de assinatura de acesso compartilhado para um compartilhamento de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: gerar um token de assinatura de acesso compartilhado para um compartilhamento
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento chamado ContosoShare.

### Exemplo 2: gerar vários tokens de assinatura de acesso compartilhado usando o pipeline
```
PS C:\>Get-AzureStorageShare -Prefix "test" | New-AzureStorageShareSASToken -Permission "rwdl"
```

Esse comando obtém todos os compartilhamentos de armazenamento correspondentes ao teste de prefixo.
O comando passa a ele para o cmdlet atual usando o operador pipeline.
O cmdlet atual cria um token de acesso compartilhado para cada compartilhamento de armazenamento que tenha as permissões especificadas.

### Exemplo 3: gerar um token de assinatura de acesso compartilhado que usa uma política de acesso compartilhado
```
PS C:\>New-AzureStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

Esse comando cria um token de assinatura de acesso compartilhado para o compartilhamento de armazenamento chamado ContosoShare que tem a política chamada ContosoPolicy03.

## OS

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto, use o cmdlet New-AzureStorageContext.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Permissão
Especifica as permissões no token para acessar o compartilhamento e os arquivos no compartilhamento.

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Política
Especifica a política de acesso armazenada para um compartilhamento.

```yaml
Type: String
Parameter Sets: SasPolicy
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
Parameter Sets: (All)
Aliases: N, Name

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
* Palavras-chave: comum, Azure, serviços, dados, armazenamento, BLOB, fila, tabela

## LINKS RELACIONADOS

[Get-AzureStorageShare](./Get-AzureStorageShare.md)

[New-AzureStorageFileSASToken](./New-AzureStorageFileSASToken.md)
