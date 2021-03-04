---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: 942bd2635c79a925779239e9746cef53195b202e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891977"
---
# <span data-ttu-id="71bff-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="71bff-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="71bff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71bff-102">SYNOPSIS</span></span>
<span data-ttu-id="71bff-103">Cria um objeto de configuração de consulta blob, que pode ser usado em Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="71bff-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="71bff-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="71bff-104">SYNTAX</span></span>

### <span data-ttu-id="71bff-105">Csv (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71bff-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="71bff-106">Json</span><span class="sxs-lookup"><span data-stu-id="71bff-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="71bff-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="71bff-107">DESCRIPTION</span></span>
<span data-ttu-id="71bff-108">O cmdlet **New-AzStorageBlobQueryConfig** cria um objeto de configuração de consulta blob, que pode ser usado em Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="71bff-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="71bff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71bff-109">EXAMPLES</span></span>

### <span data-ttu-id="71bff-110">Exemplo 1: Criar consulta blob configura e consultar um blob</span><span class="sxs-lookup"><span data-stu-id="71bff-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="71bff-111">Este comando primeiro cria o objeto de configuração de entrada como csv e o objeto de configuração de saída como json e, em seguida, usa as 2 configurações para blob de consulta.</span><span class="sxs-lookup"><span data-stu-id="71bff-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="71bff-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="71bff-112">PARAMETERS</span></span>

### <span data-ttu-id="71bff-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="71bff-113">-AsCsv</span></span>
<span data-ttu-id="71bff-114">Indique para criar uma Configuração de Consulta de Blob para CSV.</span><span class="sxs-lookup"><span data-stu-id="71bff-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71bff-115">-AsJob</span></span>
<span data-ttu-id="71bff-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="71bff-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71bff-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="71bff-117">-AsJson</span></span>
<span data-ttu-id="71bff-118">Indique para criar uma Configuração de Consulta de Blob para Json.</span><span class="sxs-lookup"><span data-stu-id="71bff-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="71bff-119">-ColumnSeparator</span></span>
<span data-ttu-id="71bff-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="71bff-120">Optional.</span></span>
<span data-ttu-id="71bff-121">A cadeia de caracteres usada para separar colunas.</span><span class="sxs-lookup"><span data-stu-id="71bff-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="71bff-122">-EscapeCharacter</span></span>
<span data-ttu-id="71bff-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="71bff-123">Optional.</span></span>
<span data-ttu-id="71bff-124">O caractere char usado como um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="71bff-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="71bff-125">-HasHeader</span></span>
<span data-ttu-id="71bff-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="71bff-126">Optional.</span></span>
<span data-ttu-id="71bff-127">Indica que ele representa os dados que têm os headers.</span><span class="sxs-lookup"><span data-stu-id="71bff-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="71bff-128">-QuotationCharacter</span></span>
<span data-ttu-id="71bff-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="71bff-129">Optional.</span></span>
<span data-ttu-id="71bff-130">O char usado para citar um campo específico.</span><span class="sxs-lookup"><span data-stu-id="71bff-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71bff-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="71bff-131">-RecordSeparator</span></span>
<span data-ttu-id="71bff-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="71bff-132">Optional.</span></span>
<span data-ttu-id="71bff-133">A cadeia de caracteres usada para separar registros.</span><span class="sxs-lookup"><span data-stu-id="71bff-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="71bff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71bff-134">CommonParameters</span></span>
<span data-ttu-id="71bff-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71bff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71bff-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71bff-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71bff-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71bff-137">INPUTS</span></span>

### <span data-ttu-id="71bff-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="71bff-138">None</span></span>

## <span data-ttu-id="71bff-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="71bff-139">OUTPUTS</span></span>

### <span data-ttu-id="71bff-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="71bff-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="71bff-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="71bff-141">NOTES</span></span>

## <span data-ttu-id="71bff-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71bff-142">RELATED LINKS</span></span>
