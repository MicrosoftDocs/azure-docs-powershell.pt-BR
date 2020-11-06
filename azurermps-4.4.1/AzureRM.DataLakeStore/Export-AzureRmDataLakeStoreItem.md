---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433153"
---
# <span data-ttu-id="66b10-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="66b10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66b10-102">SYNOPSIS</span></span>
<span data-ttu-id="66b10-103">Baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b10-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66b10-104">SYNTAX</span></span>

### <span data-ttu-id="66b10-105">Sem log de diagnóstico (padrão)</span><span class="sxs-lookup"><span data-stu-id="66b10-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66b10-106">Incluir log de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="66b10-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66b10-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66b10-107">DESCRIPTION</span></span>
<span data-ttu-id="66b10-108">O cmdlet **Export-AzureRmDataLakeStoreItem** baixa um arquivo do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b10-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="66b10-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66b10-109">EXAMPLES</span></span>

### <span data-ttu-id="66b10-110">Exemplo 1: baixar um item do repositório data Lake</span><span class="sxs-lookup"><span data-stu-id="66b10-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="66b10-111">Esse comando baixa o arquivo TestSource.csv do data Lake Store para C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="66b10-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="66b10-112">OS</span><span class="sxs-lookup"><span data-stu-id="66b10-112">PARAMETERS</span></span>

### <span data-ttu-id="66b10-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="66b10-113">-Account</span></span>
<span data-ttu-id="66b10-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b10-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="66b10-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="66b10-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="66b10-116">Especifica o número máximo de arquivos a serem baixados em paralelo para um download de pasta.</span><span class="sxs-lookup"><span data-stu-id="66b10-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="66b10-117">O valor padrão é cinco (5).</span><span class="sxs-lookup"><span data-stu-id="66b10-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="66b10-118">-Destino</span><span class="sxs-lookup"><span data-stu-id="66b10-118">-Destination</span></span>
<span data-ttu-id="66b10-119">Especifica o caminho do arquivo local para o qual baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="66b10-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="66b10-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="66b10-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="66b10-121">Opcionalmente, indica o nível de log de diagnóstico a ser usado para gravar eventos durante a importação do arquivo ou da pasta.</span><span class="sxs-lookup"><span data-stu-id="66b10-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="66b10-122">O padrão é erro.</span><span class="sxs-lookup"><span data-stu-id="66b10-122">Default is Error.</span></span>

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

### <span data-ttu-id="66b10-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="66b10-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="66b10-124">Especifica o caminho para o log de diagnóstico no qual gravar eventos durante a importação de arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="66b10-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="66b10-125">-Force</span><span class="sxs-lookup"><span data-stu-id="66b10-125">-Force</span></span>
<span data-ttu-id="66b10-126">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="66b10-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="66b10-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="66b10-127">-Path</span></span>
<span data-ttu-id="66b10-128">Especifica o caminho do item a ser baixado do repositório data Lake, começando do diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="66b10-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="66b10-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="66b10-129">-PerFileThreadCount</span></span>
<span data-ttu-id="66b10-130">Especifica o número máximo de threads a serem usados por arquivo.</span><span class="sxs-lookup"><span data-stu-id="66b10-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="66b10-131">O valor padrão é 10 (10).</span><span class="sxs-lookup"><span data-stu-id="66b10-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b10-132">-Recurse</span><span class="sxs-lookup"><span data-stu-id="66b10-132">-Recurse</span></span>
<span data-ttu-id="66b10-133">Indica que um download de pasta é recursivo.</span><span class="sxs-lookup"><span data-stu-id="66b10-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="66b10-134">-Retomar</span><span class="sxs-lookup"><span data-stu-id="66b10-134">-Resume</span></span>
<span data-ttu-id="66b10-135">Indica que o arquivo ou arquivos que estão sendo copiados são uma continuação de um download anterior.</span><span class="sxs-lookup"><span data-stu-id="66b10-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="66b10-136">O download tenta continuar a partir do último arquivo que não foi totalmente baixado.</span><span class="sxs-lookup"><span data-stu-id="66b10-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="66b10-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="66b10-137">-Confirm</span></span>
<span data-ttu-id="66b10-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b10-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66b10-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66b10-139">-WhatIf</span></span>
<span data-ttu-id="66b10-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66b10-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66b10-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66b10-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66b10-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b10-142">-DefaultProfile</span></span>
<span data-ttu-id="66b10-143">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66b10-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b10-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b10-144">CommonParameters</span></span>
<span data-ttu-id="66b10-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b10-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b10-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b10-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b10-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66b10-147">INPUTS</span></span>

## <span data-ttu-id="66b10-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66b10-148">OUTPUTS</span></span>

### <span data-ttu-id="66b10-149">String</span><span class="sxs-lookup"><span data-stu-id="66b10-149">string</span></span>
<span data-ttu-id="66b10-150">O caminho no qual o arquivo ou a pasta foi baixada.</span><span class="sxs-lookup"><span data-stu-id="66b10-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="66b10-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66b10-151">NOTES</span></span>

## <span data-ttu-id="66b10-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66b10-152">RELATED LINKS</span></span>

[<span data-ttu-id="66b10-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-154">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-155">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-156">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="66b10-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="66b10-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


