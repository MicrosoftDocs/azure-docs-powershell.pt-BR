---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945909"
---
# New-AzureQuickVM

## Sinopse
Configura e cria uma máquina virtual do Azure.

## SYNTAX

### Windows (padrão)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureQuickVM** configura e cria uma máquina virtual do Azure.
Este cmdlet pode implantar uma máquina virtual em um serviço do Azure existente.
Esse cmdlet pode, opcionalmente, criar um serviço do Azure que hospede a nova máquina virtual.

## EXEMPLOS

### Exemplo 1: criar uma máquina virtual
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

Esse comando cria uma máquina virtual que executa o sistema operacional Windows em um serviço existente.
O cmdlet baseia a máquina virtual na imagem especificada.
O comando especifica o parâmetro *WaitForBoot* .
Portanto, o cmdlet aguarda a máquina virtual iniciar.

### Exemplo 2: criar uma máquina virtual que usa certificados
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

O primeiro comando obtém certificados de uma loja e os armazena na variável $certs.

O segundo comando cria uma máquina virtual que executa o sistema operacional do Windows em um serviço existente de uma imagem.
Por padrão, o ouvinte do WinRM HTTPS está habilitado na máquina virtual.
O comando especifica o parâmetro *WaitForBoot* .
Portanto, o cmdlet aguarda a máquina virtual iniciar.
O comando carrega um certificado WinRM e X509Certificates para o serviço hospedado.

### Exemplo 3: criar uma máquina virtual que executa o sistema operacional Linux
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

Esse comando cria uma máquina virtual que executa o sistema operacional Linux a partir de uma imagem.
Esse comando cria um serviço para hospedar a nova máquina virtual.
O comando especifica um local para o serviço.

### Exemplo 4: criar uma máquina virtual e criar um serviço para hospedar a nova máquina virtual
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

O primeiro comando obtém locais usando o cmdlet **Get-AzureLocation** e, em seguida, armazena-os na variável de matriz $Locations.

O segundo comando obtém as imagens disponíveis usando o cmdlet **Get-AzureVMImage** e, em seguida, as armazena na variável de matriz $images.

O comando final cria uma grande máquina virtual chamada VirtualMachine25.
A máquina virtual executa o sistema operacional Windows.
Ele é baseado em uma das imagens no $Images.
O comando cria um serviço denominado ContosoService03 para a nova máquina virtual.
O serviço está em um local no $Locations.

### Exemplo 5: criar uma máquina virtual com um nome de IP reservado
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

O primeiro comando obtém locais e, em seguida, armazena-os na variável de matriz de $Locations.

O segundo comando obtém as imagens disponíveis e as armazena na variável de matriz de $Images.

O comando final cria uma máquina virtual chamada VirtualMachine27 com base em uma das imagens no $Images.
O comando cria um serviço em um local no $Locations.
A máquina virtual tem um nome de IP reservado, anteriormente armazenado na variável $ipName.

## OS

### -AdminUsername
Especifica o nome de usuário da conta de administrador que esse cmdlet cria na máquina virtual.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
Especifica o grupo de afinidade para a máquina virtual.
Especifique esse parâmetro ou o parâmetro de *local* somente se esse cmdlet criar um serviço do Azure para a máquina virtual.

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

### -AvailabilitySetName
Especifica o nome do conjunto de disponibilidade em que esse cmdlet cria a máquina virtual.

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

### -Certificados
Especifica uma lista de certificados que este cmdlet usa para criar o serviço.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDatafile
Especifica um arquivo de dados para a máquina virtual.
Esse cmdlet codifica o conteúdo do arquivo como Base64.
O arquivo deve ter menos de 64 kilobytes de comprimento.

Se o sistema operacional convidado for o sistema operacional do Windows, esse cmdlet salvará esses dados como um arquivo binário chamado%SYSTEMDRIVE%\AzureData\CustomData.bin.

Se o sistema operacional convidado for Linux, esse cmdlet passará os dados usando o arquivo ovf-env.xml.
A instalação copia o arquivo para o diretório/var/lib/waagent.
O agente também armazena os dados codificados em base64 no/var/lib/waagent/CustomData.

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

### -DisableGuestAgent
Indica que esse cmdlet desabilita o agente convidado de provisionamento da infraestrutura como serviço (IaaS).

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

### -DisableWinRMHttps
Indica que esse cmdlet desabilita o gerenciamento remoto do Windows (WinRM) no HTTPS.
Por padrão, o WinRM está habilitado no HTTPS.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
Especifica uma matriz de objetos do servidor DNS que define as configurações de DNS para a nova implantação.
Para criar um objeto **DnsServer** , use o cmdlet **New-AzureDns** .

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
Indica que esse cmdlet habilita o WinRM sobre HTTP.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Especifica o modo de cache do host para o disco do sistema operacional.
Os valores válidos são: 

- ReadOnly
- Leitura

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

### -ImageName
Especifica o nome da imagem de disco que esse cmdlet usa para criar o disco do sistema operacional.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Instanceize
Especifica o tamanho da instância.
Os valores válidos são: 

- ExtraSmall
- Versalete
- Port
- Muita
- ExtraLarge
- A5
- A6
- A7
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

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

### -Linux
Indica que esse cmdlet cria uma máquina virtual baseada em Linux.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
Especifica o nome de usuário da conta administrativa do Linux que esse cmdlet cria na máquina virtual.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Especifica o datacenter do Azure que hospeda a máquina virtual.
Se você especificar esse parâmetro, o cmdlet criará um serviço do Azure no local especificado.
Especifique esse parâmetro ou o parâmetro *AffinityGroup* somente se esse cmdlet criar um serviço do Azure para a máquina virtual.

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

### -MediaLocation
Especifica o local de armazenamento do Azure em que esse cmdlet cria discos de máquinas virtuais.

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

### -Nome
Especifica o nome da máquina virtual que este cmdlet cria.

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

### -NoExportPrivateKey
Indica que essa configuração não carrega a chave privada.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
Indica que esse cmdlet não adiciona um ponto de extremidade WinRM para a máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Senha
Especifica a senha da conta administrativa.

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

### -ReservedIPName
Especifica o nome do IP reservado.

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

### -ReverseDnsFqdn
Especifica o nome de domínio totalmente qualificado para a pesquisa reversa de DNS.

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

### -ServiceName
Especifica o nome de um serviço do Azure novo ou existente ao qual esse cmdlet adiciona a nova máquina virtual.

Se você especificar um novo serviço, este cmdlet o criará.
Para criar um novo serviço, você deve especificar o *local* ou o parâmetro *AffinityGroup* .

Se você especificar um serviço existente, não especifique *local* ou *AffinityGroup*.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
Especifica os pares de chaves SSH.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
Especifica as chaves públicas SSH.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Subnetnames
Especifica uma matriz de nomes de sub-rede para a máquina virtual.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
Especifica o nome de uma rede virtual para a máquina virtual.

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

### -WaitForBoot
Indica que esse cmdlet aguarda que a máquina virtual atinja o estado ReadyRole.
Se a máquina virtual alcançar um dos seguintes Estados, o cmdlet falha: FailedStartingVM, ProvisioningFailed ou ProvisioningTimeout.

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

### -Windows
Indica que esse cmdlet cria um computador virtual do Windows.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
Especifica um certificado que este cmdlet associa a um ponto de extremidade do WinRM.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
Especifica uma matriz de certificados X509 que são implantados em um serviço hospedado.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
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

[Get-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[New-AzureDns](./New-AzureDns.md)


