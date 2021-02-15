---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113865"
---
# <span data-ttu-id="a3529-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="a3529-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="a3529-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3529-102">SYNOPSIS</span></span>
<span data-ttu-id="a3529-103">Obtém a lista de itens em uma pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3529-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3529-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3529-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3529-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3529-105">DESCRIPTION</span></span>
<span data-ttu-id="a3529-106">O cmdlet **Get-AzDataLakeStoreChildItem** obtém a lista de itens em uma pasta na Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3529-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3529-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3529-107">EXAMPLES</span></span>

### <span data-ttu-id="a3529-108">Exemplo 1: Obter os itens filho de uma pasta</span><span class="sxs-lookup"><span data-stu-id="a3529-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="a3529-109">Esse comando obtém os itens filho da pasta MeusArquivos.</span><span class="sxs-lookup"><span data-stu-id="a3529-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="a3529-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3529-110">PARAMETERS</span></span>

### <span data-ttu-id="a3529-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="a3529-111">-Account</span></span>
<span data-ttu-id="a3529-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3529-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a3529-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3529-113">-DefaultProfile</span></span>
<span data-ttu-id="a3529-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a3529-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3529-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="a3529-115">-Path</span></span>
<span data-ttu-id="a3529-116">Especifica o caminho do Data Lake Store da pasta, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="a3529-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a3529-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3529-117">CommonParameters</span></span>
<span data-ttu-id="a3529-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3529-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3529-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3529-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3529-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3529-120">INPUTS</span></span>

### <span data-ttu-id="a3529-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a3529-121">System.String</span></span>

### <span data-ttu-id="a3529-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a3529-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="a3529-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3529-123">OUTPUTS</span></span>

### <span data-ttu-id="a3529-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3529-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="a3529-125">Notas</span><span class="sxs-lookup"><span data-stu-id="a3529-125">NOTES</span></span>

## <span data-ttu-id="a3529-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3529-126">RELATED LINKS</span></span>
