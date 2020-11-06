---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432136"
---
# <span data-ttu-id="6e320-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6e320-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e320-102">SYNOPSIS</span></span>
<span data-ttu-id="6e320-103">Carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="6e320-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e320-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e320-104">SYNTAX</span></span>

### <span data-ttu-id="6e320-105">NoDiagnosticLogging (padrão)</span><span class="sxs-lookup"><span data-stu-id="6e320-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e320-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="6e320-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e320-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e320-107">DESCRIPTION</span></span>
<span data-ttu-id="6e320-108">O cmdlet **Import-AzureRmDataLakeStoreItem** carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="6e320-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6e320-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e320-109">EXAMPLES</span></span>

### <span data-ttu-id="6e320-110">Exemplo 1: carregar um arquivo</span><span class="sxs-lookup"><span data-stu-id="6e320-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="6e320-111">Esse comando carrega o arquivo SrcFile.csv e o adiciona à pasta MyFiles no repositório data Lake como File.csv com uma simultaneidade de 4.</span><span class="sxs-lookup"><span data-stu-id="6e320-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="6e320-112">OS</span><span class="sxs-lookup"><span data-stu-id="6e320-112">PARAMETERS</span></span>

### <span data-ttu-id="6e320-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="6e320-113">-Account</span></span>
<span data-ttu-id="6e320-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e320-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-115">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="6e320-115">-Concurrency</span></span>
<span data-ttu-id="6e320-116">Indica o número de arquivos ou fragmentos para carregar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="6e320-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="6e320-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="6e320-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="6e320-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="6e320-119">Indica o número máximo de arquivos a serem carregados em paralelo para um carregamento de pasta.</span><span class="sxs-lookup"><span data-stu-id="6e320-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="6e320-120">O padrão será calculado como um melhor esforço com base na pasta e no tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="6e320-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e320-121">-DefaultProfile</span></span>
<span data-ttu-id="6e320-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6e320-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-123">-Destino</span><span class="sxs-lookup"><span data-stu-id="6e320-123">-Destination</span></span>
<span data-ttu-id="6e320-124">Especifica o caminho do repositório data Lake para o qual carregar um arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="6e320-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="6e320-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="6e320-126">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="6e320-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="6e320-127">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="6e320-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="6e320-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="6e320-129">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="6e320-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6e320-130">-Force</span></span>
<span data-ttu-id="6e320-131">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="6e320-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="6e320-132">-ForceBinary</span></span>
<span data-ttu-id="6e320-133">Indica que o (s) arquivo (s) que está sendo copiado (s) devem ser copiados sem preocupação para a preservação da nova linha em acréscimos.</span><span class="sxs-lookup"><span data-stu-id="6e320-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6e320-134">-Path</span></span>
<span data-ttu-id="6e320-135">Especifica o caminho local do arquivo ou da pasta a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="6e320-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="6e320-136">-PerFileThreadCount</span></span>
<span data-ttu-id="6e320-137">Indica o número máximo de threads a serem usados por arquivo.</span><span class="sxs-lookup"><span data-stu-id="6e320-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="6e320-138">O padrão será calculado como um melhor esforço com base na pasta e no tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="6e320-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-139">-Recurse</span><span class="sxs-lookup"><span data-stu-id="6e320-139">-Recurse</span></span>
<span data-ttu-id="6e320-140">Indica que essa operação deve carregar todos os itens em todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="6e320-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-141">-Retomar</span><span class="sxs-lookup"><span data-stu-id="6e320-141">-Resume</span></span>
<span data-ttu-id="6e320-142">Indica que o (s) arquivo (s) que está sendo copiado é uma continuação de um carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="6e320-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="6e320-143">Isso fará com que o sistema tente retomar o último arquivo que não foi totalmente carregado.</span><span class="sxs-lookup"><span data-stu-id="6e320-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6e320-144">-Confirm</span></span>
<span data-ttu-id="6e320-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e320-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e320-146">-WhatIf</span></span>
<span data-ttu-id="6e320-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6e320-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e320-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6e320-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e320-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e320-149">CommonParameters</span></span>
<span data-ttu-id="6e320-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e320-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e320-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e320-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e320-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e320-152">INPUTS</span></span>

### <span data-ttu-id="6e320-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6e320-153">None</span></span>
<span data-ttu-id="6e320-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6e320-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6e320-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e320-155">OUTPUTS</span></span>

### <span data-ttu-id="6e320-156">String</span><span class="sxs-lookup"><span data-stu-id="6e320-156">string</span></span>
<span data-ttu-id="6e320-157">O caminho completo na conta data Lake Store para o arquivo ou pasta carregada.</span><span class="sxs-lookup"><span data-stu-id="6e320-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="6e320-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e320-158">NOTES</span></span>

## <span data-ttu-id="6e320-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e320-159">RELATED LINKS</span></span>

[<span data-ttu-id="6e320-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-162">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-163">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-164">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6e320-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6e320-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


