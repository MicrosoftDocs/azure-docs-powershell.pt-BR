---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886049"
---
# <span data-ttu-id="18b7c-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="18b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="18b7c-103">Baixa um arquivo do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18b7c-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="18b7c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="18b7c-104">SYNTAX</span></span>

### <span data-ttu-id="18b7c-105">NoDiagnosticLogging (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18b7c-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18b7c-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="18b7c-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18b7c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="18b7c-107">DESCRIPTION</span></span>
<span data-ttu-id="18b7c-108">O cmdlet **Export-AzDataLakeStoreItem** baixa um arquivo do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18b7c-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="18b7c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18b7c-109">EXAMPLES</span></span>

### <span data-ttu-id="18b7c-110">Exemplo 1: Baixar um item do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="18b7c-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="18b7c-111">Este comando baixa o arquivo TestSource.csv do Data Lake Store para C:\Test.csv com uma concurreência de 4.</span><span class="sxs-lookup"><span data-stu-id="18b7c-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="18b7c-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="18b7c-112">PARAMETERS</span></span>

### <span data-ttu-id="18b7c-113">-Account</span><span class="sxs-lookup"><span data-stu-id="18b7c-113">-Account</span></span>
<span data-ttu-id="18b7c-114">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18b7c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="18b7c-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="18b7c-115">-Concurrency</span></span>
<span data-ttu-id="18b7c-116">Indica o número de arquivos ou partes a baixar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="18b7c-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="18b7c-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="18b7c-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="18b7c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18b7c-118">-DefaultProfile</span></span>
<span data-ttu-id="18b7c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="18b7c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18b7c-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="18b7c-120">-Destination</span></span>
<span data-ttu-id="18b7c-121">Especifica o caminho do arquivo local para o qual baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="18b7c-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7c-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="18b7c-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="18b7c-123">Opcionalmente, indica o nível de log de diagnóstico a ser usado para registrar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="18b7c-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="18b7c-124">O padrão é Error.</span><span class="sxs-lookup"><span data-stu-id="18b7c-124">Default is Error.</span></span>

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

### <span data-ttu-id="18b7c-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="18b7c-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="18b7c-126">Especifica o caminho para que o log de diagnóstico registre eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="18b7c-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="18b7c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="18b7c-127">-Force</span></span>
<span data-ttu-id="18b7c-128">Indica que essa operação pode substituir o arquivo de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="18b7c-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7c-129">-Path</span><span class="sxs-lookup"><span data-stu-id="18b7c-129">-Path</span></span>
<span data-ttu-id="18b7c-130">Especifica o caminho do item a ser baixado do Data Lake Store, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="18b7c-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18b7c-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="18b7c-131">-Recurse</span></span>
<span data-ttu-id="18b7c-132">Indica que um download de pasta é recursivo.</span><span class="sxs-lookup"><span data-stu-id="18b7c-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="18b7c-133">-Resume</span><span class="sxs-lookup"><span data-stu-id="18b7c-133">-Resume</span></span>
<span data-ttu-id="18b7c-134">Indica que os arquivos que estão sendo copiados são uma continuação de um download anterior.</span><span class="sxs-lookup"><span data-stu-id="18b7c-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="18b7c-135">Isso fará com que o sistema tente retomar do último arquivo que não foi totalmente baixado.</span><span class="sxs-lookup"><span data-stu-id="18b7c-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="18b7c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="18b7c-136">-Confirm</span></span>
<span data-ttu-id="18b7c-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18b7c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18b7c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18b7c-138">-WhatIf</span></span>
<span data-ttu-id="18b7c-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18b7c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18b7c-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18b7c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18b7c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18b7c-141">CommonParameters</span></span>
<span data-ttu-id="18b7c-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18b7c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18b7c-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18b7c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18b7c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="18b7c-144">INPUTS</span></span>

### <span data-ttu-id="18b7c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="18b7c-145">System.String</span></span>

### <span data-ttu-id="18b7c-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="18b7c-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="18b7c-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18b7c-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="18b7c-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="18b7c-148">System.Int32</span></span>

### <span data-ttu-id="18b7c-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="18b7c-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="18b7c-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="18b7c-150">OUTPUTS</span></span>

### <span data-ttu-id="18b7c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="18b7c-151">System.String</span></span>

## <span data-ttu-id="18b7c-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="18b7c-152">NOTES</span></span>

## <span data-ttu-id="18b7c-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18b7c-153">RELATED LINKS</span></span>

[<span data-ttu-id="18b7c-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="18b7c-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18b7c-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


