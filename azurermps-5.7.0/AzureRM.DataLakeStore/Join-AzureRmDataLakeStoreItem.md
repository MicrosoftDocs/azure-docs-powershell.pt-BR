---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428931"
---
# <span data-ttu-id="a4e56-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="a4e56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4e56-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e56-103">Une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a4e56-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4e56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4e56-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4e56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4e56-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e56-106">O cmdlet **Join-AzureRmDataLakeStoreItem** une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a4e56-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="a4e56-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4e56-107">EXAMPLES</span></span>

### <span data-ttu-id="a4e56-108">Exemplo 1: unir dois itens</span><span class="sxs-lookup"><span data-stu-id="a4e56-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="a4e56-109">Este comando une File01.txt e File02.txt para criar o arquivo CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="a4e56-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="a4e56-110">OS</span><span class="sxs-lookup"><span data-stu-id="a4e56-110">PARAMETERS</span></span>

### <span data-ttu-id="a4e56-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="a4e56-111">-Account</span></span>
<span data-ttu-id="a4e56-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a4e56-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a4e56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e56-113">-DefaultProfile</span></span>
<span data-ttu-id="a4e56-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e56-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e56-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="a4e56-115">-Destination</span></span>
<span data-ttu-id="a4e56-116">Especifica o caminho do repositório data Lake para o item associado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="a4e56-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e56-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4e56-117">-Force</span></span>
<span data-ttu-id="a4e56-118">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="a4e56-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="a4e56-119">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="a4e56-119">-Paths</span></span>
<span data-ttu-id="a4e56-120">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem combinados, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="a4e56-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e56-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a4e56-121">-Confirm</span></span>
<span data-ttu-id="a4e56-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4e56-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4e56-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4e56-123">-WhatIf</span></span>
<span data-ttu-id="a4e56-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a4e56-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4e56-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a4e56-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4e56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e56-126">CommonParameters</span></span>
<span data-ttu-id="a4e56-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e56-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e56-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e56-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4e56-129">INPUTS</span></span>

### <span data-ttu-id="a4e56-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a4e56-130">None</span></span>
<span data-ttu-id="a4e56-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a4e56-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4e56-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4e56-132">OUTPUTS</span></span>

### <span data-ttu-id="a4e56-133">String</span><span class="sxs-lookup"><span data-stu-id="a4e56-133">string</span></span>
<span data-ttu-id="a4e56-134">O caminho completo para o arquivo resultante dos arquivos associados.</span><span class="sxs-lookup"><span data-stu-id="a4e56-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="a4e56-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4e56-135">NOTES</span></span>

## <span data-ttu-id="a4e56-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4e56-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4e56-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a4e56-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a4e56-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a4e56-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a4e56-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a4e56-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a4e56-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


