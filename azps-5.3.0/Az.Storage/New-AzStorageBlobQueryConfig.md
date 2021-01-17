---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429090"
---
# <span data-ttu-id="182f9-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="182f9-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="182f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="182f9-102">SYNOPSIS</span></span>
<span data-ttu-id="182f9-103">Cria um objeto de configuração de consulta de BLOB, que pode ser usado em Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="182f9-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="182f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="182f9-104">SYNTAX</span></span>

### <span data-ttu-id="182f9-105">CSV (padrão)</span><span class="sxs-lookup"><span data-stu-id="182f9-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="182f9-106">Mal</span><span class="sxs-lookup"><span data-stu-id="182f9-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="182f9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="182f9-107">DESCRIPTION</span></span>
<span data-ttu-id="182f9-108">O cmdlet **New-AzStorageBlobQueryConfig** cria um objeto de configuração de consulta de BLOB, que pode ser usado em Get-AzStorageBlobQueryResult.</span><span class="sxs-lookup"><span data-stu-id="182f9-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="182f9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="182f9-109">EXAMPLES</span></span>

### <span data-ttu-id="182f9-110">Exemplo 1: criar uma consulta de blob configura e consulta um blob</span><span class="sxs-lookup"><span data-stu-id="182f9-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="182f9-111">Esse comando primeiro cria o objeto de configuração de entrada como CSV e o objeto de configuração de saída como JSON e, em seguida, use as duas configurações para o blob de consulta.</span><span class="sxs-lookup"><span data-stu-id="182f9-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="182f9-112">OS</span><span class="sxs-lookup"><span data-stu-id="182f9-112">PARAMETERS</span></span>

### <span data-ttu-id="182f9-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="182f9-113">-AsCsv</span></span>
<span data-ttu-id="182f9-114">Indicar a criação de uma configuração de consulta de BLOB para CSV.</span><span class="sxs-lookup"><span data-stu-id="182f9-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="182f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="182f9-115">-AsJob</span></span>
<span data-ttu-id="182f9-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="182f9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="182f9-117">-Asjson</span><span class="sxs-lookup"><span data-stu-id="182f9-117">-AsJson</span></span>
<span data-ttu-id="182f9-118">Indicar a criação de uma configuração de consulta de BLOB para JSON.</span><span class="sxs-lookup"><span data-stu-id="182f9-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="182f9-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="182f9-119">-ColumnSeparator</span></span>
<span data-ttu-id="182f9-120">Adicionais.</span><span class="sxs-lookup"><span data-stu-id="182f9-120">Optional.</span></span>
<span data-ttu-id="182f9-121">A cadeia de caracteres usada para separar colunas.</span><span class="sxs-lookup"><span data-stu-id="182f9-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="182f9-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="182f9-122">-EscapeCharacter</span></span>
<span data-ttu-id="182f9-123">Adicionais.</span><span class="sxs-lookup"><span data-stu-id="182f9-123">Optional.</span></span>
<span data-ttu-id="182f9-124">O caractere usado como um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="182f9-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="182f9-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="182f9-125">-HasHeader</span></span>
<span data-ttu-id="182f9-126">Adicionais.</span><span class="sxs-lookup"><span data-stu-id="182f9-126">Optional.</span></span>
<span data-ttu-id="182f9-127">Indicar que os dados têm cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="182f9-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="182f9-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="182f9-128">-QuotationCharacter</span></span>
<span data-ttu-id="182f9-129">Adicionais.</span><span class="sxs-lookup"><span data-stu-id="182f9-129">Optional.</span></span>
<span data-ttu-id="182f9-130">O caractere usado para citar um campo específico.</span><span class="sxs-lookup"><span data-stu-id="182f9-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="182f9-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="182f9-131">-RecordSeparator</span></span>
<span data-ttu-id="182f9-132">Adicionais.</span><span class="sxs-lookup"><span data-stu-id="182f9-132">Optional.</span></span>
<span data-ttu-id="182f9-133">A cadeia de caracteres usada para separar os registros.</span><span class="sxs-lookup"><span data-stu-id="182f9-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="182f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182f9-134">CommonParameters</span></span>
<span data-ttu-id="182f9-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="182f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182f9-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182f9-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="182f9-137">INPUTS</span></span>

### <span data-ttu-id="182f9-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="182f9-138">None</span></span>

## <span data-ttu-id="182f9-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="182f9-139">OUTPUTS</span></span>

### <span data-ttu-id="182f9-140">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="182f9-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="182f9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="182f9-141">NOTES</span></span>

## <span data-ttu-id="182f9-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="182f9-142">RELATED LINKS</span></span>
