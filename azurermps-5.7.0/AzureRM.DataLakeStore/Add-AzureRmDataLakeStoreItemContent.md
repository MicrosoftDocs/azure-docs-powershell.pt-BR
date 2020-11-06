---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: f272d7c57a1543f916d828d6324dd23f5780ccad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602656"
---
# <span data-ttu-id="cc0da-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="cc0da-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="cc0da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc0da-102">SYNOPSIS</span></span>
<span data-ttu-id="cc0da-103">Adiciona conteúdo a um item em um repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="cc0da-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc0da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc0da-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc0da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc0da-105">DESCRIPTION</span></span>
<span data-ttu-id="cc0da-106">O cmdlet **Add-AzureRmDataLakeStoreItemContent** adiciona conteúdo a um item em um repositório do Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="cc0da-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="cc0da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc0da-107">EXAMPLES</span></span>

### <span data-ttu-id="cc0da-108">Exemplo 1: adicionar conteúdo a um arquivo</span><span class="sxs-lookup"><span data-stu-id="cc0da-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="cc0da-109">Esse comando adiciona conteúdo ao arquivo myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="cc0da-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="cc0da-110">OS</span><span class="sxs-lookup"><span data-stu-id="cc0da-110">PARAMETERS</span></span>

### <span data-ttu-id="cc0da-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="cc0da-111">-Account</span></span>
<span data-ttu-id="cc0da-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cc0da-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc0da-113">-DefaultProfile</span></span>
<span data-ttu-id="cc0da-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cc0da-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc0da-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="cc0da-115">-Encoding</span></span>
<span data-ttu-id="cc0da-116">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="cc0da-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="cc0da-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cc0da-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc0da-118">Sabe</span><span class="sxs-lookup"><span data-stu-id="cc0da-118">Unknown</span></span>
- <span data-ttu-id="cc0da-119">String</span><span class="sxs-lookup"><span data-stu-id="cc0da-119">String</span></span>
- <span data-ttu-id="cc0da-120">ANSI</span><span class="sxs-lookup"><span data-stu-id="cc0da-120">Unicode</span></span>
- <span data-ttu-id="cc0da-121">Bits</span><span class="sxs-lookup"><span data-stu-id="cc0da-121">Byte</span></span>
- <span data-ttu-id="cc0da-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="cc0da-122">BigEndianUnicode</span></span>
- <span data-ttu-id="cc0da-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="cc0da-123">UTF8</span></span>
- <span data-ttu-id="cc0da-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="cc0da-124">UTF7</span></span>
- <span data-ttu-id="cc0da-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="cc0da-125">Ascii</span></span>
- <span data-ttu-id="cc0da-126">Assume</span><span class="sxs-lookup"><span data-stu-id="cc0da-126">Default</span></span>
- <span data-ttu-id="cc0da-127">Pelo</span><span class="sxs-lookup"><span data-stu-id="cc0da-127">Oem</span></span>
- <span data-ttu-id="cc0da-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="cc0da-128">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0da-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="cc0da-129">-Path</span></span>
<span data-ttu-id="cc0da-130">Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="cc0da-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0da-131">-Valor</span><span class="sxs-lookup"><span data-stu-id="cc0da-131">-Value</span></span>
<span data-ttu-id="cc0da-132">Especifica o conteúdo a ser adicionado ao item.</span><span class="sxs-lookup"><span data-stu-id="cc0da-132">Specifies the content to add to the item.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc0da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc0da-133">CommonParameters</span></span>
<span data-ttu-id="cc0da-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc0da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc0da-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc0da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc0da-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc0da-136">INPUTS</span></span>

### <span data-ttu-id="cc0da-137">Objeto</span><span class="sxs-lookup"><span data-stu-id="cc0da-137">Object</span></span>
<span data-ttu-id="cc0da-138">O parâmetro ' value ' aceita o valor do tipo ' Object ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="cc0da-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="cc0da-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc0da-139">OUTPUTS</span></span>

### <span data-ttu-id="cc0da-140">bool</span><span class="sxs-lookup"><span data-stu-id="cc0da-140">bool</span></span>
<span data-ttu-id="cc0da-141">Retorna verdadeiro no sucesso.</span><span class="sxs-lookup"><span data-stu-id="cc0da-141">Returns true on success.</span></span>

## <span data-ttu-id="cc0da-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc0da-142">NOTES</span></span>

## <span data-ttu-id="cc0da-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc0da-143">RELATED LINKS</span></span>

[<span data-ttu-id="cc0da-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="cc0da-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


