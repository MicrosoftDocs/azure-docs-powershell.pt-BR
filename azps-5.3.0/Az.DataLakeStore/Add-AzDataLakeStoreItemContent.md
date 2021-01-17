---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429823"
---
# <span data-ttu-id="2ddc3-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2ddc3-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="2ddc3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ddc3-102">SYNOPSIS</span></span>
<span data-ttu-id="2ddc3-103">Adiciona conteúdo a um item em um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="2ddc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ddc3-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ddc3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ddc3-105">DESCRIPTION</span></span>
<span data-ttu-id="2ddc3-106">O cmdlet **Add-AzDataLakeStoreItemContent** adiciona conteúdo a um item em um repositório do Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="2ddc3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ddc3-107">EXAMPLES</span></span>

### <span data-ttu-id="2ddc3-108">Exemplo 1: adicionar conteúdo a um arquivo</span><span class="sxs-lookup"><span data-stu-id="2ddc3-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="2ddc3-109">Esse comando adiciona conteúdo ao arquivo myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="2ddc3-110">OS</span><span class="sxs-lookup"><span data-stu-id="2ddc3-110">PARAMETERS</span></span>

### <span data-ttu-id="2ddc3-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="2ddc3-111">-Account</span></span>
<span data-ttu-id="2ddc3-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2ddc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ddc3-113">-DefaultProfile</span></span>
<span data-ttu-id="2ddc3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2ddc3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ddc3-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="2ddc3-115">-Encoding</span></span>
<span data-ttu-id="2ddc3-116">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="2ddc3-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2ddc3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ddc3-118">Sabe</span><span class="sxs-lookup"><span data-stu-id="2ddc3-118">Unknown</span></span>
- <span data-ttu-id="2ddc3-119">String</span><span class="sxs-lookup"><span data-stu-id="2ddc3-119">String</span></span>
- <span data-ttu-id="2ddc3-120">ANSI</span><span class="sxs-lookup"><span data-stu-id="2ddc3-120">Unicode</span></span>
- <span data-ttu-id="2ddc3-121">Bits</span><span class="sxs-lookup"><span data-stu-id="2ddc3-121">Byte</span></span>
- <span data-ttu-id="2ddc3-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="2ddc3-122">BigEndianUnicode</span></span>
- <span data-ttu-id="2ddc3-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="2ddc3-123">UTF8</span></span>
- <span data-ttu-id="2ddc3-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="2ddc3-124">UTF7</span></span>
- <span data-ttu-id="2ddc3-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="2ddc3-125">Ascii</span></span>
- <span data-ttu-id="2ddc3-126">Assume</span><span class="sxs-lookup"><span data-stu-id="2ddc3-126">Default</span></span>
- <span data-ttu-id="2ddc3-127">Pelo</span><span class="sxs-lookup"><span data-stu-id="2ddc3-127">Oem</span></span>
- <span data-ttu-id="2ddc3-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="2ddc3-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="2ddc3-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2ddc3-129">-Path</span></span>
<span data-ttu-id="2ddc3-130">Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="2ddc3-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2ddc3-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="2ddc3-131">-Value</span></span>
<span data-ttu-id="2ddc3-132">Especifica o conteúdo a ser adicionado ao item.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="2ddc3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ddc3-133">CommonParameters</span></span>
<span data-ttu-id="2ddc3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ddc3-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ddc3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ddc3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ddc3-136">INPUTS</span></span>

### <span data-ttu-id="2ddc3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2ddc3-137">System.String</span></span>

### <span data-ttu-id="2ddc3-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2ddc3-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2ddc3-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="2ddc3-139">System.Object</span></span>

### <span data-ttu-id="2ddc3-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="2ddc3-140">System.Text.Encoding</span></span>

## <span data-ttu-id="2ddc3-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ddc3-141">OUTPUTS</span></span>

### <span data-ttu-id="2ddc3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2ddc3-142">System.Boolean</span></span>

## <span data-ttu-id="2ddc3-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ddc3-143">NOTES</span></span>

## <span data-ttu-id="2ddc3-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ddc3-144">RELATED LINKS</span></span>

[<span data-ttu-id="2ddc3-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="2ddc3-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


