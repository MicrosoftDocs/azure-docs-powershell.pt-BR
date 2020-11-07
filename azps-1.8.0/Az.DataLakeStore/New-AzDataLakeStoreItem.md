---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: 222df24f2d3db296ce116e49da8baeb3e22ec699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770923"
---
# <span data-ttu-id="457eb-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="457eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="457eb-102">SYNOPSIS</span></span>
<span data-ttu-id="457eb-103">Cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="457eb-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="457eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="457eb-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="457eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="457eb-105">DESCRIPTION</span></span>
<span data-ttu-id="457eb-106">O cmdlet **New-AzDataLakeStoreItem** cria um novo arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="457eb-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="457eb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="457eb-107">EXAMPLES</span></span>

### <span data-ttu-id="457eb-108">Exemplo 1: criar um novo arquivo e uma nova pasta</span><span class="sxs-lookup"><span data-stu-id="457eb-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="457eb-109">O primeiro comando cria o NewFile.txt de arquivo para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="457eb-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="457eb-110">O segundo comando cria a pasta NewFolder na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="457eb-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="457eb-111">OS</span><span class="sxs-lookup"><span data-stu-id="457eb-111">PARAMETERS</span></span>

### <span data-ttu-id="457eb-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="457eb-112">-Account</span></span>
<span data-ttu-id="457eb-113">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="457eb-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="457eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457eb-114">-DefaultProfile</span></span>
<span data-ttu-id="457eb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="457eb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="457eb-116">-Encoding</span><span class="sxs-lookup"><span data-stu-id="457eb-116">-Encoding</span></span>
<span data-ttu-id="457eb-117">Especifica a codificação para o item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="457eb-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="457eb-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="457eb-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="457eb-119">Sabe</span><span class="sxs-lookup"><span data-stu-id="457eb-119">Unknown</span></span>
- <span data-ttu-id="457eb-120">String</span><span class="sxs-lookup"><span data-stu-id="457eb-120">String</span></span>
- <span data-ttu-id="457eb-121">ANSI</span><span class="sxs-lookup"><span data-stu-id="457eb-121">Unicode</span></span>
- <span data-ttu-id="457eb-122">Bits</span><span class="sxs-lookup"><span data-stu-id="457eb-122">Byte</span></span>
- <span data-ttu-id="457eb-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="457eb-123">BigEndianUnicode</span></span>
- <span data-ttu-id="457eb-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="457eb-124">UTF8</span></span>
- <span data-ttu-id="457eb-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="457eb-125">UTF7</span></span>
- <span data-ttu-id="457eb-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="457eb-126">Ascii</span></span>
- <span data-ttu-id="457eb-127">Assume</span><span class="sxs-lookup"><span data-stu-id="457eb-127">Default</span></span>
- <span data-ttu-id="457eb-128">Pelo</span><span class="sxs-lookup"><span data-stu-id="457eb-128">Oem</span></span>
- <span data-ttu-id="457eb-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="457eb-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="457eb-130">-Pasta</span><span class="sxs-lookup"><span data-stu-id="457eb-130">-Folder</span></span>
<span data-ttu-id="457eb-131">Indica que esta operação cria uma pasta.</span><span class="sxs-lookup"><span data-stu-id="457eb-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="457eb-132">-Force</span><span class="sxs-lookup"><span data-stu-id="457eb-132">-Force</span></span>
<span data-ttu-id="457eb-133">Indica que essa operação pode substituir o item de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="457eb-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="457eb-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="457eb-134">-Path</span></span>
<span data-ttu-id="457eb-135">Especifica o caminho do repositório data Lake do item a ser criado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="457eb-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="457eb-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="457eb-136">-Value</span></span>
<span data-ttu-id="457eb-137">Especifica o conteúdo a ser adicionado ao item que você criou.</span><span class="sxs-lookup"><span data-stu-id="457eb-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="457eb-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="457eb-138">-Confirm</span></span>
<span data-ttu-id="457eb-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="457eb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="457eb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="457eb-140">-WhatIf</span></span>
<span data-ttu-id="457eb-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="457eb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="457eb-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="457eb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="457eb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457eb-143">CommonParameters</span></span>
<span data-ttu-id="457eb-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="457eb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457eb-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="457eb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457eb-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="457eb-146">INPUTS</span></span>

### <span data-ttu-id="457eb-147">System. String</span><span class="sxs-lookup"><span data-stu-id="457eb-147">System.String</span></span>

### <span data-ttu-id="457eb-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="457eb-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="457eb-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="457eb-149">System.Object</span></span>

### <span data-ttu-id="457eb-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="457eb-150">System.Text.Encoding</span></span>

### <span data-ttu-id="457eb-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="457eb-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="457eb-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="457eb-152">OUTPUTS</span></span>

### <span data-ttu-id="457eb-153">System. String</span><span class="sxs-lookup"><span data-stu-id="457eb-153">System.String</span></span>

## <span data-ttu-id="457eb-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="457eb-154">NOTES</span></span>

## <span data-ttu-id="457eb-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="457eb-155">RELATED LINKS</span></span>

[<span data-ttu-id="457eb-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="457eb-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="457eb-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="457eb-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="457eb-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="457eb-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="457eb-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


