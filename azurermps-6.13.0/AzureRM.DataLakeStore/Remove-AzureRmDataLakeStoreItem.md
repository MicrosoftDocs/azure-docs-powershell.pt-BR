---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 03e43530a044bad5f3ea7509fa649da9f26a93f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426369"
---
# <span data-ttu-id="9f6de-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="9f6de-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f6de-102">SYNOPSIS</span></span>
<span data-ttu-id="9f6de-103">Exclui um arquivo ou uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f6de-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f6de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f6de-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f6de-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f6de-105">DESCRIPTION</span></span>
<span data-ttu-id="9f6de-106">O cmdlet **Remove-AzureRmDataLakeStoreItem** exclui um arquivo ou uma pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="9f6de-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9f6de-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f6de-107">EXAMPLES</span></span>

### <span data-ttu-id="9f6de-108">Exemplo 1: remover vários itens</span><span class="sxs-lookup"><span data-stu-id="9f6de-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="9f6de-109">Esse comando remove os arquivos File01.txt e File.csv do repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="9f6de-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="9f6de-110">OS</span><span class="sxs-lookup"><span data-stu-id="9f6de-110">PARAMETERS</span></span>

### <span data-ttu-id="9f6de-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="9f6de-111">-Account</span></span>
<span data-ttu-id="9f6de-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9f6de-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9f6de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f6de-113">-DefaultProfile</span></span>
<span data-ttu-id="9f6de-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f6de-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f6de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9f6de-115">-Force</span></span>
<span data-ttu-id="9f6de-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9f6de-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f6de-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f6de-117">-PassThru</span></span>
<span data-ttu-id="9f6de-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9f6de-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f6de-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9f6de-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f6de-120">-Caminhos</span><span class="sxs-lookup"><span data-stu-id="9f6de-120">-Paths</span></span>
<span data-ttu-id="9f6de-121">Especifica uma matriz de caminhos do repositório de data Lake dos arquivos a serem removidos, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="9f6de-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9f6de-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9f6de-122">-Recurse</span></span>
<span data-ttu-id="9f6de-123">Indica que essa operação exclui todos os itens da pasta de destino, incluindo subpastas.</span><span class="sxs-lookup"><span data-stu-id="9f6de-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="9f6de-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9f6de-124">-Confirm</span></span>
<span data-ttu-id="9f6de-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f6de-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f6de-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f6de-126">-WhatIf</span></span>
<span data-ttu-id="9f6de-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f6de-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f6de-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f6de-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f6de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f6de-129">CommonParameters</span></span>
<span data-ttu-id="9f6de-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f6de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f6de-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f6de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f6de-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f6de-132">INPUTS</span></span>

### <span data-ttu-id="9f6de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f6de-133">System.String</span></span>

### <span data-ttu-id="9f6de-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="9f6de-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="9f6de-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f6de-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f6de-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f6de-136">OUTPUTS</span></span>

### <span data-ttu-id="9f6de-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f6de-137">System.Boolean</span></span>

## <span data-ttu-id="9f6de-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f6de-138">NOTES</span></span>

## <span data-ttu-id="9f6de-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f6de-139">RELATED LINKS</span></span>

[<span data-ttu-id="9f6de-140">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-140">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="9f6de-141">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-141">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="9f6de-142">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-142">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="9f6de-143">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-143">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="9f6de-144">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-144">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="9f6de-145">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9f6de-145">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


