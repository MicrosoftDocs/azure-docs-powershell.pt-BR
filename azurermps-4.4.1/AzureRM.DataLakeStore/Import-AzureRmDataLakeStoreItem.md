---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609687"
---
# <span data-ttu-id="e67dd-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e67dd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e67dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e67dd-103">Carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="e67dd-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e67dd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e67dd-104">SYNTAX</span></span>

### <span data-ttu-id="e67dd-105">Sem log de diagnóstico (padrão)</span><span class="sxs-lookup"><span data-stu-id="e67dd-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67dd-106">Incluir log de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="e67dd-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e67dd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e67dd-107">DESCRIPTION</span></span>
<span data-ttu-id="e67dd-108">O cmdlet **Import-AzureRmDataLakeStoreItem** carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="e67dd-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="e67dd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e67dd-109">EXAMPLES</span></span>

### <span data-ttu-id="e67dd-110">Exemplo 1: carregar um arquivo</span><span class="sxs-lookup"><span data-stu-id="e67dd-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="e67dd-111">Esse comando carrega o arquivo SrcFile.csv e o adiciona à pasta MyFiles no repositório data Lake como File.csv.</span><span class="sxs-lookup"><span data-stu-id="e67dd-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="e67dd-112">OS</span><span class="sxs-lookup"><span data-stu-id="e67dd-112">PARAMETERS</span></span>

### <span data-ttu-id="e67dd-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="e67dd-113">-Account</span></span>
<span data-ttu-id="e67dd-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e67dd-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="e67dd-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="e67dd-116">Especifique o número máximo de arquivos a serem carregados em paralelo para um carregamento de pasta.</span><span class="sxs-lookup"><span data-stu-id="e67dd-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="e67dd-117">O valor padrão é cinco (5).</span><span class="sxs-lookup"><span data-stu-id="e67dd-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-118">-Destino</span><span class="sxs-lookup"><span data-stu-id="e67dd-118">-Destination</span></span>
<span data-ttu-id="e67dd-119">Especifica o caminho do repositório data Lake para o qual carregar um arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="e67dd-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e67dd-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e67dd-121">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="e67dd-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e67dd-122">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="e67dd-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e67dd-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="e67dd-124">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="e67dd-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e67dd-125">-Force</span></span>
<span data-ttu-id="e67dd-126">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="e67dd-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="e67dd-127">-ForceBinary</span></span>
<span data-ttu-id="e67dd-128">Indica que esta operação carrega o arquivo como um arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e67dd-128">Indicates that this operation uploads the file as a binary file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="e67dd-129">-Path</span></span>
<span data-ttu-id="e67dd-130">Especifica o caminho local do arquivo ou da pasta a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="e67dd-130">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="e67dd-131">-PerFileThreadCount</span></span>
<span data-ttu-id="e67dd-132">Especifica o número máximo de threads a serem usados por arquivo.</span><span class="sxs-lookup"><span data-stu-id="e67dd-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="e67dd-133">O valor padrão é 10 (10).</span><span class="sxs-lookup"><span data-stu-id="e67dd-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-134">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e67dd-134">-Recurse</span></span>
<span data-ttu-id="e67dd-135">Indica que essa operação deve carregar todos os itens em todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="e67dd-135">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-136">-Retomar</span><span class="sxs-lookup"><span data-stu-id="e67dd-136">-Resume</span></span>
<span data-ttu-id="e67dd-137">Indica que esta operação deve retomar um carregamento previamente cancelado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="e67dd-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e67dd-138">-Confirm</span></span>
<span data-ttu-id="e67dd-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e67dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67dd-140">-WhatIf</span></span>
<span data-ttu-id="e67dd-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e67dd-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e67dd-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e67dd-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67dd-143">-DefaultProfile</span></span>
<span data-ttu-id="e67dd-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e67dd-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67dd-145">CommonParameters</span></span>
<span data-ttu-id="e67dd-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e67dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67dd-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67dd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67dd-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e67dd-148">INPUTS</span></span>

## <span data-ttu-id="e67dd-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e67dd-149">OUTPUTS</span></span>

### <span data-ttu-id="e67dd-150">String</span><span class="sxs-lookup"><span data-stu-id="e67dd-150">string</span></span>
<span data-ttu-id="e67dd-151">O caminho completo na conta data Lake Store para o arquivo ou pasta carregada.</span><span class="sxs-lookup"><span data-stu-id="e67dd-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="e67dd-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e67dd-152">NOTES</span></span>

## <span data-ttu-id="e67dd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e67dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="e67dd-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-156">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-157">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-158">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e67dd-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e67dd-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


