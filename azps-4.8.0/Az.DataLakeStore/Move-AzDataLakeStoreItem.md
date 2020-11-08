---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111124"
---
# <span data-ttu-id="9bce1-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9bce1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9bce1-102">SYNOPSIS</span></span>
<span data-ttu-id="9bce1-103">Move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="9bce1-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9bce1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9bce1-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bce1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9bce1-105">DESCRIPTION</span></span>
<span data-ttu-id="9bce1-106">O cmdlet **move-AzDataLakeStoreItem** move ou renomeia um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="9bce1-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9bce1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9bce1-107">EXAMPLES</span></span>

### <span data-ttu-id="9bce1-108">Exemplo 1: mover e renomear um item</span><span class="sxs-lookup"><span data-stu-id="9bce1-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="9bce1-109">Esse comando renomeia o item File.txt para RenamedFile.txt e o move para uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="9bce1-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="9bce1-110">OS</span><span class="sxs-lookup"><span data-stu-id="9bce1-110">PARAMETERS</span></span>

### <span data-ttu-id="9bce1-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="9bce1-111">-Account</span></span>
<span data-ttu-id="9bce1-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9bce1-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9bce1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bce1-113">-DefaultProfile</span></span>
<span data-ttu-id="9bce1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9bce1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bce1-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="9bce1-115">-Destination</span></span>
<span data-ttu-id="9bce1-116">Especifica o caminho do repositório data Lake para o qual mover o item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="9bce1-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9bce1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9bce1-117">-Force</span></span>
<span data-ttu-id="9bce1-118">Indica que essa operação pode substituir o arquivo de destino, caso ele já exista.</span><span class="sxs-lookup"><span data-stu-id="9bce1-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="9bce1-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="9bce1-119">-Path</span></span>
<span data-ttu-id="9bce1-120">Especifica o caminho do repositório data Lake do item para mover ou renomear, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="9bce1-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9bce1-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9bce1-121">-Confirm</span></span>
<span data-ttu-id="9bce1-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bce1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bce1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bce1-123">-WhatIf</span></span>
<span data-ttu-id="9bce1-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9bce1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bce1-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9bce1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bce1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bce1-126">CommonParameters</span></span>
<span data-ttu-id="9bce1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bce1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bce1-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bce1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bce1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9bce1-129">INPUTS</span></span>

### <span data-ttu-id="9bce1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9bce1-130">System.String</span></span>

### <span data-ttu-id="9bce1-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9bce1-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9bce1-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9bce1-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9bce1-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9bce1-133">OUTPUTS</span></span>

### <span data-ttu-id="9bce1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9bce1-134">System.String</span></span>

## <span data-ttu-id="9bce1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9bce1-135">NOTES</span></span>

## <span data-ttu-id="9bce1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9bce1-136">RELATED LINKS</span></span>

[<span data-ttu-id="9bce1-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="9bce1-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="9bce1-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="9bce1-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="9bce1-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="9bce1-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9bce1-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


