---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: e38402359a3bccebc33d92211ed10d8032a0dd4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888523"
---
# New-AzImportExport

## SYNOPSIS
Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.

## SINTAXE

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.

## EXEMPLOS

### Exemplo 1: Criar um novo trabalho ImportExport
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

Esses cmdlets criam um novo trabalho ImportExport.

## PARÂMETROS

### -AcceptLanguage
Especifica o idioma preferencial para a resposta.

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

### -BackupDriveManifest
O valor padrão é false.
Indica se os arquivos de manifesto nas unidades devem ser copiados para bloquear blobs.

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

### -BlobListBlobPath
Uma coleção de cadeias de caracteres de caminho de blob.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobListBlobPathPrefix
Uma coleção de cadeias de caracteres de prefixo de blob.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CancelRequested
Indica se uma solicitação foi enviada para cancelar o trabalho.

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

### -ClientTenantId
A ID do locatário do cliente que está fazendo a solicitação.

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
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageCarrierName
O nome da operadora usada para enviar as unidades de importação ou exportação.

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

### -DeliveryPackageDriveCount
O número de unidades incluídas no pacote.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeliveryPackageShipDate
A data em que o pacote é enviado.

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

### -DeliveryPackageTrackingNumber
O número de controle do pacote.

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

### -DiagnosticsPath
O diretório de blob virtual no qual os logs de cópia e backups de arquivos de manifesto da unidade (se habilitados) serão armazenados.

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

### -DriveList
Lista de até dez unidades que compõem o trabalho.
A lista de unidade é um elemento necessário para um trabalho de importação; não é especificado para trabalhos de exportação.
Para construir, consulte a seção NOTES para propriedades DRIVELIST e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExportBlobListblobPath
O URI relativo ao blob de bloco que contém a lista de caminhos de blob ou prefixos de caminho de blob conforme definido acima, começando com o nome do contêiner.
Se o blob estiver no contêiner raiz, o URI deve começar com $root.

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

### -IncompleteBlobListUri
Um caminho de blob que aponta para um blob de bloco que contém uma lista de nomes de blob que não foram exportados devido ao espaço insuficiente da unidade.
Se todos os blobs foram exportados com êxito, esse elemento não será incluído na resposta.

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

### -JobType
O tipo de trabalho

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

### -Location
Especifica o local do Azure com suporte onde o trabalho deve ser criado

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

### -LogLevel
O valor padrão é Error.
Indica se o log de erros ou o log detalhado serão habilitados.

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

### -Name
O nome do trabalho de importação/exportação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PercentComplete
Porcentagem geral concluída para o trabalho.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProvisioningState
Especifica o estado de provisionamento do trabalho.

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

### -ResourceGroupName
O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnAddressCity
O nome da cidade a ser usado ao retornar as unidades.

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

### -ReturnAddressCountryOrRegion
O país ou região a ser usado ao retornar as unidades.

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

### -ReturnAddressEmail
Endereço de email do destinatário das unidades retornadas.

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

### -ReturnAddressPhone
Número de telefone do destinatário das unidades retornadas.

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

### -ReturnAddressPostalCode
O código postal a ser usado ao retornar as unidades.

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

### -ReturnAddressRecipientName
O nome do destinatário que receberá os discos rígidos quando eles são retornados.

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

### -ReturnAddressStateOrProvince
O estado ou província a ser usado ao retornar as unidades.

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

### -ReturnAddressStreetAddress1
A primeira linha do endereço de rua a ser usada ao retornar as unidades.

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

### -ReturnAddressStreetAddress2
A segunda linha do endereço de rua a ser usada ao retornar as unidades.

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

### -ReturnPackageCarrierName
O nome da operadora usada para enviar as unidades de importação ou exportação.

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

### -ReturnPackageDriveCount
O número de unidades incluídas no pacote.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnPackageShipDate
A data em que o pacote é enviado.

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

### -ReturnPackageTrackingNumber
O número de controle do pacote.

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

### -ReturnShippingCarrierAccountNumber
O número da conta do cliente com a operadora.

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

### -ReturnShippingCarrierName
O nome da operadora.

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

### -ShippingInformationCity
O nome da cidade a ser usado ao retornar as unidades.

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

### -ShippingInformationCountryOrRegion
O país ou região a ser usado ao retornar as unidades.

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

### -ShippingInformationPhone
Número de telefone do destinatário das unidades retornadas.

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

### -ShippingInformationPostalCode
O código postal a ser usado ao retornar as unidades.

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

### -ShippingInformationRecipientName
O nome do destinatário que receberá os discos rígidos quando eles são retornados.

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

### -ShippingInformationStateOrProvince
O estado ou província a ser usado ao retornar as unidades.

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

### -ShippingInformationStreetAddress1
A primeira linha do endereço de rua a ser usada ao retornar as unidades.

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

### -ShippingInformationStreetAddress2
A segunda linha do endereço de rua a ser usada ao retornar as unidades.

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

### -State
Estado atual do trabalho.

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

### -StorageAccountId
O identificador de recurso da conta de armazenamento da qual os dados serão importados ou exportados.

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

### -SubscriptionId
A ID da assinatura do usuário do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Especifica as marcas que serão atribuídas ao trabalho.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse

## NOTES

ALIASES

PROPRIEDADES DE PARÂMETRO COMPLEXO

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


DRIVELIST <IDriveStatus[]>: lista de até dez unidades que compõem o trabalho. A lista de unidade é um elemento necessário para um trabalho de importação; não é especificado para trabalhos de exportação.
  - `[BitLockerKey <String>]`: A chave BitLocker usada para criptografar a unidade.
  - `[BytesSucceeded <Int64?>]`: Bytes transferidos com êxito para a unidade.
  - `[CopyStatus <String>]`: Status detalhado sobre o processo de transferência de dados. Esse campo não é retornado na resposta até que a unidade está no estado Transfering.
  - `[DriveHeaderHash <String>]`: O valor de hash do header da unidade.
  - `[DriveId <String>]`: O número de série de hardware da unidade, sem espaços.
  - `[ErrorLogUri <String>]`: Um URI que aponta para o blob que contém o log de erros da operação de transferência de dados.
  - `[ManifestFile <String>]`: O caminho relativo do arquivo de manifesto na unidade. 
  - `[ManifestHash <String>]`: O hash MD5 codificado em Base16 do arquivo de manifesto na unidade.
  - `[ManifestUri <String>]`: Um URI que aponta para o blob que contém o arquivo de manifesto da unidade. 
  - `[PercentComplete <Int32?>]`: Porcentagem concluída para a unidade. 
  - `[State <DriveState?>]`: o estado atual da unidade. 
  - `[VerboseLogUri <String>]`: Um URI que aponta para o blob que contém o log detalhado para a operação de transferência de dados. 

## LINKS RELACIONADOS

