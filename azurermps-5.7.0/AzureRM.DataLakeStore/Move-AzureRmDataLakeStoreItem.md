---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602650"
---
# <span data-ttu-id="5015f-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5015f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5015f-102">SYNOPSIS</span></span>
<span data-ttu-id="5015f-103">Move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="5015f-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5015f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5015f-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5015f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5015f-105">DESCRIPTION</span></span>
<span data-ttu-id="5015f-106">O cmdlet **move-AzureRmDataLakeStoreItem** move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="5015f-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5015f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5015f-107">EXAMPLES</span></span>

### <span data-ttu-id="5015f-108">Exemplo 1: mover e renomear um item</span><span class="sxs-lookup"><span data-stu-id="5015f-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="5015f-109">Esse comando renomeia o item File.txt para RenamedFile.txt e o move para uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="5015f-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="5015f-110">OS</span><span class="sxs-lookup"><span data-stu-id="5015f-110">PARAMETERS</span></span>

### <span data-ttu-id="5015f-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="5015f-111">-Account</span></span>
<span data-ttu-id="5015f-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5015f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5015f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5015f-113">-DefaultProfile</span></span>
<span data-ttu-id="5015f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5015f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5015f-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="5015f-115">-Destination</span></span>
<span data-ttu-id="5015f-116">Especifica o caminho do repositório data Lake para o qual mover o item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="5015f-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5015f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5015f-117">-Force</span></span>
<span data-ttu-id="5015f-118">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="5015f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="5015f-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5015f-119">-Path</span></span>
<span data-ttu-id="5015f-120">Especifica o caminho do repositório data Lake do item para mover ou renomear, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="5015f-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5015f-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5015f-121">-Confirm</span></span>
<span data-ttu-id="5015f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5015f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5015f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5015f-123">-WhatIf</span></span>
<span data-ttu-id="5015f-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5015f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5015f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5015f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5015f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5015f-126">CommonParameters</span></span>
<span data-ttu-id="5015f-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5015f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5015f-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5015f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5015f-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5015f-129">INPUTS</span></span>

### <span data-ttu-id="5015f-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5015f-130">None</span></span>
<span data-ttu-id="5015f-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5015f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5015f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5015f-132">OUTPUTS</span></span>

### <span data-ttu-id="5015f-133">String</span><span class="sxs-lookup"><span data-stu-id="5015f-133">string</span></span>
<span data-ttu-id="5015f-134">O caminho completo para o arquivo ou pasta movida.</span><span class="sxs-lookup"><span data-stu-id="5015f-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="5015f-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5015f-135">NOTES</span></span>

## <span data-ttu-id="5015f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5015f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5015f-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5015f-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5015f-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5015f-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5015f-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5015f-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5015f-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


