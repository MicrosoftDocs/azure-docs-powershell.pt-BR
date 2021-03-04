---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 9a2e0f7abbf9fa6797b4ced7c6e841b51a63a9dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888371"
---
# <span data-ttu-id="79764-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="79764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79764-102">SYNOPSIS</span></span>
<span data-ttu-id="79764-103">Insinte um ou mais arquivos para criar um arquivo no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="79764-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="79764-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="79764-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79764-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="79764-105">DESCRIPTION</span></span>
<span data-ttu-id="79764-106">O cmdlet **Join-AzDataLakeStoreItem** ins junta um ou mais arquivos para criar um arquivo no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="79764-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="79764-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79764-107">EXAMPLES</span></span>

### <span data-ttu-id="79764-108">Exemplo 1: Ingressar dois itens</span><span class="sxs-lookup"><span data-stu-id="79764-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="79764-109">Esse comando se junta File01.txt e File02.txt criar o arquivo CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="79764-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="79764-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="79764-110">PARAMETERS</span></span>

### <span data-ttu-id="79764-111">-Account</span><span class="sxs-lookup"><span data-stu-id="79764-111">-Account</span></span>
<span data-ttu-id="79764-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="79764-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="79764-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79764-113">-DefaultProfile</span></span>
<span data-ttu-id="79764-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="79764-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79764-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="79764-115">-Destination</span></span>
<span data-ttu-id="79764-116">Especifica o caminho do Data Lake Store para o item ingressada, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="79764-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79764-117">-Force</span><span class="sxs-lookup"><span data-stu-id="79764-117">-Force</span></span>
<span data-ttu-id="79764-118">Indica que essa operação pode substituir o arquivo de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="79764-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="79764-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="79764-119">-Paths</span></span>
<span data-ttu-id="79764-120">Especifica uma matriz de caminhos do Data Lake Store dos arquivos a combinar, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="79764-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79764-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79764-121">-Confirm</span></span>
<span data-ttu-id="79764-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79764-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79764-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79764-123">-WhatIf</span></span>
<span data-ttu-id="79764-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79764-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79764-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79764-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79764-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79764-126">CommonParameters</span></span>
<span data-ttu-id="79764-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79764-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79764-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79764-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79764-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79764-129">INPUTS</span></span>

### <span data-ttu-id="79764-130">System.String</span><span class="sxs-lookup"><span data-stu-id="79764-130">System.String</span></span>

### <span data-ttu-id="79764-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="79764-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="79764-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="79764-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="79764-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79764-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="79764-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="79764-134">OUTPUTS</span></span>

### <span data-ttu-id="79764-135">System.String</span><span class="sxs-lookup"><span data-stu-id="79764-135">System.String</span></span>

## <span data-ttu-id="79764-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="79764-136">NOTES</span></span>

## <span data-ttu-id="79764-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79764-137">RELATED LINKS</span></span>

[<span data-ttu-id="79764-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="79764-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="79764-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="79764-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="79764-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="79764-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="79764-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


