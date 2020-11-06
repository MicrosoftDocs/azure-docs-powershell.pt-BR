---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609696"
---
# <span data-ttu-id="37ab7-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="37ab7-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="37ab7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="37ab7-103">Obtém o conteúdo de um arquivo no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="37ab7-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37ab7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37ab7-104">SYNTAX</span></span>

### <span data-ttu-id="37ab7-105">Visualizar o conteúdo do arquivo (padrão)</span><span class="sxs-lookup"><span data-stu-id="37ab7-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ab7-106">Visualizar linhas do arquivo no cabeçalho do arquivo</span><span class="sxs-lookup"><span data-stu-id="37ab7-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ab7-107">Visualizar linhas do arquivo no final do arquivo</span><span class="sxs-lookup"><span data-stu-id="37ab7-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ab7-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37ab7-108">DESCRIPTION</span></span>
<span data-ttu-id="37ab7-109">O cmdlet **Get-AzureRmDataLakeStoreItemContent** Obtém o conteúdo de um arquivo no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="37ab7-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="37ab7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37ab7-110">EXAMPLES</span></span>

### <span data-ttu-id="37ab7-111">Exemplo 1: obter o conteúdo de um arquivo</span><span class="sxs-lookup"><span data-stu-id="37ab7-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="37ab7-112">Esse comando obtém o conteúdo do arquivo MyFile.txt na conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="37ab7-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="37ab7-113">Exemplo 2: obter as duas primeiras linhas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="37ab7-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="37ab7-114">Esse comando obtém as duas primeiras linhas separadas da linha no MyFile.txt do arquivo na conta do ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="37ab7-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="37ab7-115">OS</span><span class="sxs-lookup"><span data-stu-id="37ab7-115">PARAMETERS</span></span>

### <span data-ttu-id="37ab7-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="37ab7-116">-Account</span></span>
<span data-ttu-id="37ab7-117">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="37ab7-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="37ab7-118">-Encoding</span><span class="sxs-lookup"><span data-stu-id="37ab7-118">-Encoding</span></span>
<span data-ttu-id="37ab7-119">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="37ab7-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="37ab7-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37ab7-121">Sabe</span><span class="sxs-lookup"><span data-stu-id="37ab7-121">Unknown</span></span>
- <span data-ttu-id="37ab7-122">String</span><span class="sxs-lookup"><span data-stu-id="37ab7-122">String</span></span>
- <span data-ttu-id="37ab7-123">ANSI</span><span class="sxs-lookup"><span data-stu-id="37ab7-123">Unicode</span></span>
- <span data-ttu-id="37ab7-124">Bits</span><span class="sxs-lookup"><span data-stu-id="37ab7-124">Byte</span></span>
- <span data-ttu-id="37ab7-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="37ab7-125">BigEndianUnicode</span></span>
- <span data-ttu-id="37ab7-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="37ab7-126">UTF8</span></span>
- <span data-ttu-id="37ab7-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="37ab7-127">UTF7</span></span>
- <span data-ttu-id="37ab7-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="37ab7-128">Ascii</span></span>
- <span data-ttu-id="37ab7-129">Assume</span><span class="sxs-lookup"><span data-stu-id="37ab7-129">Default</span></span>
- <span data-ttu-id="37ab7-130">Pelo</span><span class="sxs-lookup"><span data-stu-id="37ab7-130">Oem</span></span>
- <span data-ttu-id="37ab7-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="37ab7-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-132">-Force</span><span class="sxs-lookup"><span data-stu-id="37ab7-132">-Force</span></span>
<span data-ttu-id="37ab7-133">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="37ab7-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-134">-Chefe</span><span class="sxs-lookup"><span data-stu-id="37ab7-134">-Head</span></span>
<span data-ttu-id="37ab7-135">O número de linhas (delimitado por nova linha) do início do arquivo a ser visualizado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="37ab7-136">Se nenhuma linha nova for encontrada no primeiro 4MB de dados, somente os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="37ab7-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-137">-Comprimento</span><span class="sxs-lookup"><span data-stu-id="37ab7-137">-Length</span></span>
<span data-ttu-id="37ab7-138">Especifica o comprimento, em bytes, do conteúdo a obter.</span><span class="sxs-lookup"><span data-stu-id="37ab7-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-139">-Offset</span><span class="sxs-lookup"><span data-stu-id="37ab7-139">-Offset</span></span>
<span data-ttu-id="37ab7-140">Especifica o número de bytes a serem ignorados em um arquivo antes de obter conteúdo.</span><span class="sxs-lookup"><span data-stu-id="37ab7-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="37ab7-141">-Path</span></span>
<span data-ttu-id="37ab7-142">Especifica o caminho do repositório data Lake de um arquivo, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="37ab7-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="37ab7-143">-Caudal</span><span class="sxs-lookup"><span data-stu-id="37ab7-143">-Tail</span></span>
<span data-ttu-id="37ab7-144">O número de linhas (delimitado por nova linha) do final do arquivo a ser visualizado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="37ab7-145">Se nenhuma linha nova for encontrada no primeiro 4MB de dados, somente os dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="37ab7-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37ab7-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37ab7-146">-Confirm</span></span>
<span data-ttu-id="37ab7-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ab7-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ab7-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ab7-148">-WhatIf</span></span>
<span data-ttu-id="37ab7-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ab7-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ab7-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ab7-151">-DefaultProfile</span></span>
<span data-ttu-id="37ab7-152">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37ab7-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ab7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ab7-153">CommonParameters</span></span>
<span data-ttu-id="37ab7-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ab7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ab7-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ab7-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ab7-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37ab7-156">INPUTS</span></span>

## <span data-ttu-id="37ab7-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37ab7-157">OUTPUTS</span></span>

### <span data-ttu-id="37ab7-158">Byte []</span><span class="sxs-lookup"><span data-stu-id="37ab7-158">byte[]</span></span>
<span data-ttu-id="37ab7-159">A representação de fluxo de bytes do conteúdo do arquivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="37ab7-160">String</span><span class="sxs-lookup"><span data-stu-id="37ab7-160">string</span></span>
<span data-ttu-id="37ab7-161">A representação de cadeia de caracteres (na codificação especificada) do conteúdo do arquivo recuperado.</span><span class="sxs-lookup"><span data-stu-id="37ab7-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="37ab7-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37ab7-162">NOTES</span></span>

## <span data-ttu-id="37ab7-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37ab7-163">RELATED LINKS</span></span>

