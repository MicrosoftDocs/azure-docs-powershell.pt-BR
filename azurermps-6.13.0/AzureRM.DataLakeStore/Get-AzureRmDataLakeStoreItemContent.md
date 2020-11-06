---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440060"
---
# <span data-ttu-id="44937-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="44937-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="44937-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44937-102">SYNOPSIS</span></span>
<span data-ttu-id="44937-103">Obtém o conteúdo de um arquivo no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="44937-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44937-104">SYNTAX</span></span>

### <span data-ttu-id="44937-105">PreviewFileContent (padrão)</span><span class="sxs-lookup"><span data-stu-id="44937-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44937-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="44937-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44937-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="44937-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44937-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44937-108">DESCRIPTION</span></span>
<span data-ttu-id="44937-109">O cmdlet **Get-AzureRmDataLakeStoreItemContent** Obtém o conteúdo de um arquivo no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="44937-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="44937-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44937-110">EXAMPLES</span></span>

### <span data-ttu-id="44937-111">Exemplo 1: obter o conteúdo de um arquivo</span><span class="sxs-lookup"><span data-stu-id="44937-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="44937-112">Esse comando obtém o conteúdo do arquivo MyFile.txt na conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="44937-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="44937-113">Exemplo 2: obter as duas primeiras linhas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="44937-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="44937-114">Esse comando obtém as duas primeiras linhas separadas da linha no MyFile.txt do arquivo na conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="44937-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="44937-115">OS</span><span class="sxs-lookup"><span data-stu-id="44937-115">PARAMETERS</span></span>

### <span data-ttu-id="44937-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="44937-116">-Account</span></span>
<span data-ttu-id="44937-117">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="44937-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="44937-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44937-118">-DefaultProfile</span></span>
<span data-ttu-id="44937-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44937-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44937-120">-Encoding</span><span class="sxs-lookup"><span data-stu-id="44937-120">-Encoding</span></span>
<span data-ttu-id="44937-121">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="44937-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="44937-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="44937-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44937-123">Sabe</span><span class="sxs-lookup"><span data-stu-id="44937-123">Unknown</span></span>
- <span data-ttu-id="44937-124">String</span><span class="sxs-lookup"><span data-stu-id="44937-124">String</span></span>
- <span data-ttu-id="44937-125">ANSI</span><span class="sxs-lookup"><span data-stu-id="44937-125">Unicode</span></span>
- <span data-ttu-id="44937-126">Bits</span><span class="sxs-lookup"><span data-stu-id="44937-126">Byte</span></span>
- <span data-ttu-id="44937-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="44937-127">BigEndianUnicode</span></span>
- <span data-ttu-id="44937-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="44937-128">UTF8</span></span>
- <span data-ttu-id="44937-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="44937-129">UTF7</span></span>
- <span data-ttu-id="44937-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="44937-130">Ascii</span></span>
- <span data-ttu-id="44937-131">Assume</span><span class="sxs-lookup"><span data-stu-id="44937-131">Default</span></span>
- <span data-ttu-id="44937-132">Pelo</span><span class="sxs-lookup"><span data-stu-id="44937-132">Oem</span></span>
- <span data-ttu-id="44937-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="44937-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-134">-Force</span><span class="sxs-lookup"><span data-stu-id="44937-134">-Force</span></span>
<span data-ttu-id="44937-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="44937-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-136">-Chefe</span><span class="sxs-lookup"><span data-stu-id="44937-136">-Head</span></span>
<span data-ttu-id="44937-137">O número de linhas (delimitado por nova linha) do início do arquivo a ser visualizado.</span><span class="sxs-lookup"><span data-stu-id="44937-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="44937-138">Se nenhuma linha nova for encontrada no primeiro 4MB de dados, somente os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="44937-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-139">-Comprimento</span><span class="sxs-lookup"><span data-stu-id="44937-139">-Length</span></span>
<span data-ttu-id="44937-140">Especifica o comprimento, em bytes, do conteúdo a obter.</span><span class="sxs-lookup"><span data-stu-id="44937-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="44937-141">-Offset</span></span>
<span data-ttu-id="44937-142">Especifica o número de bytes a serem ignorados em um arquivo antes de obter conteúdo.</span><span class="sxs-lookup"><span data-stu-id="44937-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-143">-Caminho</span><span class="sxs-lookup"><span data-stu-id="44937-143">-Path</span></span>
<span data-ttu-id="44937-144">Especifica o caminho do repositório data Lake de um arquivo, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="44937-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="44937-145">-Caudal</span><span class="sxs-lookup"><span data-stu-id="44937-145">-Tail</span></span>
<span data-ttu-id="44937-146">O número de linhas (delimitado por nova linha) do final do arquivo a ser visualizado.</span><span class="sxs-lookup"><span data-stu-id="44937-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="44937-147">Se nenhuma linha nova for encontrada no primeiro 4MB de dados, somente os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="44937-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44937-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44937-148">-Confirm</span></span>
<span data-ttu-id="44937-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44937-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44937-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44937-150">-WhatIf</span></span>
<span data-ttu-id="44937-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44937-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44937-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44937-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44937-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44937-153">CommonParameters</span></span>
<span data-ttu-id="44937-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44937-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44937-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44937-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44937-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44937-156">INPUTS</span></span>

### <span data-ttu-id="44937-157">System. String</span><span class="sxs-lookup"><span data-stu-id="44937-157">System.String</span></span>

### <span data-ttu-id="44937-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="44937-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="44937-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44937-159">System.Int32</span></span>

### <span data-ttu-id="44937-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="44937-160">System.Int64</span></span>

### <span data-ttu-id="44937-161">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="44937-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="44937-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="44937-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44937-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44937-163">OUTPUTS</span></span>

### <span data-ttu-id="44937-164">System. byte</span><span class="sxs-lookup"><span data-stu-id="44937-164">System.Byte</span></span>
<span data-ttu-id="44937-165">A representação de fluxo de bytes do conteúdo do arquivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="44937-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="44937-166">System. String</span><span class="sxs-lookup"><span data-stu-id="44937-166">System.String</span></span>
<span data-ttu-id="44937-167">A representação de cadeia de caracteres (na codificação especificada) do conteúdo do arquivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="44937-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="44937-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44937-168">NOTES</span></span>

## <span data-ttu-id="44937-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44937-169">RELATED LINKS</span></span>