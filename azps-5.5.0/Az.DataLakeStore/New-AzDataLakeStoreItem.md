---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113258"
---
# <span data-ttu-id="f1116-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f1116-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1116-102">SYNOPSIS</span></span>
<span data-ttu-id="f1116-103">Cria um novo arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f1116-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f1116-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1116-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1116-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1116-105">DESCRIPTION</span></span>
<span data-ttu-id="f1116-106">O cmdlet **New-AzDataLakeStoreItem** cria um novo arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f1116-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f1116-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1116-107">EXAMPLES</span></span>

### <span data-ttu-id="f1116-108">Exemplo 1: Criar um novo arquivo e uma nova pasta</span><span class="sxs-lookup"><span data-stu-id="f1116-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="f1116-109">O primeiro comando cria o arquivo NewFile.txt para a conta especificada.</span><span class="sxs-lookup"><span data-stu-id="f1116-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="f1116-110">O segundo comando cria a pasta NovaPasta na pasta raiz.</span><span class="sxs-lookup"><span data-stu-id="f1116-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="f1116-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1116-111">PARAMETERS</span></span>

### <span data-ttu-id="f1116-112">-Conta</span><span class="sxs-lookup"><span data-stu-id="f1116-112">-Account</span></span>
<span data-ttu-id="f1116-113">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f1116-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f1116-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1116-114">-DefaultProfile</span></span>
<span data-ttu-id="f1116-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f1116-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1116-116">-Codificação</span><span class="sxs-lookup"><span data-stu-id="f1116-116">-Encoding</span></span>
<span data-ttu-id="f1116-117">Especifica a codificação do item a ser criado.</span><span class="sxs-lookup"><span data-stu-id="f1116-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f1116-118">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f1116-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f1116-119">Desconhecido</span><span class="sxs-lookup"><span data-stu-id="f1116-119">Unknown</span></span>
- <span data-ttu-id="f1116-120">String</span><span class="sxs-lookup"><span data-stu-id="f1116-120">String</span></span>
- <span data-ttu-id="f1116-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="f1116-121">Unicode</span></span>
- <span data-ttu-id="f1116-122">Byte</span><span class="sxs-lookup"><span data-stu-id="f1116-122">Byte</span></span>
- <span data-ttu-id="f1116-123">Bigendianunicode</span><span class="sxs-lookup"><span data-stu-id="f1116-123">BigEndianUnicode</span></span>
- <span data-ttu-id="f1116-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="f1116-124">UTF8</span></span>
- <span data-ttu-id="f1116-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="f1116-125">UTF7</span></span>
- <span data-ttu-id="f1116-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="f1116-126">Ascii</span></span>
- <span data-ttu-id="f1116-127">Padrão</span><span class="sxs-lookup"><span data-stu-id="f1116-127">Default</span></span>
- <span data-ttu-id="f1116-128">Oem</span><span class="sxs-lookup"><span data-stu-id="f1116-128">Oem</span></span>
- <span data-ttu-id="f1116-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f1116-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f1116-130">-Pasta</span><span class="sxs-lookup"><span data-stu-id="f1116-130">-Folder</span></span>
<span data-ttu-id="f1116-131">Indica que essa operação cria uma pasta.</span><span class="sxs-lookup"><span data-stu-id="f1116-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="f1116-132">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f1116-132">-Force</span></span>
<span data-ttu-id="f1116-133">Indica que essa operação pode substituir o item de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="f1116-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="f1116-134">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f1116-134">-Path</span></span>
<span data-ttu-id="f1116-135">Especifica o caminho do Data Lake Store do item a ser criado, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="f1116-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f1116-136">-Valor</span><span class="sxs-lookup"><span data-stu-id="f1116-136">-Value</span></span>
<span data-ttu-id="f1116-137">Especifica o conteúdo a ser adicionar ao item que você cria.</span><span class="sxs-lookup"><span data-stu-id="f1116-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="f1116-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f1116-138">-Confirm</span></span>
<span data-ttu-id="f1116-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1116-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1116-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1116-140">-WhatIf</span></span>
<span data-ttu-id="f1116-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f1116-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1116-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1116-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1116-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1116-143">CommonParameters</span></span>
<span data-ttu-id="f1116-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1116-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1116-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1116-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1116-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1116-146">INPUTS</span></span>

### <span data-ttu-id="f1116-147">System.String</span><span class="sxs-lookup"><span data-stu-id="f1116-147">System.String</span></span>

### <span data-ttu-id="f1116-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f1116-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f1116-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="f1116-149">System.Object</span></span>

### <span data-ttu-id="f1116-150">Codificação system.text.text</span><span class="sxs-lookup"><span data-stu-id="f1116-150">System.Text.Encoding</span></span>

### <span data-ttu-id="f1116-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1116-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1116-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1116-152">OUTPUTS</span></span>

### <span data-ttu-id="f1116-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f1116-153">System.String</span></span>

## <span data-ttu-id="f1116-154">Notas</span><span class="sxs-lookup"><span data-stu-id="f1116-154">NOTES</span></span>

## <span data-ttu-id="f1116-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1116-155">RELATED LINKS</span></span>

[<span data-ttu-id="f1116-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1116-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1116-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1116-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1116-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f1116-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f1116-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


