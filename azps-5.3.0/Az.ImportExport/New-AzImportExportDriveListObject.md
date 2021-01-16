---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433761"
---
# <span data-ttu-id="f6384-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="f6384-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="f6384-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6384-102">SYNOPSIS</span></span>
<span data-ttu-id="f6384-103">Crie um objeto Driverlist para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="f6384-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f6384-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6384-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6384-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6384-105">DESCRIPTION</span></span>
<span data-ttu-id="f6384-106">Crie um objeto Driverlist para ImportExport.</span><span class="sxs-lookup"><span data-stu-id="f6384-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f6384-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6384-107">EXAMPLES</span></span>

### <span data-ttu-id="f6384-108">Exemplo 1: criar uma nova unidade de disco para o trabalho ImportExport</span><span class="sxs-lookup"><span data-stu-id="f6384-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="f6384-109">Esses cmdlets criam uma nova unidade de disco para o trabalho do ImportExport.</span><span class="sxs-lookup"><span data-stu-id="f6384-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="f6384-110">OS</span><span class="sxs-lookup"><span data-stu-id="f6384-110">PARAMETERS</span></span>

### <span data-ttu-id="f6384-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="f6384-111">-BitLockerKey</span></span>
<span data-ttu-id="f6384-112">A chave do BitLocker usada para criptografar a unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="f6384-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="f6384-113">-BytesSucceeded</span></span>
<span data-ttu-id="f6384-114">Bytes transferidos com êxito para a unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="f6384-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="f6384-115">-CopyStatus</span></span>
<span data-ttu-id="f6384-116">Status detalhado sobre o processo de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="f6384-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="f6384-117">Este campo não é retornado na resposta até que a unidade esteja no estado de transferência.</span><span class="sxs-lookup"><span data-stu-id="f6384-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="f6384-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="f6384-118">-DriveHeaderHash</span></span>
<span data-ttu-id="f6384-119">O valor de hash do cabeçalho da unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="f6384-120">-DriveID</span><span class="sxs-lookup"><span data-stu-id="f6384-120">-DriveId</span></span>
<span data-ttu-id="f6384-121">O número de série do hardware da unidade, sem espaços.</span><span class="sxs-lookup"><span data-stu-id="f6384-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="f6384-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="f6384-122">-ErrorLogUri</span></span>
<span data-ttu-id="f6384-123">Um URI que aponta para o blob que contém o log de erros para a operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="f6384-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="f6384-124">-MANIFESTFILE</span><span class="sxs-lookup"><span data-stu-id="f6384-124">-ManifestFile</span></span>
<span data-ttu-id="f6384-125">O caminho relativo do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="f6384-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="f6384-126">-ManifestHash</span></span>
<span data-ttu-id="f6384-127">O hash MD5 codificado Base16 do arquivo de manifesto na unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="f6384-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="f6384-128">-ManifestUri</span></span>
<span data-ttu-id="f6384-129">Um URI que aponta para o blob que contém o arquivo de manifesto da unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="f6384-130">-PorcentagemConcluída</span><span class="sxs-lookup"><span data-stu-id="f6384-130">-PercentComplete</span></span>
<span data-ttu-id="f6384-131">Porcentagem concluída para a unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="f6384-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="f6384-132">-State</span></span>
<span data-ttu-id="f6384-133">O estado atual da unidade.</span><span class="sxs-lookup"><span data-stu-id="f6384-133">The drive's current state.</span></span>

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

### <span data-ttu-id="f6384-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="f6384-134">-VerboseLogUri</span></span>
<span data-ttu-id="f6384-135">Um URI que aponta para o blob que contém o log detalhado para a operação de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="f6384-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="f6384-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6384-136">CommonParameters</span></span>
<span data-ttu-id="f6384-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6384-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6384-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6384-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6384-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6384-139">INPUTS</span></span>

## <span data-ttu-id="f6384-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6384-140">OUTPUTS</span></span>

### <span data-ttu-id="f6384-141">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. Api20161101. IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="f6384-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="f6384-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6384-142">NOTES</span></span>

<span data-ttu-id="f6384-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f6384-143">ALIASES</span></span>

## <span data-ttu-id="f6384-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6384-144">RELATED LINKS</span></span>

