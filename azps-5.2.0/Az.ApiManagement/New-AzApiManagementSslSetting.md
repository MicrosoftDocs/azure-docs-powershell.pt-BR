---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262046"
---
# New-AzApiManagementSslSetting

## Sinopse
Cria uma instância de PsApiManagementSslSetting

## SYNTAX

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
Comando auxiliar para criar uma instância de PsApiManagementSslSetting.
Esse comando deve ser usado com o comando New-AzApiManagement.

## EXEMPLOS

### Exemplo 1: criar uma configuração SSL para habilitar o TLS 1,0 em backend e front-end
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

Crie uma nova instância de PsApiManagementSslSetting para habilitar o TLSv 1,0 em ambos os front-end (entre cliente e APIM) e back-end (entre APIM e back-end) do gateway do ApiManagement.

## OS

### -BackendProtocol
Configurações do protocolo de segurança back-end. Este parâmetro é opcional.
As configurações de protocolo válidas são `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CipherSuite
Configurações de pacotes de codificação SSL na ordem especificada. Este parâmetro é opcional.
As configurações válidas são `TripleDes168` -habilitar/desabilitar a viagem Des 168

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -FrontendProtocol
Configurações de protocolos de segurança de front-end. Este parâmetro é opcional.
As configurações de protocolo válidas são `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerProtocol
Configurações de protocolo de servidor como Http2. Este parâmetro é opcional.
As configurações válidas são `Http2` -habilitar Http 2,0

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings

## INFORMA

## LINKS RELACIONADOS

[New-AzApiManagement](./New-AzApiManagement.md)

