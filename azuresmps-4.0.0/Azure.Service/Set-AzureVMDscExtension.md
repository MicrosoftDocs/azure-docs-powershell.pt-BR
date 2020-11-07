---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947351"
---
# Set-AzureVMDscExtension

## Sinopse
Configura a extensão DSC em uma máquina virtual.

## SYNTAX

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureVMDscExtension** configura a extensão da configuração de estado desejada (DSC) em uma máquina virtual.

## EXEMPLOS

### Exemplo 1: configurar a extensão DSC em uma máquina virtual
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

Esse comando configura a extensão DSC em uma máquina virtual.

O pacote MyConfiguration.ps1.zip deve ter sido previamente carregado no armazenamento do Azure usando o comando **Publish-AzureVMDscConfiguration** e inclui o script MyConfiguration.ps1 e os módulos dos quais ele depende.

O argumento myconfiguration indica a configuração DSC específica dentro do script a ser executada.
O parâmetro- *ConfigurationArgument* especifica uma Hashtable com os argumentos que são passados para a função de configuração.

### Exemplo 2: configurar a extensão DSC em uma máquina virtual usando um caminho para os dados de configuração
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

Esse comando configura a extensão DSC em uma máquina virtual usando um caminho para os dados de configuração.

## OS

### -ConfigurationArchive
Especifica o nome do pacote de configuração (arquivo. zip) que foi carregado anteriormente por Publish-AzureVMDscConfiguration.
Esse parâmetro deve especificar somente o nome do arquivo, sem qualquer caminho.

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

### -ConfigurationArgument
Especifica uma Hashtable especificando os argumentos para a função de configuração.
As chaves correspondem aos nomes de parâmetro e aos valores para os valores de parâmetro.

Os valores aceitáveis para esse parâmetro são:

- tipos primitivos
- String
- matriz
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Especifica o caminho de um arquivo. psd1 que especifica os dados para a função de configuração.
Esse arquivo deve conter uma Hashtable, conforme descrito em separando os dados de configuração e de ambiente https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Especifica o nome do script de configuração ou do módulo que é invocado pela extensão DSC.

O valor desse parâmetro deve ser o nome de uma das funções de configuração contidas nos scripts ou módulos empacotados em *ConfigurationArchive*.

Esse cmdlet usa como padrão o nome do arquivo fornecido pelo parâmetro *ConfigurationArchive* se você omitir esse parâmetro, excluindo qualquer extensão.
Por exemplo, se *ConfigurationArchive* for "SalesWebSite.ps1.zip", o valor padrão para *ConfigurationName* será "SalesWebSite".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ContainerName
Especifica o nome do contêiner de armazenamento do Azure em que o *ConfigurationArchive* está localizado.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataCollection
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet substitui BLOBs existentes.

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

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Referencename
Especifica uma cadeia de caracteres definida pelo usuário que pode ser usada para fazer referência a uma extensão.
Esse parâmetro é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.
Para atualizações subsequentes, você deve especificar o nome de referência usado anteriormente enquanto atualiza a extensão.
O *referencename* atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Especifica o contexto de armazenamento do Azure que fornece as configurações de segurança usadas para acessar o script de configuração.
Esse contexto fornece acesso de leitura ao contêiner especificado pelo parâmetro *ContainerName* .

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Especifica o sufixo de ponto de extremidade DNS para todos os serviços de armazenamento, por exemplo, "core.contoso.net".

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versão
Especifica a versão específica da extensão DSC a ser usada.
O valor padrão é definido como "1. *" se esse parâmetro não for especificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica o objeto da máquina virtual persistente.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
Especifica a versão da Windows Management Framework (WMF) a ser instalada na máquina virtual.
A extensão DSC depende dos recursos DSC disponíveis apenas nas atualizações do WMF.
Esse parâmetro especifica qual versão da atualização instalar na máquina virtual.
Os valores aceitáveis para esse parâmetro são:

- 4,0.
Instala o WMF 4,0, a menos que uma versão mais recente já esteja instalada.
- 5,0.
Instala a versão mais recente do WMF 5,0.
- novidades.
Instala o WMF mais recente, no momento, o WMF 5,0.

O valor padrão é mais recente.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Publicar-AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


