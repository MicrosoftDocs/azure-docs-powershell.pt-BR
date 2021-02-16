---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116337"
---
# <span data-ttu-id="1ca97-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="1ca97-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="1ca97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ca97-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca97-103">Cria um objeto de configuração de consulta de blob, que pode ser usado no Get-AzStorageB diamondQueryResult.</span><span class="sxs-lookup"><span data-stu-id="1ca97-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="1ca97-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ca97-104">SYNTAX</span></span>

### <span data-ttu-id="1ca97-105">Csv (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ca97-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="1ca97-106">Json</span><span class="sxs-lookup"><span data-stu-id="1ca97-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="1ca97-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ca97-107">DESCRIPTION</span></span>
<span data-ttu-id="1ca97-108">O cmdlet **New-AzStorageB diamondQueryConfig** cria um objeto de configuração de consulta de blob, que pode ser usado no Get-AzStorageB diamondQueryResult.</span><span class="sxs-lookup"><span data-stu-id="1ca97-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="1ca97-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1ca97-109">EXAMPLES</span></span>

### <span data-ttu-id="1ca97-110">Exemplo 1: criar uma consulta de blob configura e consultar um blob</span><span class="sxs-lookup"><span data-stu-id="1ca97-110">Example 1: Create blob query configures , and query a blob</span></span>
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

<span data-ttu-id="1ca97-111">Esse comando primeiro cria o objeto de configuração de entrada como csv e o objeto de configuração de saída como json e, em seguida, usa as 2 configurações para blob de consulta.</span><span class="sxs-lookup"><span data-stu-id="1ca97-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="1ca97-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ca97-112">PARAMETERS</span></span>

### <span data-ttu-id="1ca97-113">-AsCsv</span><span class="sxs-lookup"><span data-stu-id="1ca97-113">-AsCsv</span></span>
<span data-ttu-id="1ca97-114">Indicar para criar uma Configuração de Consulta de Blob para CSV.</span><span class="sxs-lookup"><span data-stu-id="1ca97-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

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

### <span data-ttu-id="1ca97-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ca97-115">-AsJob</span></span>
<span data-ttu-id="1ca97-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1ca97-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ca97-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="1ca97-117">-AsJson</span></span>
<span data-ttu-id="1ca97-118">Indique para criar uma Configuração de Consulta blob para Json.</span><span class="sxs-lookup"><span data-stu-id="1ca97-118">Indicate to create a Blob Query Configuration for Json.</span></span>

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

### <span data-ttu-id="1ca97-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="1ca97-119">-ColumnSeparator</span></span>
<span data-ttu-id="1ca97-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca97-120">Optional.</span></span>
<span data-ttu-id="1ca97-121">A cadeia de caracteres usada para separar colunas.</span><span class="sxs-lookup"><span data-stu-id="1ca97-121">The string used to separate columns.</span></span>

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

### <span data-ttu-id="1ca97-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="1ca97-122">-EscapeCharacter</span></span>
<span data-ttu-id="1ca97-123">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca97-123">Optional.</span></span>
<span data-ttu-id="1ca97-124">A char usada como um caractere de escape.</span><span class="sxs-lookup"><span data-stu-id="1ca97-124">The char used as an escape character.</span></span>

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

### <span data-ttu-id="1ca97-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="1ca97-125">-HasHeader</span></span>
<span data-ttu-id="1ca97-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca97-126">Optional.</span></span>
<span data-ttu-id="1ca97-127">Indique que ele representa os dados com os headers.</span><span class="sxs-lookup"><span data-stu-id="1ca97-127">Indicate it represent the data has headers.</span></span>

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

### <span data-ttu-id="1ca97-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="1ca97-128">-QuotationCharacter</span></span>
<span data-ttu-id="1ca97-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca97-129">Optional.</span></span>
<span data-ttu-id="1ca97-130">A char costumava citar um campo específico.</span><span class="sxs-lookup"><span data-stu-id="1ca97-130">The char used to quote a specific field.</span></span>

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

### <span data-ttu-id="1ca97-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="1ca97-131">-RecordSeparator</span></span>
<span data-ttu-id="1ca97-132">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1ca97-132">Optional.</span></span>
<span data-ttu-id="1ca97-133">A cadeia de caracteres usada para separar registros.</span><span class="sxs-lookup"><span data-stu-id="1ca97-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="1ca97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca97-134">CommonParameters</span></span>
<span data-ttu-id="1ca97-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca97-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca97-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca97-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="1ca97-137">INPUTS</span></span>

### <span data-ttu-id="1ca97-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1ca97-138">None</span></span>

## <span data-ttu-id="1ca97-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="1ca97-139">OUTPUTS</span></span>

### <span data-ttu-id="1ca97-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBltQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ca97-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="1ca97-141">Notas</span><span class="sxs-lookup"><span data-stu-id="1ca97-141">NOTES</span></span>

## <span data-ttu-id="1ca97-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ca97-142">RELATED LINKS</span></span>
