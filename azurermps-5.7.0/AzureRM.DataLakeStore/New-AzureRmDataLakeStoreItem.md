---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427564"
---
# <span data-ttu-id="8db78-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="8db78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8db78-102">SYNOPSIS</span></span>
<span data-ttu-id="8db78-103">Cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8db78-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8db78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8db78-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8db78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8db78-105">DESCRIPTION</span></span>
<span data-ttu-id="8db78-106">O cmdlet **New-AzureRmDataLakeStoreItem** cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8db78-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8db78-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8db78-107">EXAMPLES</span></span>

### <span data-ttu-id="8db78-108">Exemplo 1: criar um novo arquivo e uma nova pasta</span><span class="sxs-lookup"><span data-stu-id="8db78-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="8db78-109">O primeiro comando cria o NewFile.txt de arquivo para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="8db78-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="8db78-110">O segundo comando cria a pasta NewFolder na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="8db78-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="8db78-111">OS</span><span class="sxs-lookup"><span data-stu-id="8db78-111">PARAMETERS</span></span>

### <span data-ttu-id="8db78-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="8db78-112">-Account</span></span>
<span data-ttu-id="8db78-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8db78-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8db78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8db78-114">-DefaultProfile</span></span>
<span data-ttu-id="8db78-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8db78-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8db78-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="8db78-116">-Encoding</span></span>
<span data-ttu-id="8db78-117">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8db78-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="8db78-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8db78-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8db78-119">Sabe</span><span class="sxs-lookup"><span data-stu-id="8db78-119">Unknown</span></span>
- <span data-ttu-id="8db78-120">String</span><span class="sxs-lookup"><span data-stu-id="8db78-120">String</span></span>
- <span data-ttu-id="8db78-121">ANSI</span><span class="sxs-lookup"><span data-stu-id="8db78-121">Unicode</span></span>
- <span data-ttu-id="8db78-122">Bits</span><span class="sxs-lookup"><span data-stu-id="8db78-122">Byte</span></span>
- <span data-ttu-id="8db78-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="8db78-123">BigEndianUnicode</span></span>
- <span data-ttu-id="8db78-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="8db78-124">UTF8</span></span>
- <span data-ttu-id="8db78-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="8db78-125">UTF7</span></span>
- <span data-ttu-id="8db78-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="8db78-126">Ascii</span></span>
- <span data-ttu-id="8db78-127">Assume</span><span class="sxs-lookup"><span data-stu-id="8db78-127">Default</span></span>
- <span data-ttu-id="8db78-128">Pelo</span><span class="sxs-lookup"><span data-stu-id="8db78-128">Oem</span></span>
- <span data-ttu-id="8db78-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="8db78-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-130">-Pasta</span><span class="sxs-lookup"><span data-stu-id="8db78-130">-Folder</span></span>
<span data-ttu-id="8db78-131">Indica que esta operação cria uma pasta.</span><span class="sxs-lookup"><span data-stu-id="8db78-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8db78-132">-Force</span></span>
<span data-ttu-id="8db78-133">Indica que essa operação pode substituir o item de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="8db78-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8db78-134">-Path</span></span>
<span data-ttu-id="8db78-135">Especifica o caminho do repositório data Lake do item a ser criado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="8db78-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8db78-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="8db78-136">-Value</span></span>
<span data-ttu-id="8db78-137">Especifica o conteúdo a ser adicionado ao item que você criou.</span><span class="sxs-lookup"><span data-stu-id="8db78-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8db78-138">-Confirm</span></span>
<span data-ttu-id="8db78-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8db78-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8db78-140">-WhatIf</span></span>
<span data-ttu-id="8db78-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8db78-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8db78-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8db78-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8db78-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8db78-143">CommonParameters</span></span>
<span data-ttu-id="8db78-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8db78-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8db78-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8db78-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8db78-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8db78-146">INPUTS</span></span>

### <span data-ttu-id="8db78-147">Objeto</span><span class="sxs-lookup"><span data-stu-id="8db78-147">Object</span></span>
<span data-ttu-id="8db78-148">O parâmetro ' value ' aceita o valor do tipo ' Object ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="8db78-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="8db78-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8db78-149">OUTPUTS</span></span>

### <span data-ttu-id="8db78-150">String</span><span class="sxs-lookup"><span data-stu-id="8db78-150">string</span></span>
<span data-ttu-id="8db78-151">O caminho completo para o arquivo ou a pasta criada.</span><span class="sxs-lookup"><span data-stu-id="8db78-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="8db78-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8db78-152">NOTES</span></span>

## <span data-ttu-id="8db78-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8db78-153">RELATED LINKS</span></span>

[<span data-ttu-id="8db78-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8db78-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8db78-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8db78-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8db78-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8db78-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8db78-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


