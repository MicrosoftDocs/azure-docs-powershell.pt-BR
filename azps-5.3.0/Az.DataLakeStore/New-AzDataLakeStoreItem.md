---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426621"
---
# <span data-ttu-id="18c40-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="18c40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18c40-102">SYNOPSIS</span></span>
<span data-ttu-id="18c40-103">Cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18c40-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="18c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18c40-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18c40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18c40-105">DESCRIPTION</span></span>
<span data-ttu-id="18c40-106">O cmdlet **New-AzDataLakeStoreItem** cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18c40-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="18c40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18c40-107">EXAMPLES</span></span>

### <span data-ttu-id="18c40-108">Exemplo 1: criar um novo arquivo e uma nova pasta</span><span class="sxs-lookup"><span data-stu-id="18c40-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="18c40-109">O primeiro comando cria o NewFile.txt de arquivo para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="18c40-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="18c40-110">O segundo comando cria a pasta NewFolder na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="18c40-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="18c40-111">OS</span><span class="sxs-lookup"><span data-stu-id="18c40-111">PARAMETERS</span></span>

### <span data-ttu-id="18c40-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="18c40-112">-Account</span></span>
<span data-ttu-id="18c40-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="18c40-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="18c40-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18c40-114">-DefaultProfile</span></span>
<span data-ttu-id="18c40-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="18c40-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18c40-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="18c40-116">-Encoding</span></span>
<span data-ttu-id="18c40-117">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="18c40-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="18c40-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="18c40-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18c40-119">Sabe</span><span class="sxs-lookup"><span data-stu-id="18c40-119">Unknown</span></span>
- <span data-ttu-id="18c40-120">String</span><span class="sxs-lookup"><span data-stu-id="18c40-120">String</span></span>
- <span data-ttu-id="18c40-121">ANSI</span><span class="sxs-lookup"><span data-stu-id="18c40-121">Unicode</span></span>
- <span data-ttu-id="18c40-122">Bits</span><span class="sxs-lookup"><span data-stu-id="18c40-122">Byte</span></span>
- <span data-ttu-id="18c40-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="18c40-123">BigEndianUnicode</span></span>
- <span data-ttu-id="18c40-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="18c40-124">UTF8</span></span>
- <span data-ttu-id="18c40-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="18c40-125">UTF7</span></span>
- <span data-ttu-id="18c40-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="18c40-126">Ascii</span></span>
- <span data-ttu-id="18c40-127">Assume</span><span class="sxs-lookup"><span data-stu-id="18c40-127">Default</span></span>
- <span data-ttu-id="18c40-128">Pelo</span><span class="sxs-lookup"><span data-stu-id="18c40-128">Oem</span></span>
- <span data-ttu-id="18c40-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="18c40-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="18c40-130">-Pasta</span><span class="sxs-lookup"><span data-stu-id="18c40-130">-Folder</span></span>
<span data-ttu-id="18c40-131">Indica que esta operação cria uma pasta.</span><span class="sxs-lookup"><span data-stu-id="18c40-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="18c40-132">-Force</span><span class="sxs-lookup"><span data-stu-id="18c40-132">-Force</span></span>
<span data-ttu-id="18c40-133">Indica que essa operação pode substituir o item de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="18c40-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="18c40-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="18c40-134">-Path</span></span>
<span data-ttu-id="18c40-135">Especifica o caminho do repositório data Lake do item a ser criado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="18c40-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="18c40-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="18c40-136">-Value</span></span>
<span data-ttu-id="18c40-137">Especifica o conteúdo a ser adicionado ao item que você criou.</span><span class="sxs-lookup"><span data-stu-id="18c40-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="18c40-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18c40-138">-Confirm</span></span>
<span data-ttu-id="18c40-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18c40-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18c40-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18c40-140">-WhatIf</span></span>
<span data-ttu-id="18c40-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18c40-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18c40-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18c40-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18c40-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18c40-143">CommonParameters</span></span>
<span data-ttu-id="18c40-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18c40-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18c40-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18c40-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18c40-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18c40-146">INPUTS</span></span>

### <span data-ttu-id="18c40-147">System. String</span><span class="sxs-lookup"><span data-stu-id="18c40-147">System.String</span></span>

### <span data-ttu-id="18c40-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="18c40-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="18c40-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="18c40-149">System.Object</span></span>

### <span data-ttu-id="18c40-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="18c40-150">System.Text.Encoding</span></span>

### <span data-ttu-id="18c40-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="18c40-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="18c40-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18c40-152">OUTPUTS</span></span>

### <span data-ttu-id="18c40-153">System. String</span><span class="sxs-lookup"><span data-stu-id="18c40-153">System.String</span></span>

## <span data-ttu-id="18c40-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18c40-154">NOTES</span></span>

## <span data-ttu-id="18c40-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18c40-155">RELATED LINKS</span></span>

[<span data-ttu-id="18c40-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="18c40-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="18c40-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="18c40-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="18c40-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="18c40-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18c40-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


