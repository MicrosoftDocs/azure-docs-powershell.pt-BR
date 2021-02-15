---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113797"
---
# <span data-ttu-id="ff7bb-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="ff7bb-101">New-AzImportExport</span></span>

## <span data-ttu-id="ff7bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7bb-103">Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="ff7bb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff7bb-104">SYNTAX</span></span>

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

## <span data-ttu-id="ff7bb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="ff7bb-106">Cria um novo trabalho ou atualiza um trabalho existente na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="ff7bb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="ff7bb-108">Exemplo 1: Criar um novo trabalho ImportExport</span><span class="sxs-lookup"><span data-stu-id="ff7bb-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="ff7bb-109">Esses cmdlets criam um novo trabalho ImportExport.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="ff7bb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff7bb-110">PARAMETERS</span></span>

### <span data-ttu-id="ff7bb-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="ff7bb-111">-AcceptLanguage</span></span>
<span data-ttu-id="ff7bb-112">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="ff7bb-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="ff7bb-113">-BackupDriveManifest</span></span>
<span data-ttu-id="ff7bb-114">O valor padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-114">Default value is false.</span></span>
<span data-ttu-id="ff7bb-115">Indica se os arquivos de manifesto nas unidades devem ser copiados para bloquear blobs.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="ff7bb-116">-BlobListBpath</span><span class="sxs-lookup"><span data-stu-id="ff7bb-116">-BlobListBlobPath</span></span>
<span data-ttu-id="ff7bb-117">Um conjunto de cadeias de caracteres de caminho de blob.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="ff7bb-118">-BlobListBpathPrefix</span><span class="sxs-lookup"><span data-stu-id="ff7bb-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="ff7bb-119">Um conjunto de cadeias de caracteres de prefixo de blob.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="ff7bb-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="ff7bb-120">-CancelRequested</span></span>
<span data-ttu-id="ff7bb-121">Indica se uma solicitação foi enviada para cancelar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="ff7bb-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="ff7bb-122">-ClientTenantId</span></span>
<span data-ttu-id="ff7bb-123">A ID do locatário do cliente que está fazendo a solicitação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="ff7bb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7bb-124">-DefaultProfile</span></span>
<span data-ttu-id="ff7bb-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff7bb-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="ff7bb-127">O nome da operadora usada para enviar as unidades de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="ff7bb-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="ff7bb-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="ff7bb-129">O número de unidades incluídas no pacote.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="ff7bb-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="ff7bb-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="ff7bb-131">A data em que o pacote é enviado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="ff7bb-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="ff7bb-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="ff7bb-133">O número de acompanhamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="ff7bb-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="ff7bb-134">-DiagnosticsPath</span></span>
<span data-ttu-id="ff7bb-135">O diretório de blob virtual para o qual os logs de cópia e backups de arquivos de manifesto de unidade (se habilitado) serão armazenados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="ff7bb-136">-Lista de Discos</span><span class="sxs-lookup"><span data-stu-id="ff7bb-136">-DriveList</span></span>
<span data-ttu-id="ff7bb-137">Lista de até dez unidades que compõem o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="ff7bb-138">A lista de unidade é um elemento obrigatório para um trabalho de importação; não é especificado para trabalhos de exportação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="ff7bb-139">Para construir, confira a seção ANOTAÇÕES para propriedades da LISTA DE UNIDADE e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="ff7bb-140">-ExportBlistbpath</span><span class="sxs-lookup"><span data-stu-id="ff7bb-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="ff7bb-141">O URI relativo ao blob de bloco que contém a lista de trajetórias de blob ou prefixos de caminho de blob conforme definido acima, começando com o nome do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="ff7bb-142">Se o blob estiver no contêiner raiz, o URI deve começar com $root.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="ff7bb-143">-IncompleteBlistUri</span><span class="sxs-lookup"><span data-stu-id="ff7bb-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="ff7bb-144">Um caminho de blob que aponta para um blob de bloco que contém uma lista de nomes de blob que não foram exportados devido a um espaço de unidade insuficiente.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="ff7bb-145">Se todos os blobs foram exportados com êxito, esse elemento não será incluído na resposta.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="ff7bb-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="ff7bb-146">-JobType</span></span>
<span data-ttu-id="ff7bb-147">O tipo de trabalho</span><span class="sxs-lookup"><span data-stu-id="ff7bb-147">The type of job</span></span>

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

### <span data-ttu-id="ff7bb-148">-Local</span><span class="sxs-lookup"><span data-stu-id="ff7bb-148">-Location</span></span>
<span data-ttu-id="ff7bb-149">Especifica o local do Azure com suporte onde o trabalho deve ser criado</span><span class="sxs-lookup"><span data-stu-id="ff7bb-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="ff7bb-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="ff7bb-150">-LogLevel</span></span>
<span data-ttu-id="ff7bb-151">O valor padrão é Erro.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-151">Default value is Error.</span></span>
<span data-ttu-id="ff7bb-152">Indica se o log de erros ou o registro em log detalhado serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="ff7bb-153">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff7bb-153">-Name</span></span>
<span data-ttu-id="ff7bb-154">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="ff7bb-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="ff7bb-155">-PercentComplete</span></span>
<span data-ttu-id="ff7bb-156">Porcentagem geral concluída para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="ff7bb-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="ff7bb-157">-ProvisioningState</span></span>
<span data-ttu-id="ff7bb-158">Especifica o estado de provisionamento do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="ff7bb-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-159">-ResourceGroupName</span></span>
<span data-ttu-id="ff7bb-160">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="ff7bb-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="ff7bb-161">-ReturnAddressCity</span></span>
<span data-ttu-id="ff7bb-162">O nome da cidade a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="ff7bb-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="ff7bb-164">O país ou região a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="ff7bb-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="ff7bb-166">Endereço de email do destinatário das unidades retornadas.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="ff7bb-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="ff7bb-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="ff7bb-168">Número de telefone do destinatário das unidades retornadas.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="ff7bb-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="ff7bb-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="ff7bb-170">O CEP a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="ff7bb-172">O nome do destinatário que receberá os discos rígidos quando ele for retornado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="ff7bb-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="ff7bb-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="ff7bb-174">O estado ou a província a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-175">-ReturnAddressDressDress1</span><span class="sxs-lookup"><span data-stu-id="ff7bb-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="ff7bb-176">A primeira linha do endereço a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-177">-ReturnAddressDressDress2</span><span class="sxs-lookup"><span data-stu-id="ff7bb-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="ff7bb-178">A segunda linha do endereço de rua a ser usada ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="ff7bb-180">O nome da operadora usada para enviar as unidades de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="ff7bb-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="ff7bb-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="ff7bb-182">O número de unidades incluídas no pacote.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="ff7bb-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="ff7bb-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="ff7bb-184">A data em que o pacote é enviado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="ff7bb-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="ff7bb-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="ff7bb-186">O número de acompanhamento do pacote.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="ff7bb-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="ff7bb-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="ff7bb-188">O número da conta do cliente com a operadora.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="ff7bb-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="ff7bb-190">O nome da operadora.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-190">The carrier's name.</span></span>

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

### <span data-ttu-id="ff7bb-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="ff7bb-191">-ShippingInformationCity</span></span>
<span data-ttu-id="ff7bb-192">O nome da cidade a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="ff7bb-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="ff7bb-194">O país ou região a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="ff7bb-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="ff7bb-196">Número de telefone do destinatário das unidades retornadas.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="ff7bb-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="ff7bb-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="ff7bb-198">O CEP a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="ff7bb-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="ff7bb-200">O nome do destinatário que receberá os discos rígidos quando ele for retornado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="ff7bb-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="ff7bb-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="ff7bb-202">O estado ou a província a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-203">-ShippingInformationInaAddress1</span><span class="sxs-lookup"><span data-stu-id="ff7bb-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="ff7bb-204">A primeira linha do endereço a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-205">-ShippingInformationInaAddress2</span><span class="sxs-lookup"><span data-stu-id="ff7bb-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="ff7bb-206">A segunda linha do endereço de rua a ser usada ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="ff7bb-207">-Estado</span><span class="sxs-lookup"><span data-stu-id="ff7bb-207">-State</span></span>
<span data-ttu-id="ff7bb-208">Estado atual do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-208">Current state of the job.</span></span>

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

### <span data-ttu-id="ff7bb-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff7bb-209">-StorageAccountId</span></span>
<span data-ttu-id="ff7bb-210">O identificador de recursos da conta de armazenamento da qual os dados serão importados ou exportados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="ff7bb-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff7bb-211">-SubscriptionId</span></span>
<span data-ttu-id="ff7bb-212">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="ff7bb-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff7bb-213">-Tag</span></span>
<span data-ttu-id="ff7bb-214">Especifica as marcas que serão atribuídas ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="ff7bb-215">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ff7bb-215">-Confirm</span></span>
<span data-ttu-id="ff7bb-216">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff7bb-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff7bb-217">-WhatIf</span></span>
<span data-ttu-id="ff7bb-218">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff7bb-219">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff7bb-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7bb-220">CommonParameters</span></span>
<span data-ttu-id="ff7bb-221">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7bb-222">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff7bb-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7bb-223">Entradas</span><span class="sxs-lookup"><span data-stu-id="ff7bb-223">INPUTS</span></span>

## <span data-ttu-id="ff7bb-224">Saídas</span><span class="sxs-lookup"><span data-stu-id="ff7bb-224">OUTPUTS</span></span>

### <span data-ttu-id="ff7bb-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="ff7bb-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="ff7bb-226">Notas</span><span class="sxs-lookup"><span data-stu-id="ff7bb-226">NOTES</span></span>

<span data-ttu-id="ff7bb-227">Aliases</span><span class="sxs-lookup"><span data-stu-id="ff7bb-227">ALIASES</span></span>

<span data-ttu-id="ff7bb-228">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ff7bb-229">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ff7bb-230">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ff7bb-231">LISTA DE <IDriveStatus[]>: Lista de até dez unidades que compõem o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="ff7bb-232">A lista de unidade é um elemento obrigatório para um trabalho de importação; não é especificado para trabalhos de exportação.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="ff7bb-233">`[BitLockerKey <String>]`: a chave BitLocker usada para criptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="ff7bb-234">`[BytesSucceeded <Int64?>]`: Bytes transferidos com êxito para a unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="ff7bb-235">`[CopyStatus <String>]`: Status detalhado sobre o processo de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="ff7bb-236">Esse campo não será retornado na resposta até que a unidade seja transferida.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="ff7bb-237">`[DriveHeaderHash <String>]`: o valor de hash do header da unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="ff7bb-238">`[DriveId <String>]`: O número de série de hardware da unidade, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="ff7bb-239">`[ErrorLogUri <String>]`: um URI que aponta para o blob que contém o log de erros da operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="ff7bb-240">`[ManifestFile <String>]`: o caminho relativo do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="ff7bb-241">`[ManifestHash <String>]`: O hash MD5 codificado com Base16 do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="ff7bb-242">`[ManifestUri <String>]`: um URI que aponta para o blob que contém o arquivo de manifesto da unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="ff7bb-243">`[PercentComplete <Int32?>]`: Porcentagem concluída para a unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="ff7bb-244">`[State <DriveState?>]`: o estado atual da unidade.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="ff7bb-245">`[VerboseLogUri <String>]`: um URI que aponta para o blob que contém o log detalhado para a operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="ff7bb-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="ff7bb-246">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff7bb-246">RELATED LINKS</span></span>

