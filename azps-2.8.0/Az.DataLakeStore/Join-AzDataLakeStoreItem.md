---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 7ff40890783edbfaf610434f0b25ad04b4b3be21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596834"
---
# <span data-ttu-id="67ab3-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="67ab3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="67ab3-103">Une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67ab3-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="67ab3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67ab3-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ab3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="67ab3-106">O cmdlet **Join-AzDataLakeStoreItem** une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67ab3-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="67ab3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="67ab3-108">Exemplo 1: unir dois itens</span><span class="sxs-lookup"><span data-stu-id="67ab3-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="67ab3-109">Este comando une File01.txt e File02.txt para criar o arquivo CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="67ab3-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="67ab3-110">OS</span><span class="sxs-lookup"><span data-stu-id="67ab3-110">PARAMETERS</span></span>

### <span data-ttu-id="67ab3-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="67ab3-111">-Account</span></span>
<span data-ttu-id="67ab3-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67ab3-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="67ab3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ab3-113">-DefaultProfile</span></span>
<span data-ttu-id="67ab3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67ab3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67ab3-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="67ab3-115">-Destination</span></span>
<span data-ttu-id="67ab3-116">Especifica o caminho do repositório data Lake para o item associado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="67ab3-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="67ab3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="67ab3-117">-Force</span></span>
<span data-ttu-id="67ab3-118">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="67ab3-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="67ab3-119">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="67ab3-119">-Paths</span></span>
<span data-ttu-id="67ab3-120">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem combinados, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="67ab3-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="67ab3-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67ab3-121">-Confirm</span></span>
<span data-ttu-id="67ab3-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67ab3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ab3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ab3-123">-WhatIf</span></span>
<span data-ttu-id="67ab3-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67ab3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ab3-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67ab3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ab3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ab3-126">CommonParameters</span></span>
<span data-ttu-id="67ab3-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ab3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ab3-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ab3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ab3-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67ab3-129">INPUTS</span></span>

### <span data-ttu-id="67ab3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="67ab3-130">System.String</span></span>

### <span data-ttu-id="67ab3-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="67ab3-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="67ab3-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="67ab3-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="67ab3-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="67ab3-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="67ab3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67ab3-134">OUTPUTS</span></span>

### <span data-ttu-id="67ab3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="67ab3-135">System.String</span></span>

## <span data-ttu-id="67ab3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67ab3-136">NOTES</span></span>

## <span data-ttu-id="67ab3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67ab3-137">RELATED LINKS</span></span>

[<span data-ttu-id="67ab3-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="67ab3-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="67ab3-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="67ab3-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="67ab3-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="67ab3-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67ab3-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


