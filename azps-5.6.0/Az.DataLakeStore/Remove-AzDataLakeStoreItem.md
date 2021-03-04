---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ce4a8051867b535ba2aff4429b5bcfa0b9ab53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892980"
---
# <span data-ttu-id="36113-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="36113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36113-102">SYNOPSIS</span></span>
<span data-ttu-id="36113-103">Exclui um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="36113-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="36113-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="36113-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36113-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="36113-105">DESCRIPTION</span></span>
<span data-ttu-id="36113-106">O cmdlet **Remove-AzDataLakeStoreItem** exclui um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="36113-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="36113-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="36113-107">EXAMPLES</span></span>

### <span data-ttu-id="36113-108">Exemplo 1: Remover vários itens</span><span class="sxs-lookup"><span data-stu-id="36113-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="36113-109">Este comando remove os arquivos File01.txt e File.csv do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="36113-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="36113-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="36113-110">PARAMETERS</span></span>

### <span data-ttu-id="36113-111">-Account</span><span class="sxs-lookup"><span data-stu-id="36113-111">-Account</span></span>
<span data-ttu-id="36113-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="36113-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="36113-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36113-113">-DefaultProfile</span></span>
<span data-ttu-id="36113-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="36113-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36113-115">-Force</span><span class="sxs-lookup"><span data-stu-id="36113-115">-Force</span></span>
<span data-ttu-id="36113-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="36113-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36113-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36113-117">-PassThru</span></span>
<span data-ttu-id="36113-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="36113-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36113-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="36113-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36113-120">-Paths</span><span class="sxs-lookup"><span data-stu-id="36113-120">-Paths</span></span>
<span data-ttu-id="36113-121">Especifica uma matriz de caminhos do Data Lake Store dos arquivos a remover, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="36113-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36113-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="36113-122">-Recurse</span></span>
<span data-ttu-id="36113-123">Indica que essa operação exclui todos os itens na pasta de destino, incluindo subpastas.</span><span class="sxs-lookup"><span data-stu-id="36113-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36113-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36113-124">-Confirm</span></span>
<span data-ttu-id="36113-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36113-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36113-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36113-126">-WhatIf</span></span>
<span data-ttu-id="36113-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="36113-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36113-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36113-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36113-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36113-129">CommonParameters</span></span>
<span data-ttu-id="36113-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36113-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36113-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36113-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36113-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36113-132">INPUTS</span></span>

### <span data-ttu-id="36113-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36113-133">System.String</span></span>

### <span data-ttu-id="36113-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="36113-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="36113-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36113-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36113-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="36113-136">OUTPUTS</span></span>

### <span data-ttu-id="36113-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36113-137">System.Boolean</span></span>

## <span data-ttu-id="36113-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="36113-138">NOTES</span></span>

## <span data-ttu-id="36113-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36113-139">RELATED LINKS</span></span>

[<span data-ttu-id="36113-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="36113-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="36113-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="36113-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="36113-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="36113-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="36113-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


