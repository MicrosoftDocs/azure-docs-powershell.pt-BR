---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111138"
---
# <span data-ttu-id="435a6-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="435a6-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="435a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="435a6-102">SYNOPSIS</span></span>
<span data-ttu-id="435a6-103">Adiciona conteúdo a um item em um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="435a6-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="435a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="435a6-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="435a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="435a6-105">DESCRIPTION</span></span>
<span data-ttu-id="435a6-106">O cmdlet **Add-AzDataLakeStoreItemContent** adiciona conteúdo a um item em um repositório do Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="435a6-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="435a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="435a6-107">EXAMPLES</span></span>

### <span data-ttu-id="435a6-108">Exemplo 1: adicionar conteúdo a um arquivo</span><span class="sxs-lookup"><span data-stu-id="435a6-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="435a6-109">Esse comando adiciona conteúdo ao arquivo myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="435a6-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="435a6-110">OS</span><span class="sxs-lookup"><span data-stu-id="435a6-110">PARAMETERS</span></span>

### <span data-ttu-id="435a6-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="435a6-111">-Account</span></span>
<span data-ttu-id="435a6-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="435a6-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="435a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435a6-113">-DefaultProfile</span></span>
<span data-ttu-id="435a6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="435a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="435a6-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="435a6-115">-Encoding</span></span>
<span data-ttu-id="435a6-116">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="435a6-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="435a6-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="435a6-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="435a6-118">Sabe</span><span class="sxs-lookup"><span data-stu-id="435a6-118">Unknown</span></span>
- <span data-ttu-id="435a6-119">String</span><span class="sxs-lookup"><span data-stu-id="435a6-119">String</span></span>
- <span data-ttu-id="435a6-120">ANSI</span><span class="sxs-lookup"><span data-stu-id="435a6-120">Unicode</span></span>
- <span data-ttu-id="435a6-121">Bits</span><span class="sxs-lookup"><span data-stu-id="435a6-121">Byte</span></span>
- <span data-ttu-id="435a6-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="435a6-122">BigEndianUnicode</span></span>
- <span data-ttu-id="435a6-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="435a6-123">UTF8</span></span>
- <span data-ttu-id="435a6-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="435a6-124">UTF7</span></span>
- <span data-ttu-id="435a6-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="435a6-125">Ascii</span></span>
- <span data-ttu-id="435a6-126">Assume</span><span class="sxs-lookup"><span data-stu-id="435a6-126">Default</span></span>
- <span data-ttu-id="435a6-127">Pelo</span><span class="sxs-lookup"><span data-stu-id="435a6-127">Oem</span></span>
- <span data-ttu-id="435a6-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="435a6-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="435a6-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="435a6-129">-Path</span></span>
<span data-ttu-id="435a6-130">Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="435a6-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="435a6-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="435a6-131">-Value</span></span>
<span data-ttu-id="435a6-132">Especifica o conteúdo a ser adicionado ao item.</span><span class="sxs-lookup"><span data-stu-id="435a6-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="435a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435a6-133">CommonParameters</span></span>
<span data-ttu-id="435a6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="435a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435a6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435a6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435a6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="435a6-136">INPUTS</span></span>

### <span data-ttu-id="435a6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="435a6-137">System.String</span></span>

### <span data-ttu-id="435a6-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="435a6-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="435a6-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="435a6-139">System.Object</span></span>

### <span data-ttu-id="435a6-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="435a6-140">System.Text.Encoding</span></span>

## <span data-ttu-id="435a6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="435a6-141">OUTPUTS</span></span>

### <span data-ttu-id="435a6-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="435a6-142">System.Boolean</span></span>

## <span data-ttu-id="435a6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="435a6-143">NOTES</span></span>

## <span data-ttu-id="435a6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="435a6-144">RELATED LINKS</span></span>

[<span data-ttu-id="435a6-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="435a6-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


