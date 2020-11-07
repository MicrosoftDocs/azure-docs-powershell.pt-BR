---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770927"
---
# <span data-ttu-id="1471e-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1471e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1471e-102">SYNOPSIS</span></span>
<span data-ttu-id="1471e-103">Carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="1471e-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="1471e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1471e-104">SYNTAX</span></span>

### <span data-ttu-id="1471e-105">NoDiagnosticLogging (padrão)</span><span class="sxs-lookup"><span data-stu-id="1471e-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1471e-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="1471e-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1471e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1471e-107">DESCRIPTION</span></span>
<span data-ttu-id="1471e-108">O cmdlet **Import-AzDataLakeStoreItem** carrega um arquivo ou diretório local para um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="1471e-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="1471e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1471e-109">EXAMPLES</span></span>

### <span data-ttu-id="1471e-110">Exemplo 1: carregar um arquivo</span><span class="sxs-lookup"><span data-stu-id="1471e-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="1471e-111">Esse comando carrega o arquivo SrcFile.csv e o adiciona à pasta MyFiles no repositório data Lake como File.csv com uma simultaneidade de 4.</span><span class="sxs-lookup"><span data-stu-id="1471e-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="1471e-112">OS</span><span class="sxs-lookup"><span data-stu-id="1471e-112">PARAMETERS</span></span>

### <span data-ttu-id="1471e-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="1471e-113">-Account</span></span>
<span data-ttu-id="1471e-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1471e-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1471e-115">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="1471e-115">-Concurrency</span></span>
<span data-ttu-id="1471e-116">Indica o número de arquivos ou fragmentos para carregar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="1471e-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="1471e-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="1471e-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1471e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1471e-118">-DefaultProfile</span></span>
<span data-ttu-id="1471e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1471e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1471e-120">-Destino</span><span class="sxs-lookup"><span data-stu-id="1471e-120">-Destination</span></span>
<span data-ttu-id="1471e-121">Especifica o caminho do repositório data Lake para o qual carregar um arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="1471e-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1471e-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="1471e-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="1471e-123">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="1471e-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="1471e-124">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="1471e-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1471e-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="1471e-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="1471e-126">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="1471e-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1471e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1471e-127">-Force</span></span>
<span data-ttu-id="1471e-128">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="1471e-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="1471e-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="1471e-129">-ForceBinary</span></span>
<span data-ttu-id="1471e-130">Indica que o (s) arquivo (s) que está sendo copiado (s) devem ser copiados sem preocupação para a preservação da nova linha em acréscimos.</span><span class="sxs-lookup"><span data-stu-id="1471e-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="1471e-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1471e-131">-Path</span></span>
<span data-ttu-id="1471e-132">Especifica o caminho local do arquivo ou da pasta a ser carregada.</span><span class="sxs-lookup"><span data-stu-id="1471e-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="1471e-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="1471e-133">-Recurse</span></span>
<span data-ttu-id="1471e-134">Indica que essa operação deve carregar todos os itens em todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="1471e-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="1471e-135">-Retomar</span><span class="sxs-lookup"><span data-stu-id="1471e-135">-Resume</span></span>
<span data-ttu-id="1471e-136">Indica que o (s) arquivo (s) que está sendo copiado é uma continuação de um carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="1471e-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="1471e-137">Isso fará com que o sistema tente retomar o último arquivo que não foi totalmente carregado.</span><span class="sxs-lookup"><span data-stu-id="1471e-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="1471e-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1471e-138">-Confirm</span></span>
<span data-ttu-id="1471e-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1471e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1471e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1471e-140">-WhatIf</span></span>
<span data-ttu-id="1471e-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1471e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1471e-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1471e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1471e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1471e-143">CommonParameters</span></span>
<span data-ttu-id="1471e-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1471e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1471e-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1471e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1471e-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1471e-146">INPUTS</span></span>

### <span data-ttu-id="1471e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1471e-147">System.String</span></span>

### <span data-ttu-id="1471e-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1471e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1471e-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1471e-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1471e-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1471e-150">System.Int32</span></span>

### <span data-ttu-id="1471e-151">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="1471e-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="1471e-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1471e-152">OUTPUTS</span></span>

### <span data-ttu-id="1471e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1471e-153">System.String</span></span>

## <span data-ttu-id="1471e-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1471e-154">NOTES</span></span>

## <span data-ttu-id="1471e-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1471e-155">RELATED LINKS</span></span>

[<span data-ttu-id="1471e-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-158">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-159">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1471e-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1471e-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


