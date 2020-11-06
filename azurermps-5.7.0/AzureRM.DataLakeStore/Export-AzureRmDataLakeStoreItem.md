---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602374"
---
# <span data-ttu-id="88c5f-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="88c5f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="88c5f-103">Baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="88c5f-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88c5f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88c5f-104">SYNTAX</span></span>

### <span data-ttu-id="88c5f-105">NoDiagnosticLogging (padrão)</span><span class="sxs-lookup"><span data-stu-id="88c5f-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c5f-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="88c5f-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c5f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88c5f-107">DESCRIPTION</span></span>
<span data-ttu-id="88c5f-108">O cmdlet **Export-AzureRmDataLakeStoreItem** baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="88c5f-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="88c5f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88c5f-109">EXAMPLES</span></span>

### <span data-ttu-id="88c5f-110">Exemplo 1: baixar um item do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="88c5f-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="88c5f-111">Esse comando baixa o arquivo TestSource.csv do data Lake Store para C:\Test.csv com uma simultaneidade de 4.</span><span class="sxs-lookup"><span data-stu-id="88c5f-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="88c5f-112">OS</span><span class="sxs-lookup"><span data-stu-id="88c5f-112">PARAMETERS</span></span>

### <span data-ttu-id="88c5f-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="88c5f-113">-Account</span></span>
<span data-ttu-id="88c5f-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="88c5f-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="88c5f-115">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="88c5f-115">-Concurrency</span></span>
<span data-ttu-id="88c5f-116">Indica o número de arquivos ou blocos a serem baixados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="88c5f-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="88c5f-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="88c5f-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5f-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="88c5f-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="88c5f-119">Indica o número máximo de arquivos a serem baixados em paralelo para um download de pasta.</span><span class="sxs-lookup"><span data-stu-id="88c5f-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="88c5f-120">O padrão será calculado como um melhor esforço com base na pasta e no tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="88c5f-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="88c5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c5f-121">-DefaultProfile</span></span>
<span data-ttu-id="88c5f-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88c5f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c5f-123">-Destino</span><span class="sxs-lookup"><span data-stu-id="88c5f-123">-Destination</span></span>
<span data-ttu-id="88c5f-124">Especifica o caminho do arquivo local para o qual baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="88c5f-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5f-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="88c5f-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="88c5f-126">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="88c5f-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="88c5f-127">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="88c5f-127">Default is Error.</span></span>

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

### <span data-ttu-id="88c5f-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="88c5f-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="88c5f-129">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="88c5f-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="88c5f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="88c5f-130">-Force</span></span>
<span data-ttu-id="88c5f-131">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="88c5f-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5f-132">-Caminho</span><span class="sxs-lookup"><span data-stu-id="88c5f-132">-Path</span></span>
<span data-ttu-id="88c5f-133">Especifica o caminho do item a ser baixado do repositório data Lake, começando do diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="88c5f-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5f-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="88c5f-134">-PerFileThreadCount</span></span>
<span data-ttu-id="88c5f-135">Indica o número máximo de threads a serem usados por arquivo.</span><span class="sxs-lookup"><span data-stu-id="88c5f-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="88c5f-136">O padrão será calculado como um melhor esforço com base na pasta e no tamanho do arquivo</span><span class="sxs-lookup"><span data-stu-id="88c5f-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88c5f-137">-Recurse</span><span class="sxs-lookup"><span data-stu-id="88c5f-137">-Recurse</span></span>
<span data-ttu-id="88c5f-138">Indica que um download de pasta é recursivo.</span><span class="sxs-lookup"><span data-stu-id="88c5f-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="88c5f-139">-Retomar</span><span class="sxs-lookup"><span data-stu-id="88c5f-139">-Resume</span></span>
<span data-ttu-id="88c5f-140">Indica que o (s) arquivo (s) que está sendo copiado é uma continuação de um download anterior.</span><span class="sxs-lookup"><span data-stu-id="88c5f-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="88c5f-141">Isso fará com que o sistema tente retomar o último arquivo que não foi totalmente baixado.</span><span class="sxs-lookup"><span data-stu-id="88c5f-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="88c5f-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88c5f-142">-Confirm</span></span>
<span data-ttu-id="88c5f-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c5f-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88c5f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c5f-144">-WhatIf</span></span>
<span data-ttu-id="88c5f-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88c5f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c5f-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88c5f-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88c5f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c5f-147">CommonParameters</span></span>
<span data-ttu-id="88c5f-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c5f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c5f-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88c5f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c5f-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88c5f-150">INPUTS</span></span>

### <span data-ttu-id="88c5f-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88c5f-151">None</span></span>
<span data-ttu-id="88c5f-152">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="88c5f-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88c5f-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88c5f-153">OUTPUTS</span></span>

### <span data-ttu-id="88c5f-154">String</span><span class="sxs-lookup"><span data-stu-id="88c5f-154">string</span></span>
<span data-ttu-id="88c5f-155">O caminho no qual o arquivo ou a pasta foi baixada.</span><span class="sxs-lookup"><span data-stu-id="88c5f-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="88c5f-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88c5f-156">NOTES</span></span>

## <span data-ttu-id="88c5f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88c5f-157">RELATED LINKS</span></span>

[<span data-ttu-id="88c5f-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-160">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-161">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-162">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="88c5f-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="88c5f-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


