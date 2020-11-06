---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2e50135762826661e82f499f2aec48c67d00c648
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426375"
---
# <span data-ttu-id="a9220-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="a9220-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9220-102">SYNOPSIS</span></span>
<span data-ttu-id="a9220-103">Cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9220-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9220-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9220-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9220-105">DESCRIPTION</span></span>
<span data-ttu-id="a9220-106">O cmdlet **New-AzureRmDataLakeStoreItem** cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9220-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a9220-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9220-107">EXAMPLES</span></span>

### <span data-ttu-id="a9220-108">Exemplo 1: criar um novo arquivo e uma nova pasta</span><span class="sxs-lookup"><span data-stu-id="a9220-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="a9220-109">O primeiro comando cria o NewFile.txt de arquivo para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="a9220-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="a9220-110">O segundo comando cria a pasta NewFolder na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="a9220-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="a9220-111">OS</span><span class="sxs-lookup"><span data-stu-id="a9220-111">PARAMETERS</span></span>

### <span data-ttu-id="a9220-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="a9220-112">-Account</span></span>
<span data-ttu-id="a9220-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9220-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a9220-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9220-114">-DefaultProfile</span></span>
<span data-ttu-id="a9220-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9220-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9220-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="a9220-116">-Encoding</span></span>
<span data-ttu-id="a9220-117">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a9220-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a9220-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a9220-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9220-119">Sabe</span><span class="sxs-lookup"><span data-stu-id="a9220-119">Unknown</span></span>
- <span data-ttu-id="a9220-120">String</span><span class="sxs-lookup"><span data-stu-id="a9220-120">String</span></span>
- <span data-ttu-id="a9220-121">ANSI</span><span class="sxs-lookup"><span data-stu-id="a9220-121">Unicode</span></span>
- <span data-ttu-id="a9220-122">Bits</span><span class="sxs-lookup"><span data-stu-id="a9220-122">Byte</span></span>
- <span data-ttu-id="a9220-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a9220-123">BigEndianUnicode</span></span>
- <span data-ttu-id="a9220-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="a9220-124">UTF8</span></span>
- <span data-ttu-id="a9220-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="a9220-125">UTF7</span></span>
- <span data-ttu-id="a9220-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="a9220-126">Ascii</span></span>
- <span data-ttu-id="a9220-127">Assume</span><span class="sxs-lookup"><span data-stu-id="a9220-127">Default</span></span>
- <span data-ttu-id="a9220-128">Pelo</span><span class="sxs-lookup"><span data-stu-id="a9220-128">Oem</span></span>
- <span data-ttu-id="a9220-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a9220-129">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9220-130">-Pasta</span><span class="sxs-lookup"><span data-stu-id="a9220-130">-Folder</span></span>
<span data-ttu-id="a9220-131">Indica que esta operação cria uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a9220-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="a9220-132">-Force</span><span class="sxs-lookup"><span data-stu-id="a9220-132">-Force</span></span>
<span data-ttu-id="a9220-133">Indica que essa operação pode substituir o item de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="a9220-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="a9220-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a9220-134">-Path</span></span>
<span data-ttu-id="a9220-135">Especifica o caminho do repositório data Lake do item a ser criado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="a9220-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a9220-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="a9220-136">-Value</span></span>
<span data-ttu-id="a9220-137">Especifica o conteúdo a ser adicionado ao item que você criou.</span><span class="sxs-lookup"><span data-stu-id="a9220-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9220-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9220-138">-Confirm</span></span>
<span data-ttu-id="a9220-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9220-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9220-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9220-140">-WhatIf</span></span>
<span data-ttu-id="a9220-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9220-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9220-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9220-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9220-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9220-143">CommonParameters</span></span>
<span data-ttu-id="a9220-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9220-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9220-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9220-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9220-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9220-146">INPUTS</span></span>

### <span data-ttu-id="a9220-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9220-147">System.String</span></span>

### <span data-ttu-id="a9220-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a9220-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a9220-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9220-149">System.Object</span></span>

### <span data-ttu-id="a9220-150">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="a9220-150">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="a9220-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9220-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9220-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9220-152">OUTPUTS</span></span>

### <span data-ttu-id="a9220-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a9220-153">System.String</span></span>
<span data-ttu-id="a9220-154">O caminho completo para o arquivo ou a pasta criada.</span><span class="sxs-lookup"><span data-stu-id="a9220-154">The full path to the created file or folder.</span></span>

## <span data-ttu-id="a9220-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9220-155">NOTES</span></span>

## <span data-ttu-id="a9220-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9220-156">RELATED LINKS</span></span>

[<span data-ttu-id="a9220-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9220-158">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9220-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9220-160">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-160">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9220-161">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-161">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9220-162">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9220-162">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


