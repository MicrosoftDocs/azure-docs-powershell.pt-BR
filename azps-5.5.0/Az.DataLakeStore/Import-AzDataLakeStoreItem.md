---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117724"
---
# <span data-ttu-id="46c0a-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="46c0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="46c0a-103">Carrega um arquivo ou diretório local em uma Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46c0a-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="46c0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46c0a-104">SYNTAX</span></span>

### <span data-ttu-id="46c0a-105">NoDiagnosticLogging (Padrão)</span><span class="sxs-lookup"><span data-stu-id="46c0a-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46c0a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="46c0a-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46c0a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="46c0a-107">DESCRIPTION</span></span>
<span data-ttu-id="46c0a-108">O cmdlet **Import-AzDataLakeStoreItem** carrega um arquivo ou diretório local em uma Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46c0a-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="46c0a-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46c0a-109">EXAMPLES</span></span>

### <span data-ttu-id="46c0a-110">Exemplo 1: Carregar um arquivo</span><span class="sxs-lookup"><span data-stu-id="46c0a-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="46c0a-111">Esse comando carrega o arquivo SrcFile.csv e o adiciona à pasta MeusArquivos no Data Lake Store como File.csv com uma simultância de 4.</span><span class="sxs-lookup"><span data-stu-id="46c0a-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="46c0a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46c0a-112">PARAMETERS</span></span>

### <span data-ttu-id="46c0a-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="46c0a-113">-Account</span></span>
<span data-ttu-id="46c0a-114">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="46c0a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="46c0a-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="46c0a-115">-Concurrency</span></span>
<span data-ttu-id="46c0a-116">Indica o número de arquivos ou blocos a carregar em paralelo.</span><span class="sxs-lookup"><span data-stu-id="46c0a-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="46c0a-117">O padrão será calculado como um melhor esforço com base nas especificações do sistema.</span><span class="sxs-lookup"><span data-stu-id="46c0a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="46c0a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c0a-118">-DefaultProfile</span></span>
<span data-ttu-id="46c0a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="46c0a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46c0a-120">-Destino</span><span class="sxs-lookup"><span data-stu-id="46c0a-120">-Destination</span></span>
<span data-ttu-id="46c0a-121">Especifica o caminho da Data Lake Store para o qual carregar um arquivo ou pasta, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="46c0a-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="46c0a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="46c0a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="46c0a-123">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="46c0a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="46c0a-124">O padrão é Erro.</span><span class="sxs-lookup"><span data-stu-id="46c0a-124">Default is Error.</span></span>

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

### <span data-ttu-id="46c0a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="46c0a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="46c0a-126">Especifica o caminho para o log de diagnóstico para o registro de eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="46c0a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="46c0a-127">-Forçar</span><span class="sxs-lookup"><span data-stu-id="46c0a-127">-Force</span></span>
<span data-ttu-id="46c0a-128">Indica que essa operação pode substituir o arquivo de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="46c0a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="46c0a-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="46c0a-129">-ForceBinary</span></span>
<span data-ttu-id="46c0a-130">Indica que os arquivos que estão sendo copiados devem ser copiados sem se preocupar com a preservação de novas linhas entre os anexados.</span><span class="sxs-lookup"><span data-stu-id="46c0a-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="46c0a-131">-Caminho</span><span class="sxs-lookup"><span data-stu-id="46c0a-131">-Path</span></span>
<span data-ttu-id="46c0a-132">Especifica o caminho local do arquivo ou pasta a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="46c0a-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="46c0a-133">-Recorrência</span><span class="sxs-lookup"><span data-stu-id="46c0a-133">-Recurse</span></span>
<span data-ttu-id="46c0a-134">Indica que essa operação deve carregar todos os itens em todas as subpastas.</span><span class="sxs-lookup"><span data-stu-id="46c0a-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="46c0a-135">-Currículo</span><span class="sxs-lookup"><span data-stu-id="46c0a-135">-Resume</span></span>
<span data-ttu-id="46c0a-136">Indica que os arquivos que estão sendo copiados são uma continuação de um carregamento anterior.</span><span class="sxs-lookup"><span data-stu-id="46c0a-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="46c0a-137">Isso fará com que o sistema tente retomar do último arquivo que não foi totalmente carregado.</span><span class="sxs-lookup"><span data-stu-id="46c0a-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="46c0a-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="46c0a-138">-Confirm</span></span>
<span data-ttu-id="46c0a-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c0a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c0a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c0a-140">-WhatIf</span></span>
<span data-ttu-id="46c0a-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="46c0a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c0a-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46c0a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c0a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c0a-143">CommonParameters</span></span>
<span data-ttu-id="46c0a-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c0a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c0a-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46c0a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c0a-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="46c0a-146">INPUTS</span></span>

### <span data-ttu-id="46c0a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="46c0a-147">System.String</span></span>

### <span data-ttu-id="46c0a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="46c0a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="46c0a-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="46c0a-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="46c0a-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="46c0a-150">System.Int32</span></span>

### <span data-ttu-id="46c0a-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="46c0a-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="46c0a-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="46c0a-152">OUTPUTS</span></span>

### <span data-ttu-id="46c0a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="46c0a-153">System.String</span></span>

## <span data-ttu-id="46c0a-154">Notas</span><span class="sxs-lookup"><span data-stu-id="46c0a-154">NOTES</span></span>

## <span data-ttu-id="46c0a-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46c0a-155">RELATED LINKS</span></span>

[<span data-ttu-id="46c0a-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="46c0a-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="46c0a-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


