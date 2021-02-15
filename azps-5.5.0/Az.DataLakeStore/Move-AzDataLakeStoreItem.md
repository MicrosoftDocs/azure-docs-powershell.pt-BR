---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115378"
---
# <span data-ttu-id="92f1f-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="92f1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="92f1f-103">Move ou renomeia um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92f1f-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92f1f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92f1f-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f1f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="92f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="92f1f-106">O cmdlet **Move-AzDataLakeStoreItem** move ou renomeia um arquivo ou pasta na Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92f1f-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="92f1f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92f1f-107">EXAMPLES</span></span>

### <span data-ttu-id="92f1f-108">Exemplo 1: Mover e renomear um item</span><span class="sxs-lookup"><span data-stu-id="92f1f-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="92f1f-109">Esse comando renomeia o item File.txt para RenamedFile.txt e o move para uma pasta diferente.</span><span class="sxs-lookup"><span data-stu-id="92f1f-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="92f1f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92f1f-110">PARAMETERS</span></span>

### <span data-ttu-id="92f1f-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="92f1f-111">-Account</span></span>
<span data-ttu-id="92f1f-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="92f1f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="92f1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f1f-113">-DefaultProfile</span></span>
<span data-ttu-id="92f1f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="92f1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92f1f-115">-Destino</span><span class="sxs-lookup"><span data-stu-id="92f1f-115">-Destination</span></span>
<span data-ttu-id="92f1f-116">Especifica o caminho do Data Lake Store para o qual mover o item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="92f1f-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92f1f-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="92f1f-117">-Force</span></span>
<span data-ttu-id="92f1f-118">Indica que essa operação pode substituir o arquivo de destino se ele já existir.</span><span class="sxs-lookup"><span data-stu-id="92f1f-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="92f1f-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="92f1f-119">-Path</span></span>
<span data-ttu-id="92f1f-120">Especifica o caminho do Data Lake Store do item para mover ou renomear, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="92f1f-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="92f1f-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="92f1f-121">-Confirm</span></span>
<span data-ttu-id="92f1f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92f1f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92f1f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f1f-123">-WhatIf</span></span>
<span data-ttu-id="92f1f-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="92f1f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92f1f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="92f1f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92f1f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f1f-126">CommonParameters</span></span>
<span data-ttu-id="92f1f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f1f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f1f-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f1f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f1f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="92f1f-129">INPUTS</span></span>

### <span data-ttu-id="92f1f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="92f1f-130">System.String</span></span>

### <span data-ttu-id="92f1f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="92f1f-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="92f1f-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="92f1f-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="92f1f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="92f1f-133">OUTPUTS</span></span>

### <span data-ttu-id="92f1f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="92f1f-134">System.String</span></span>

## <span data-ttu-id="92f1f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="92f1f-135">NOTES</span></span>

## <span data-ttu-id="92f1f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92f1f-136">RELATED LINKS</span></span>

[<span data-ttu-id="92f1f-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="92f1f-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="92f1f-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="92f1f-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="92f1f-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="92f1f-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="92f1f-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


