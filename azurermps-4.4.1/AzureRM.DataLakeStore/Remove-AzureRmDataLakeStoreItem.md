---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439954"
---
# <span data-ttu-id="3b65a-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3b65a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b65a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b65a-103">Exclui um arquivo ou uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b65a-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b65a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b65a-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b65a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b65a-105">DESCRIPTION</span></span>
<span data-ttu-id="3b65a-106">O cmdlet **Remove-AzureRmDataLakeStoreItem** exclui um arquivo ou uma pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="3b65a-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3b65a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b65a-107">EXAMPLES</span></span>

### <span data-ttu-id="3b65a-108">Exemplo 1: remover vários itens</span><span class="sxs-lookup"><span data-stu-id="3b65a-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="3b65a-109">Esse comando remove os arquivos File01.txt e File.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="3b65a-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="3b65a-110">OS</span><span class="sxs-lookup"><span data-stu-id="3b65a-110">PARAMETERS</span></span>

### <span data-ttu-id="3b65a-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="3b65a-111">-Account</span></span>
<span data-ttu-id="3b65a-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b65a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3b65a-113">-Limpar</span><span class="sxs-lookup"><span data-stu-id="3b65a-113">-Clean</span></span>
<span data-ttu-id="3b65a-114">Indica que essa operação remove todo o conteúdo da pasta de destino e mantém a pasta.</span><span class="sxs-lookup"><span data-stu-id="3b65a-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="3b65a-115">Use esse parâmetro com o parâmetro *recurse* .</span><span class="sxs-lookup"><span data-stu-id="3b65a-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="3b65a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3b65a-116">-Force</span></span>
<span data-ttu-id="3b65a-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b65a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b65a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b65a-118">-PassThru</span></span>
<span data-ttu-id="3b65a-119">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3b65a-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b65a-120">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3b65a-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b65a-121">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="3b65a-121">-Paths</span></span>
<span data-ttu-id="3b65a-122">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem removidos, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="3b65a-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3b65a-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3b65a-123">-Recurse</span></span>
<span data-ttu-id="3b65a-124">Indica que essa operação exclui todos os itens da pasta de destino, incluindo subpastas.</span><span class="sxs-lookup"><span data-stu-id="3b65a-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="3b65a-125">A menos que você especifique o parâmetro *Clean* , a pasta de destino também será excluída.</span><span class="sxs-lookup"><span data-stu-id="3b65a-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

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

### <span data-ttu-id="3b65a-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b65a-126">-Confirm</span></span>
<span data-ttu-id="3b65a-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b65a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b65a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b65a-128">-WhatIf</span></span>
<span data-ttu-id="3b65a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b65a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b65a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b65a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b65a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b65a-131">-DefaultProfile</span></span>
<span data-ttu-id="3b65a-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b65a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b65a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b65a-133">CommonParameters</span></span>
<span data-ttu-id="3b65a-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b65a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b65a-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b65a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b65a-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b65a-136">INPUTS</span></span>

## <span data-ttu-id="3b65a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b65a-137">OUTPUTS</span></span>

### <span data-ttu-id="3b65a-138">bool</span><span class="sxs-lookup"><span data-stu-id="3b65a-138">bool</span></span>
<span data-ttu-id="3b65a-139">Se PassThru for especificado, retornará o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="3b65a-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="3b65a-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b65a-140">NOTES</span></span>

## <span data-ttu-id="3b65a-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b65a-141">RELATED LINKS</span></span>

[<span data-ttu-id="3b65a-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b65a-143">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b65a-144">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b65a-145">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b65a-146">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b65a-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b65a-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


