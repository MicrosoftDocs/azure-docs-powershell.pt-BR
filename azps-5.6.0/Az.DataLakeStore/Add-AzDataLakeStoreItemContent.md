---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890864"
---
# <span data-ttu-id="b53ec-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b53ec-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="b53ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b53ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b53ec-103">Adiciona conteúdo a um item em um Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b53ec-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="b53ec-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b53ec-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b53ec-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b53ec-105">DESCRIPTION</span></span>
<span data-ttu-id="b53ec-106">O cmdlet **Add-AzDataLakeStoreItemContent** adiciona conteúdo a um item em um Repositório do Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="b53ec-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="b53ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b53ec-107">EXAMPLES</span></span>

### <span data-ttu-id="b53ec-108">Exemplo 1: Adicionar conteúdo a um arquivo</span><span class="sxs-lookup"><span data-stu-id="b53ec-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="b53ec-109">Este comando adiciona conteúdo ao arquivo myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="b53ec-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="b53ec-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b53ec-110">PARAMETERS</span></span>

### <span data-ttu-id="b53ec-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b53ec-111">-Account</span></span>
<span data-ttu-id="b53ec-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b53ec-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="b53ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b53ec-113">-DefaultProfile</span></span>
<span data-ttu-id="b53ec-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b53ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b53ec-115">-Codificação</span><span class="sxs-lookup"><span data-stu-id="b53ec-115">-Encoding</span></span>
<span data-ttu-id="b53ec-116">Especifica a codificação do item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b53ec-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="b53ec-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b53ec-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b53ec-118">Desconhecido</span><span class="sxs-lookup"><span data-stu-id="b53ec-118">Unknown</span></span>
- <span data-ttu-id="b53ec-119">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="b53ec-119">String</span></span>
- <span data-ttu-id="b53ec-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="b53ec-120">Unicode</span></span>
- <span data-ttu-id="b53ec-121">Byte</span><span class="sxs-lookup"><span data-stu-id="b53ec-121">Byte</span></span>
- <span data-ttu-id="b53ec-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="b53ec-122">BigEndianUnicode</span></span>
- <span data-ttu-id="b53ec-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="b53ec-123">UTF8</span></span>
- <span data-ttu-id="b53ec-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="b53ec-124">UTF7</span></span>
- <span data-ttu-id="b53ec-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="b53ec-125">Ascii</span></span>
- <span data-ttu-id="b53ec-126">Padrão</span><span class="sxs-lookup"><span data-stu-id="b53ec-126">Default</span></span>
- <span data-ttu-id="b53ec-127">Oem</span><span class="sxs-lookup"><span data-stu-id="b53ec-127">Oem</span></span>
- <span data-ttu-id="b53ec-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="b53ec-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="b53ec-129">-Path</span><span class="sxs-lookup"><span data-stu-id="b53ec-129">-Path</span></span>
<span data-ttu-id="b53ec-130">Especifica o caminho do Data Lake Store do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="b53ec-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="b53ec-131">-Value</span><span class="sxs-lookup"><span data-stu-id="b53ec-131">-Value</span></span>
<span data-ttu-id="b53ec-132">Especifica o conteúdo a ser acrescentado ao item.</span><span class="sxs-lookup"><span data-stu-id="b53ec-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="b53ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b53ec-133">CommonParameters</span></span>
<span data-ttu-id="b53ec-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b53ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b53ec-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b53ec-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b53ec-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b53ec-136">INPUTS</span></span>

### <span data-ttu-id="b53ec-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b53ec-137">System.String</span></span>

### <span data-ttu-id="b53ec-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b53ec-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b53ec-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="b53ec-139">System.Object</span></span>

### <span data-ttu-id="b53ec-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="b53ec-140">System.Text.Encoding</span></span>

## <span data-ttu-id="b53ec-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b53ec-141">OUTPUTS</span></span>

### <span data-ttu-id="b53ec-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b53ec-142">System.Boolean</span></span>

## <span data-ttu-id="b53ec-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="b53ec-143">NOTES</span></span>

## <span data-ttu-id="b53ec-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b53ec-144">RELATED LINKS</span></span>

[<span data-ttu-id="b53ec-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="b53ec-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


