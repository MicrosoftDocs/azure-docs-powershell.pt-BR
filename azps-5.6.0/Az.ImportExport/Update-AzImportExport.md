---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888252"
---
# <span data-ttu-id="07145-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="07145-101">Update-AzImportExport</span></span>

## <span data-ttu-id="07145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07145-102">SYNOPSIS</span></span>
<span data-ttu-id="07145-103">Atualiza propriedades específicas de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="07145-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="07145-104">Você pode chamar essa operação para notificar o serviço de Importação/Exportação de que os discos rígidos que compõem o trabalho de importação ou exportação foram enviados para o data center da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07145-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="07145-105">Ele também pode ser usado para cancelar um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="07145-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="07145-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07145-106">SYNTAX</span></span>

### <span data-ttu-id="07145-107">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07145-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="07145-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="07145-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="07145-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07145-109">DESCRIPTION</span></span>
<span data-ttu-id="07145-110">Atualiza propriedades específicas de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="07145-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="07145-111">Você pode chamar essa operação para notificar o serviço de Importação/Exportação de que os discos rígidos que compõem o trabalho de importação ou exportação foram enviados para o data center da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07145-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="07145-112">Ele também pode ser usado para cancelar um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="07145-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="07145-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07145-113">EXAMPLES</span></span>

### <span data-ttu-id="07145-114">Exemplo 1: Atualizar o trabalho ImportExport por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="07145-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="07145-115">Este cmdlet atualiza o trabalho ImportExport por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="07145-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="07145-116">Exemplo 2: Atualizar o trabalho ImportExport por identidade.</span><span class="sxs-lookup"><span data-stu-id="07145-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="07145-117">Este cmdlet atualiza o trabalho ImportExport por identidade.</span><span class="sxs-lookup"><span data-stu-id="07145-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="07145-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07145-118">PARAMETERS</span></span>

### <span data-ttu-id="07145-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="07145-119">-AcceptLanguage</span></span>
<span data-ttu-id="07145-120">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="07145-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="07145-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="07145-121">-BackupDriveManifest</span></span>
<span data-ttu-id="07145-122">Indica se os arquivos de manifesto nas unidades devem ser copiados para bloquear blobs.</span><span class="sxs-lookup"><span data-stu-id="07145-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="07145-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="07145-123">-CancelRequested</span></span>
<span data-ttu-id="07145-124">Se especificado, o valor deve ser true.</span><span class="sxs-lookup"><span data-stu-id="07145-124">If specified, the value must be true.</span></span>
<span data-ttu-id="07145-125">O serviço tentará cancelar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="07145-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="07145-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07145-126">-DefaultProfile</span></span>
<span data-ttu-id="07145-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07145-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07145-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="07145-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="07145-129">O nome da operadora usada para enviar as unidades de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="07145-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="07145-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="07145-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="07145-131">O número de unidades incluídas no pacote.</span><span class="sxs-lookup"><span data-stu-id="07145-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="07145-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="07145-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="07145-133">A data em que o pacote é enviado.</span><span class="sxs-lookup"><span data-stu-id="07145-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="07145-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="07145-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="07145-135">O número de controle do pacote.</span><span class="sxs-lookup"><span data-stu-id="07145-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="07145-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="07145-136">-DriveList</span></span>
<span data-ttu-id="07145-137">Lista de unidades que compõem o trabalho.</span><span class="sxs-lookup"><span data-stu-id="07145-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="07145-138">Para construir, consulte a seção NOTES para propriedades DRIVELIST e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="07145-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="07145-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07145-139">-InputObject</span></span>
<span data-ttu-id="07145-140">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="07145-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07145-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="07145-141">-LogLevel</span></span>
<span data-ttu-id="07145-142">Indica se o log de erros ou o log detalhado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="07145-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="07145-143">-Name</span><span class="sxs-lookup"><span data-stu-id="07145-143">-Name</span></span>
<span data-ttu-id="07145-144">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="07145-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07145-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07145-145">-ResourceGroupName</span></span>
<span data-ttu-id="07145-146">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="07145-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07145-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="07145-147">-ReturnAddressCity</span></span>
<span data-ttu-id="07145-148">O nome da cidade a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="07145-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="07145-150">O país ou região a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="07145-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="07145-152">Endereço de email do destinatário das unidades retornadas.</span><span class="sxs-lookup"><span data-stu-id="07145-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="07145-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="07145-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="07145-154">Número de telefone do destinatário das unidades retornadas.</span><span class="sxs-lookup"><span data-stu-id="07145-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="07145-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="07145-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="07145-156">O código postal a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="07145-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="07145-158">O nome do destinatário que receberá os discos rígidos quando eles são retornados.</span><span class="sxs-lookup"><span data-stu-id="07145-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="07145-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="07145-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="07145-160">O estado ou província a ser usado ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="07145-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="07145-162">A primeira linha do endereço de rua a ser usada ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="07145-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="07145-164">A segunda linha do endereço de rua a ser usada ao retornar as unidades.</span><span class="sxs-lookup"><span data-stu-id="07145-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="07145-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="07145-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="07145-166">O número da conta do cliente com a operadora.</span><span class="sxs-lookup"><span data-stu-id="07145-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="07145-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="07145-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="07145-168">O nome da operadora.</span><span class="sxs-lookup"><span data-stu-id="07145-168">The carrier's name.</span></span>

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

### <span data-ttu-id="07145-169">-State</span><span class="sxs-lookup"><span data-stu-id="07145-169">-State</span></span>
<span data-ttu-id="07145-170">Se especificado, o valor deve ser Envio, que informa ao serviço de Importação/Exportação que o pacote do trabalho foi enviado.</span><span class="sxs-lookup"><span data-stu-id="07145-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="07145-171">As propriedades ReturnAddress e DeliveryPackage devem ter sido definidas nesta solicitação ou em uma solicitação anterior, caso contrário, a solicitação falhará.</span><span class="sxs-lookup"><span data-stu-id="07145-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="07145-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="07145-172">-SubscriptionId</span></span>
<span data-ttu-id="07145-173">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="07145-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07145-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="07145-174">-Tag</span></span>
<span data-ttu-id="07145-175">Especifica as marcas que serão atribuídas ao trabalho</span><span class="sxs-lookup"><span data-stu-id="07145-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07145-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07145-176">-Confirm</span></span>
<span data-ttu-id="07145-177">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07145-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07145-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07145-178">-WhatIf</span></span>
<span data-ttu-id="07145-179">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07145-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07145-180">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07145-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07145-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07145-181">CommonParameters</span></span>
<span data-ttu-id="07145-182">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07145-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07145-183">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07145-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07145-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07145-184">INPUTS</span></span>

### <span data-ttu-id="07145-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="07145-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="07145-186">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07145-186">OUTPUTS</span></span>

### <span data-ttu-id="07145-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="07145-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="07145-188">NOTES</span><span class="sxs-lookup"><span data-stu-id="07145-188">NOTES</span></span>

<span data-ttu-id="07145-189">ALIASES</span><span class="sxs-lookup"><span data-stu-id="07145-189">ALIASES</span></span>

<span data-ttu-id="07145-190">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="07145-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="07145-191">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="07145-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="07145-192">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="07145-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="07145-193">DRIVELIST <IDriveStatus[]>: lista de unidades que compõem o trabalho.</span><span class="sxs-lookup"><span data-stu-id="07145-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="07145-194">`[BitLockerKey <String>]`: A chave BitLocker usada para criptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="07145-195">`[BytesSucceeded <Int64?>]`: Bytes transferidos com êxito para a unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="07145-196">`[CopyStatus <String>]`: Status detalhado sobre o processo de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="07145-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="07145-197">Esse campo não é retornado na resposta até que a unidade está no estado Transfering.</span><span class="sxs-lookup"><span data-stu-id="07145-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="07145-198">`[DriveHeaderHash <String>]`: O valor de hash do header da unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="07145-199">`[DriveId <String>]`: O número de série de hardware da unidade, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="07145-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="07145-200">`[ErrorLogUri <String>]`: Um URI que aponta para o blob que contém o log de erros da operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="07145-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="07145-201">`[ManifestFile <String>]`: O caminho relativo do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="07145-202">`[ManifestHash <String>]`: O hash MD5 codificado em Base16 do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="07145-203">`[ManifestUri <String>]`: Um URI que aponta para o blob que contém o arquivo de manifesto da unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="07145-204">`[PercentComplete <Int32?>]`: Porcentagem concluída para a unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="07145-205">`[State <DriveState?>]`: o estado atual da unidade.</span><span class="sxs-lookup"><span data-stu-id="07145-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="07145-206">`[VerboseLogUri <String>]`: Um URI que aponta para o blob que contém o log detalhado para a operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="07145-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="07145-207">INPUTOBJECT <IImportExportIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="07145-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="07145-208">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="07145-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="07145-209">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="07145-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="07145-210">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="07145-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="07145-211">Por exemplo, West US ou westus.</span><span class="sxs-lookup"><span data-stu-id="07145-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="07145-212">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="07145-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="07145-213">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="07145-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="07145-214">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07145-214">RELATED LINKS</span></span>

