---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 8f128396982be5e461e450d320c0264dddb09fa8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886679"
---
# <span data-ttu-id="0afbb-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="0afbb-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="0afbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afbb-102">SYNOPSIS</span></span>
<span data-ttu-id="0afbb-103">Obtém o conteúdo de um arquivo no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0afbb-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="0afbb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0afbb-104">SYNTAX</span></span>

### <span data-ttu-id="0afbb-105">PreviewFileContent (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0afbb-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afbb-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="0afbb-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afbb-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="0afbb-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afbb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0afbb-108">DESCRIPTION</span></span>
<span data-ttu-id="0afbb-109">O cmdlet **Get-AzDataLakeStoreItemContent** obtém o conteúdo de um arquivo no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0afbb-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="0afbb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0afbb-110">EXAMPLES</span></span>

### <span data-ttu-id="0afbb-111">Exemplo 1: Obter o conteúdo de um arquivo</span><span class="sxs-lookup"><span data-stu-id="0afbb-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="0afbb-112">Este comando obtém o conteúdo do arquivo MyFile.txt na conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0afbb-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="0afbb-113">Exemplo 2: Obter as duas primeiras linhas de um arquivo</span><span class="sxs-lookup"><span data-stu-id="0afbb-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="0afbb-114">Este comando obtém as duas primeiras linhas separadas de linha no arquivo MyFile.txt na conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="0afbb-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="0afbb-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0afbb-115">PARAMETERS</span></span>

### <span data-ttu-id="0afbb-116">-Account</span><span class="sxs-lookup"><span data-stu-id="0afbb-116">-Account</span></span>
<span data-ttu-id="0afbb-117">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0afbb-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0afbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afbb-118">-DefaultProfile</span></span>
<span data-ttu-id="0afbb-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0afbb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0afbb-120">-Codificação</span><span class="sxs-lookup"><span data-stu-id="0afbb-120">-Encoding</span></span>
<span data-ttu-id="0afbb-121">Especifica a codificação do item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0afbb-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="0afbb-122">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0afbb-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0afbb-123">Desconhecido</span><span class="sxs-lookup"><span data-stu-id="0afbb-123">Unknown</span></span>
- <span data-ttu-id="0afbb-124">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="0afbb-124">String</span></span>
- <span data-ttu-id="0afbb-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="0afbb-125">Unicode</span></span>
- <span data-ttu-id="0afbb-126">Byte</span><span class="sxs-lookup"><span data-stu-id="0afbb-126">Byte</span></span>
- <span data-ttu-id="0afbb-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="0afbb-127">BigEndianUnicode</span></span>
- <span data-ttu-id="0afbb-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="0afbb-128">UTF8</span></span>
- <span data-ttu-id="0afbb-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="0afbb-129">UTF7</span></span>
- <span data-ttu-id="0afbb-130">Ascii</span><span class="sxs-lookup"><span data-stu-id="0afbb-130">Ascii</span></span>
- <span data-ttu-id="0afbb-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="0afbb-131">Default</span></span>
- <span data-ttu-id="0afbb-132">Oem</span><span class="sxs-lookup"><span data-stu-id="0afbb-132">Oem</span></span>
- <span data-ttu-id="0afbb-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="0afbb-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afbb-134">-Force</span><span class="sxs-lookup"><span data-stu-id="0afbb-134">-Force</span></span>
<span data-ttu-id="0afbb-135">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0afbb-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0afbb-136">-Head</span><span class="sxs-lookup"><span data-stu-id="0afbb-136">-Head</span></span>
<span data-ttu-id="0afbb-137">O número de linhas (nova linha delimitada) do início do arquivo para a visualização.</span><span class="sxs-lookup"><span data-stu-id="0afbb-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="0afbb-138">Se nenhuma nova linha for encontrada nos primeiros 4 mb de dados, somente esses dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="0afbb-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="0afbb-139">-Length</span><span class="sxs-lookup"><span data-stu-id="0afbb-139">-Length</span></span>
<span data-ttu-id="0afbb-140">Especifica o comprimento, em bytes, do conteúdo a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="0afbb-140">Specifies the length, in bytes, of the content to get.</span></span>

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

### <span data-ttu-id="0afbb-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="0afbb-141">-Offset</span></span>
<span data-ttu-id="0afbb-142">Especifica o número de bytes a ignorar em um arquivo antes de obter conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0afbb-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

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

### <span data-ttu-id="0afbb-143">-Path</span><span class="sxs-lookup"><span data-stu-id="0afbb-143">-Path</span></span>
<span data-ttu-id="0afbb-144">Especifica o caminho do Data Lake Store de um arquivo, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="0afbb-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0afbb-145">-Tail</span><span class="sxs-lookup"><span data-stu-id="0afbb-145">-Tail</span></span>
<span data-ttu-id="0afbb-146">O número de linhas (nova linha delimitada) do final do arquivo para a visualização.</span><span class="sxs-lookup"><span data-stu-id="0afbb-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="0afbb-147">Se nenhuma nova linha for encontrada nos primeiros 4 mb de dados, somente esses dados serão retornados.</span><span class="sxs-lookup"><span data-stu-id="0afbb-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

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

### <span data-ttu-id="0afbb-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0afbb-148">-Confirm</span></span>
<span data-ttu-id="0afbb-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0afbb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afbb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afbb-150">-WhatIf</span></span>
<span data-ttu-id="0afbb-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0afbb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0afbb-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0afbb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afbb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afbb-153">CommonParameters</span></span>
<span data-ttu-id="0afbb-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0afbb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afbb-155">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afbb-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afbb-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0afbb-156">INPUTS</span></span>

### <span data-ttu-id="0afbb-157">System.String</span><span class="sxs-lookup"><span data-stu-id="0afbb-157">System.String</span></span>

### <span data-ttu-id="0afbb-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0afbb-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0afbb-159">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0afbb-159">System.Int32</span></span>

### <span data-ttu-id="0afbb-160">System.Int64</span><span class="sxs-lookup"><span data-stu-id="0afbb-160">System.Int64</span></span>

### <span data-ttu-id="0afbb-161">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="0afbb-161">System.Text.Encoding</span></span>

### <span data-ttu-id="0afbb-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0afbb-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0afbb-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0afbb-163">OUTPUTS</span></span>

### <span data-ttu-id="0afbb-164">System.Byte</span><span class="sxs-lookup"><span data-stu-id="0afbb-164">System.Byte</span></span>

### <span data-ttu-id="0afbb-165">System.String</span><span class="sxs-lookup"><span data-stu-id="0afbb-165">System.String</span></span>

## <span data-ttu-id="0afbb-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="0afbb-166">NOTES</span></span>

## <span data-ttu-id="0afbb-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0afbb-167">RELATED LINKS</span></span>
