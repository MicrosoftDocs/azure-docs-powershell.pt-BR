---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: afe19fed7cd8de43cb28b7b3f73b01312cdd42fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891048"
---
# <span data-ttu-id="82747-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="82747-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82747-102">SYNOPSIS</span></span>
<span data-ttu-id="82747-103">Carrega um arquivo ou diretório local em um Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82747-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="82747-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="82747-104">SYNTAX</span></span>

### <span data-ttu-id="82747-105">NoDiagnosticLogging (Padrão)</span><span class="sxs-lookup"><span data-stu-id="82747-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82747-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="82747-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82747-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="82747-107">DESCRIPTION</span></span>
<span data-ttu-id="82747-108">O cmdlet **Import-AzDataLakeStoreItem** carrega um arquivo ou diretório local em um Repositório do Data Lake.</span><span class="sxs-lookup"><span data-stu-id="82747-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="82747-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="82747-109">EXAMPLES</span></span>

### <span data-ttu-id="82747-110">Exemplo 1: Carregar um arquivo</span><span class="sxs-lookup"><span data-stu-id="82747-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="82747-111">Este comando carrega o arquivo SrcFile.csv e o adiciona à pasta MyFiles no Data Lake Store como File.csv com uma simulta de 4.</span><span class="sxs-lookup"><span data-stu-id="82747-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="82747-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="82747-112">PARAMETERS</span></span>

### <span data-ttu-id="82747-113">-Account</span><span class="sxs-lookup"><span data-stu-id="82747-113">-Account</span></span>
<span data-ttu-id="82747-114">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="82747-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="82747-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="82747-115">-Concurrency</span></span>
<span data-ttu-id="82747-116">Indica o número de arquivos ou partes para carregar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="82747-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="82747-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="82747-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="82747-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82747-118">-DefaultProfile</span></span>
<span data-ttu-id="82747-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="82747-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82747-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="82747-120">-Destination</span></span>
<span data-ttu-id="82747-121">Especifica o caminho do Data Lake Store para o qual carregar um arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="82747-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="82747-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="82747-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="82747-123">Opcionalmente, indica o nível de log de diagnóstico a ser usado para registrar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="82747-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="82747-124">O padrão é Error.</span><span class="sxs-lookup"><span data-stu-id="82747-124">Default is Error.</span></span>

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

### <span data-ttu-id="82747-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="82747-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="82747-126">Especifica o caminho para que o log de diagnóstico registre eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="82747-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="82747-127">-Force</span><span class="sxs-lookup"><span data-stu-id="82747-127">-Force</span></span>
<span data-ttu-id="82747-128">Indica que essa operação pode substituir o arquivo de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="82747-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="82747-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="82747-129">-ForceBinary</span></span>
<span data-ttu-id="82747-130">Indica que os arquivos que estão sendo copiados devem ser copiados sem preocupação com a preservação de nova linha entre os apêndices.</span><span class="sxs-lookup"><span data-stu-id="82747-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="82747-131">-Path</span><span class="sxs-lookup"><span data-stu-id="82747-131">-Path</span></span>
<span data-ttu-id="82747-132">Especifica o caminho local do arquivo ou pasta a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="82747-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="82747-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="82747-133">-Recurse</span></span>
<span data-ttu-id="82747-134">Indica que essa operação deve carregar todos os itens em todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="82747-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="82747-135">-Resume</span><span class="sxs-lookup"><span data-stu-id="82747-135">-Resume</span></span>
<span data-ttu-id="82747-136">Indica que os arquivos que estão sendo copiados são uma continuação de um carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="82747-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="82747-137">Isso fará com que o sistema tente retomar do último arquivo que não foi carregado totalmente.</span><span class="sxs-lookup"><span data-stu-id="82747-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="82747-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82747-138">-Confirm</span></span>
<span data-ttu-id="82747-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82747-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82747-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82747-140">-WhatIf</span></span>
<span data-ttu-id="82747-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="82747-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82747-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="82747-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82747-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82747-143">CommonParameters</span></span>
<span data-ttu-id="82747-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82747-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82747-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82747-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82747-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82747-146">INPUTS</span></span>

### <span data-ttu-id="82747-147">System.String</span><span class="sxs-lookup"><span data-stu-id="82747-147">System.String</span></span>

### <span data-ttu-id="82747-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="82747-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="82747-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82747-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="82747-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="82747-150">System.Int32</span></span>

### <span data-ttu-id="82747-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="82747-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="82747-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="82747-152">OUTPUTS</span></span>

### <span data-ttu-id="82747-153">System.String</span><span class="sxs-lookup"><span data-stu-id="82747-153">System.String</span></span>

## <span data-ttu-id="82747-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="82747-154">NOTES</span></span>

## <span data-ttu-id="82747-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="82747-155">RELATED LINKS</span></span>

[<span data-ttu-id="82747-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="82747-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="82747-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


