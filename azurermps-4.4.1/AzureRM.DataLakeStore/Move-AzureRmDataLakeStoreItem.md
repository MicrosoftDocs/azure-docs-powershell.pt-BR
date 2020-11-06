---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5d975e70423e03e3ab17bbfc8631ff8e1f892cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609686"
---
# <span data-ttu-id="c6b9e-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="c6b9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b9e-103">Move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6b9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6b9e-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6b9e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6b9e-105">DESCRIPTION</span></span>
<span data-ttu-id="c6b9e-106">O cmdlet **move-AzureRmDataLakeStoreItem** move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c6b9e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6b9e-107">EXAMPLES</span></span>

### <span data-ttu-id="c6b9e-108">Exemplo 1: mover e renomear um item</span><span class="sxs-lookup"><span data-stu-id="c6b9e-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="c6b9e-109">Esse comando renomeia o item File.txt para RenamedFile.txt e o move para uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="c6b9e-110">OS</span><span class="sxs-lookup"><span data-stu-id="c6b9e-110">PARAMETERS</span></span>

### <span data-ttu-id="c6b9e-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="c6b9e-111">-Account</span></span>
<span data-ttu-id="c6b9e-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c6b9e-113">-Destino</span><span class="sxs-lookup"><span data-stu-id="c6b9e-113">-Destination</span></span>
<span data-ttu-id="c6b9e-114">Especifica o caminho do repositório data Lake para o qual mover o item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="c6b9e-114">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c6b9e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c6b9e-115">-Force</span></span>
<span data-ttu-id="c6b9e-116">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="c6b9e-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c6b9e-117">-Path</span></span>
<span data-ttu-id="c6b9e-118">Especifica o caminho do repositório data Lake do item para mover ou renomear, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="c6b9e-118">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c6b9e-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6b9e-119">-Confirm</span></span>
<span data-ttu-id="c6b9e-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b9e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b9e-121">-WhatIf</span></span>
<span data-ttu-id="c6b9e-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b9e-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b9e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b9e-124">-DefaultProfile</span></span>
<span data-ttu-id="c6b9e-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6b9e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b9e-126">CommonParameters</span></span>
<span data-ttu-id="c6b9e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b9e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6b9e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b9e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6b9e-129">INPUTS</span></span>

## <span data-ttu-id="c6b9e-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6b9e-130">OUTPUTS</span></span>

### <span data-ttu-id="c6b9e-131">String</span><span class="sxs-lookup"><span data-stu-id="c6b9e-131">string</span></span>
<span data-ttu-id="c6b9e-132">O caminho completo para o arquivo ou pasta movida.</span><span class="sxs-lookup"><span data-stu-id="c6b9e-132">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="c6b9e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6b9e-133">NOTES</span></span>

## <span data-ttu-id="c6b9e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6b9e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6b9e-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c6b9e-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c6b9e-137">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c6b9e-138">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c6b9e-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c6b9e-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c6b9e-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


