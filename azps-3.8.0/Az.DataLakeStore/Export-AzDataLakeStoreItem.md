---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940510"
---
# <span data-ttu-id="5e4ea-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="5e4ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4ea-103">Baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5e4ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e4ea-104">SYNTAX</span></span>

### <span data-ttu-id="5e4ea-105">NoDiagnosticLogging (padrão)</span><span class="sxs-lookup"><span data-stu-id="5e4ea-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e4ea-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="5e4ea-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e4ea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e4ea-107">DESCRIPTION</span></span>
<span data-ttu-id="5e4ea-108">O cmdlet **Export-AzDataLakeStoreItem** baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5e4ea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e4ea-109">EXAMPLES</span></span>

### <span data-ttu-id="5e4ea-110">Exemplo 1: baixar um item do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="5e4ea-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="5e4ea-111">Esse comando baixa o arquivo TestSource.csv do data Lake Store para C:\Test.csv com uma simultaneidade de 4.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="5e4ea-112">OS</span><span class="sxs-lookup"><span data-stu-id="5e4ea-112">PARAMETERS</span></span>

### <span data-ttu-id="5e4ea-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="5e4ea-113">-Account</span></span>
<span data-ttu-id="5e4ea-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5e4ea-115">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="5e4ea-115">-Concurrency</span></span>
<span data-ttu-id="5e4ea-116">Indica o número de arquivos ou blocos a serem baixados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="5e4ea-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="5e4ea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4ea-118">-DefaultProfile</span></span>
<span data-ttu-id="5e4ea-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e4ea-120">-Destino</span><span class="sxs-lookup"><span data-stu-id="5e4ea-120">-Destination</span></span>
<span data-ttu-id="5e4ea-121">Especifica o caminho do arquivo local para o qual baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="5e4ea-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5e4ea-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5e4ea-123">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5e4ea-124">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-124">Default is Error.</span></span>

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

### <span data-ttu-id="5e4ea-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5e4ea-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="5e4ea-126">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5e4ea-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5e4ea-127">-Force</span></span>
<span data-ttu-id="5e4ea-128">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="5e4ea-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5e4ea-129">-Path</span></span>
<span data-ttu-id="5e4ea-130">Especifica o caminho do item a ser baixado do repositório data Lake, começando do diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="5e4ea-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="5e4ea-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="5e4ea-131">-Recurse</span></span>
<span data-ttu-id="5e4ea-132">Indica que um download de pasta é recursivo.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="5e4ea-133">-Retomar</span><span class="sxs-lookup"><span data-stu-id="5e4ea-133">-Resume</span></span>
<span data-ttu-id="5e4ea-134">Indica que o (s) arquivo (s) que está sendo copiado é uma continuação de um download anterior.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="5e4ea-135">Isso fará com que o sistema tente retomar o último arquivo que não foi totalmente baixado.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="5e4ea-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5e4ea-136">-Confirm</span></span>
<span data-ttu-id="5e4ea-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e4ea-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e4ea-138">-WhatIf</span></span>
<span data-ttu-id="5e4ea-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e4ea-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e4ea-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4ea-141">CommonParameters</span></span>
<span data-ttu-id="5e4ea-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e4ea-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e4ea-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4ea-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4ea-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e4ea-144">INPUTS</span></span>

### <span data-ttu-id="5e4ea-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5e4ea-145">System.String</span></span>

### <span data-ttu-id="5e4ea-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5e4ea-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5e4ea-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5e4ea-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="5e4ea-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5e4ea-148">System.Int32</span></span>

### <span data-ttu-id="5e4ea-149">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="5e4ea-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="5e4ea-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e4ea-150">OUTPUTS</span></span>

### <span data-ttu-id="5e4ea-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5e4ea-151">System.String</span></span>

## <span data-ttu-id="5e4ea-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e4ea-152">NOTES</span></span>

## <span data-ttu-id="5e4ea-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e4ea-153">RELATED LINKS</span></span>

[<span data-ttu-id="5e4ea-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-156">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-157">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="5e4ea-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5e4ea-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


