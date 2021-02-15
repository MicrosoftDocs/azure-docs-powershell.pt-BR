---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115390"
---
# <span data-ttu-id="6e7fa-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6e7fa-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="6e7fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e7fa-102">SYNOPSIS</span></span>
<span data-ttu-id="6e7fa-103">Adiciona conteúdo a um item em um Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="6e7fa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e7fa-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e7fa-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6e7fa-105">DESCRIPTION</span></span>
<span data-ttu-id="6e7fa-106">O cmdlet **Add-AzDataLakeStoreItemContent** adiciona conteúdo a um item em um Repositório de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="6e7fa-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e7fa-107">EXAMPLES</span></span>

### <span data-ttu-id="6e7fa-108">Exemplo 1: Adicionar conteúdo a um arquivo</span><span class="sxs-lookup"><span data-stu-id="6e7fa-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="6e7fa-109">Esse comando adiciona conteúdo ao arquivo myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="6e7fa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e7fa-110">PARAMETERS</span></span>

### <span data-ttu-id="6e7fa-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="6e7fa-111">-Account</span></span>
<span data-ttu-id="6e7fa-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6e7fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e7fa-113">-DefaultProfile</span></span>
<span data-ttu-id="6e7fa-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6e7fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e7fa-115">-Codificação</span><span class="sxs-lookup"><span data-stu-id="6e7fa-115">-Encoding</span></span>
<span data-ttu-id="6e7fa-116">Especifica a codificação do item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="6e7fa-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e7fa-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e7fa-118">Desconhecido</span><span class="sxs-lookup"><span data-stu-id="6e7fa-118">Unknown</span></span>
- <span data-ttu-id="6e7fa-119">String</span><span class="sxs-lookup"><span data-stu-id="6e7fa-119">String</span></span>
- <span data-ttu-id="6e7fa-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="6e7fa-120">Unicode</span></span>
- <span data-ttu-id="6e7fa-121">Byte</span><span class="sxs-lookup"><span data-stu-id="6e7fa-121">Byte</span></span>
- <span data-ttu-id="6e7fa-122">Bigendianunicode</span><span class="sxs-lookup"><span data-stu-id="6e7fa-122">BigEndianUnicode</span></span>
- <span data-ttu-id="6e7fa-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="6e7fa-123">UTF8</span></span>
- <span data-ttu-id="6e7fa-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="6e7fa-124">UTF7</span></span>
- <span data-ttu-id="6e7fa-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="6e7fa-125">Ascii</span></span>
- <span data-ttu-id="6e7fa-126">Padrão</span><span class="sxs-lookup"><span data-stu-id="6e7fa-126">Default</span></span>
- <span data-ttu-id="6e7fa-127">Oem</span><span class="sxs-lookup"><span data-stu-id="6e7fa-127">Oem</span></span>
- <span data-ttu-id="6e7fa-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="6e7fa-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7fa-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="6e7fa-129">-Path</span></span>
<span data-ttu-id="6e7fa-130">Especifica o caminho do Data Lake Store do item a ser modificado, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="6e7fa-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6e7fa-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="6e7fa-131">-Value</span></span>
<span data-ttu-id="6e7fa-132">Especifica o conteúdo a ser acrescentado ao item.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e7fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e7fa-133">CommonParameters</span></span>
<span data-ttu-id="6e7fa-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e7fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e7fa-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e7fa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e7fa-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="6e7fa-136">INPUTS</span></span>

### <span data-ttu-id="6e7fa-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6e7fa-137">System.String</span></span>

### <span data-ttu-id="6e7fa-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6e7fa-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6e7fa-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="6e7fa-139">System.Object</span></span>

### <span data-ttu-id="6e7fa-140">Codificação system.text.text</span><span class="sxs-lookup"><span data-stu-id="6e7fa-140">System.Text.Encoding</span></span>

## <span data-ttu-id="6e7fa-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="6e7fa-141">OUTPUTS</span></span>

### <span data-ttu-id="6e7fa-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6e7fa-142">System.Boolean</span></span>

## <span data-ttu-id="6e7fa-143">Notas</span><span class="sxs-lookup"><span data-stu-id="6e7fa-143">NOTES</span></span>

## <span data-ttu-id="6e7fa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e7fa-144">RELATED LINKS</span></span>

[<span data-ttu-id="6e7fa-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="6e7fa-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


