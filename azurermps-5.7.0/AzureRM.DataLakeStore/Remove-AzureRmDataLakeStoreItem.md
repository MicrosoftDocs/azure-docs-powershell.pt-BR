---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426712"
---
# <span data-ttu-id="3ec03-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3ec03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ec03-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec03-103">Exclui um arquivo ou uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3ec03-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ec03-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ec03-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec03-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ec03-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec03-106">O cmdlet **Remove-AzureRmDataLakeStoreItem** exclui um arquivo ou uma pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="3ec03-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3ec03-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ec03-107">EXAMPLES</span></span>

### <span data-ttu-id="3ec03-108">Exemplo 1: remover vários itens</span><span class="sxs-lookup"><span data-stu-id="3ec03-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="3ec03-109">Esse comando remove os arquivos File01.txt e File.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="3ec03-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="3ec03-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ec03-110">PARAMETERS</span></span>

### <span data-ttu-id="3ec03-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="3ec03-111">-Account</span></span>
<span data-ttu-id="3ec03-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3ec03-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3ec03-113">-Limpar</span><span class="sxs-lookup"><span data-stu-id="3ec03-113">-Clean</span></span>
<span data-ttu-id="3ec03-114">Indica que o usuário quer remover todo o conteúdo da pasta, mas não a própria pasta</span><span class="sxs-lookup"><span data-stu-id="3ec03-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

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

### <span data-ttu-id="3ec03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec03-115">-DefaultProfile</span></span>
<span data-ttu-id="3ec03-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec03-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ec03-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ec03-117">-Force</span></span>
<span data-ttu-id="3ec03-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3ec03-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec03-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ec03-119">-PassThru</span></span>
<span data-ttu-id="3ec03-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3ec03-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3ec03-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3ec03-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec03-122">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="3ec03-122">-Paths</span></span>
<span data-ttu-id="3ec03-123">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem removidos, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="3ec03-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec03-124">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3ec03-124">-Recurse</span></span>
<span data-ttu-id="3ec03-125">Indica que essa operação exclui todos os itens da pasta de destino, incluindo subpastas.</span><span class="sxs-lookup"><span data-stu-id="3ec03-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="3ec03-126">A menos que você especifique o parâmetro *Clean* , a pasta de destino também será excluída.</span><span class="sxs-lookup"><span data-stu-id="3ec03-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ec03-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ec03-127">-Confirm</span></span>
<span data-ttu-id="3ec03-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec03-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec03-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec03-129">-WhatIf</span></span>
<span data-ttu-id="3ec03-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ec03-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec03-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ec03-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec03-132">CommonParameters</span></span>
<span data-ttu-id="3ec03-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec03-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec03-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec03-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ec03-135">INPUTS</span></span>

### <span data-ttu-id="3ec03-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ec03-136">None</span></span>
<span data-ttu-id="3ec03-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3ec03-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ec03-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ec03-138">OUTPUTS</span></span>

### <span data-ttu-id="3ec03-139">bool</span><span class="sxs-lookup"><span data-stu-id="3ec03-139">bool</span></span>
<span data-ttu-id="3ec03-140">Se PassThru for especificado, retornará o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3ec03-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="3ec03-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ec03-141">NOTES</span></span>

## <span data-ttu-id="3ec03-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ec03-142">RELATED LINKS</span></span>

[<span data-ttu-id="3ec03-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3ec03-144">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3ec03-145">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3ec03-146">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3ec03-147">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3ec03-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3ec03-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


