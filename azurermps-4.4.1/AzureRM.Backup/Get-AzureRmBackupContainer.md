---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602233"
---
# Get-AzureRmBackupContainer

## Sinopse
Obtém contêineres de backup.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmBackupContainer** Obtém contêineres de backup do Azure.

Um **AzureBackupContainer** encapsula fontes de dados, itens protegidos e pontos de recuperação.
Um **AzureBackupContainer** pode ser um dos seguintes: 

- Um computador Windows Server
- Um servidor do System Center Data Protection Manager (SCDPM) 
- Uma máquina virtual do Azure infraestrutura como serviço (IaaS)

Antes de o backup poder fazer backup de uma fonte de dados ou item, você deve registrar o contêiner que a mantém com o serviço de backup do Azure.
O contêiner deve ser autenticado para enviar dados de backup para o cofre de backup.
Para computadores com o Windows Server e servidores do SCDPM, o registro é mantido com o nome de domínio totalmente qualificado do servidor.

## EXEMPLOS

### Exemplo 1: exibir todos os servidores registrados em um cofre
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .
O comando armazena esse objeto na variável $Vault.

O segundo comando obtém todos os contêineres do tipo Windows a partir do cofre no $Vault.

### Exemplo 2: obter um contêiner específico
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Esse comando obtém o contêiner chamado DPMSERVER. CONTOSO.COM.
O comando especifica o cofre no $Vault e o tipo de contêiner.

### Exemplo 3: exibir todas as máquinas virtuais do Azure registradas
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Este comando obtém as máquinas virtuais registradas do cofre no $Vault.

## OS

### -ManagedResourceGroupName
Especifica o nome do grupo de recursos associado ao contêiner.
Esse nome é o mesmo valor que você especificou para o parâmetro *ServiceName* ou *ResourceGroupName* do cmdlet Register-AzureRmBackupContainer.

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

### -Nome
Especifica o nome do contêiner que este cmdlet obtém.

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

### -Status
Especifica o status atual dos contêineres que este cmdlet obtém.
Os valores aceitáveis para esse parâmetro são:

- Não cadastrado 
- Removido 
- Registrar

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de contêiners que esse cmdlet obtém.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cofre
Especifica um cofre de backup do qual este cmdlet obtém contêineres.
Para obter um **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### AzureBackupVault

## EXIBE

### AzureBackupContainer

## INFORMA
* Nenhuma

## LINKS RELACIONADOS

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Cancelar registro-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


