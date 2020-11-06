---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432630"
---
# <span data-ttu-id="ceadc-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ceadc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ceadc-102">SYNOPSIS</span></span>
<span data-ttu-id="ceadc-103">Une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ceadc-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ceadc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ceadc-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceadc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ceadc-105">DESCRIPTION</span></span>
<span data-ttu-id="ceadc-106">O cmdlet **Join-AzureRmDataLakeStoreItem** une um ou mais arquivos para criar um arquivo no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ceadc-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="ceadc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ceadc-107">EXAMPLES</span></span>

### <span data-ttu-id="ceadc-108">Exemplo 1: unir dois itens</span><span class="sxs-lookup"><span data-stu-id="ceadc-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="ceadc-109">Este comando une File01.txt e File02.txt para criar o arquivo CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="ceadc-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="ceadc-110">OS</span><span class="sxs-lookup"><span data-stu-id="ceadc-110">PARAMETERS</span></span>

### <span data-ttu-id="ceadc-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="ceadc-111">-Account</span></span>
<span data-ttu-id="ceadc-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ceadc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ceadc-113">-Destino</span><span class="sxs-lookup"><span data-stu-id="ceadc-113">-Destination</span></span>
<span data-ttu-id="ceadc-114">Especifica o caminho do repositório data Lake para o item associado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="ceadc-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ceadc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ceadc-115">-Force</span></span>
<span data-ttu-id="ceadc-116">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="ceadc-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="ceadc-117">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="ceadc-117">-Paths</span></span>
<span data-ttu-id="ceadc-118">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem combinados, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="ceadc-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ceadc-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ceadc-119">-Confirm</span></span>
<span data-ttu-id="ceadc-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceadc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceadc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceadc-121">-WhatIf</span></span>
<span data-ttu-id="ceadc-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ceadc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ceadc-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ceadc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceadc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceadc-124">-DefaultProfile</span></span>
<span data-ttu-id="ceadc-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ceadc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ceadc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceadc-126">CommonParameters</span></span>
<span data-ttu-id="ceadc-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceadc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceadc-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceadc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceadc-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ceadc-129">INPUTS</span></span>

## <span data-ttu-id="ceadc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ceadc-130">OUTPUTS</span></span>

### <span data-ttu-id="ceadc-131">String</span><span class="sxs-lookup"><span data-stu-id="ceadc-131">string</span></span>
<span data-ttu-id="ceadc-132">O caminho completo para o arquivo resultante dos arquivos associados.</span><span class="sxs-lookup"><span data-stu-id="ceadc-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="ceadc-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ceadc-133">NOTES</span></span>

## <span data-ttu-id="ceadc-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ceadc-134">RELATED LINKS</span></span>

[<span data-ttu-id="ceadc-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ceadc-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ceadc-137">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ceadc-138">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ceadc-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ceadc-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ceadc-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


