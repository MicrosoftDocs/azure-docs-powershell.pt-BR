---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887739"
---
# <span data-ttu-id="e2969-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="e2969-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="e2969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2969-102">SYNOPSIS</span></span>
<span data-ttu-id="e2969-103">Crie um objeto DriverList para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="e2969-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e2969-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e2969-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="e2969-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e2969-105">DESCRIPTION</span></span>
<span data-ttu-id="e2969-106">Crie um objeto DriverList para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="e2969-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="e2969-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2969-107">EXAMPLES</span></span>

### <span data-ttu-id="e2969-108">Exemplo 1: Criar um novo trabalho DriveList para ImportExport</span><span class="sxs-lookup"><span data-stu-id="e2969-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="e2969-109">Esses cmdlets criam um novo trabalho DriveList para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="e2969-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="e2969-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e2969-110">PARAMETERS</span></span>

### <span data-ttu-id="e2969-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="e2969-111">-BitLockerKey</span></span>
<span data-ttu-id="e2969-112">A chave BitLocker usada para criptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="e2969-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="e2969-113">-BytesSucceeded</span></span>
<span data-ttu-id="e2969-114">Bytes transferidos com êxito para a unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2969-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="e2969-115">-CopyStatus</span></span>
<span data-ttu-id="e2969-116">Status detalhado sobre o processo de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="e2969-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="e2969-117">Esse campo não é retornado na resposta até que a unidade está no estado Transfering.</span><span class="sxs-lookup"><span data-stu-id="e2969-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="e2969-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="e2969-118">-DriveHeaderHash</span></span>
<span data-ttu-id="e2969-119">O valor de hash do header da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="e2969-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="e2969-120">-DriveId</span></span>
<span data-ttu-id="e2969-121">O número de série de hardware da unidade, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="e2969-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="e2969-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="e2969-122">-ErrorLogUri</span></span>
<span data-ttu-id="e2969-123">Um URI que aponta para o blob que contém o log de erros da operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="e2969-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e2969-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="e2969-124">-ManifestFile</span></span>
<span data-ttu-id="e2969-125">O caminho relativo do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e2969-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="e2969-126">-ManifestHash</span></span>
<span data-ttu-id="e2969-127">O hash MD5 codificado em Base16 do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="e2969-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="e2969-128">-ManifestUri</span></span>
<span data-ttu-id="e2969-129">Um URI que aponta para o blob que contém o arquivo de manifesto da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="e2969-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="e2969-130">-PercentComplete</span></span>
<span data-ttu-id="e2969-131">Porcentagem concluída para a unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="e2969-132">-State</span><span class="sxs-lookup"><span data-stu-id="e2969-132">-State</span></span>
<span data-ttu-id="e2969-133">O estado atual da unidade.</span><span class="sxs-lookup"><span data-stu-id="e2969-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2969-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="e2969-134">-VerboseLogUri</span></span>
<span data-ttu-id="e2969-135">Um URI que aponta para o blob que contém o log detalhado para a operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="e2969-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="e2969-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2969-136">CommonParameters</span></span>
<span data-ttu-id="e2969-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2969-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2969-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2969-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2969-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2969-139">INPUTS</span></span>

## <span data-ttu-id="e2969-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e2969-140">OUTPUTS</span></span>

### <span data-ttu-id="e2969-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="e2969-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="e2969-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="e2969-142">NOTES</span></span>

<span data-ttu-id="e2969-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2969-143">ALIASES</span></span>

## <span data-ttu-id="e2969-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2969-144">RELATED LINKS</span></span>

