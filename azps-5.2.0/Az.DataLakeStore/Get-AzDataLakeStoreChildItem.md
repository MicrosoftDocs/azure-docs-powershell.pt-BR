---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261524"
---
# <span data-ttu-id="03d9f-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="03d9f-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="03d9f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="03d9f-102">SYNOPSIS</span></span>
<span data-ttu-id="03d9f-103">Obtém a lista de itens em uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03d9f-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="03d9f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="03d9f-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03d9f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="03d9f-105">DESCRIPTION</span></span>
<span data-ttu-id="03d9f-106">O cmdlet **Get-AzDataLakeStoreChildItem** Obtém a lista de itens em uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03d9f-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="03d9f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="03d9f-107">EXAMPLES</span></span>

### <span data-ttu-id="03d9f-108">Exemplo 1: obter os itens filhos para uma pasta</span><span class="sxs-lookup"><span data-stu-id="03d9f-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="03d9f-109">Esse comando obtém os itens filhos para a pasta myfiles.</span><span class="sxs-lookup"><span data-stu-id="03d9f-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="03d9f-110">OS</span><span class="sxs-lookup"><span data-stu-id="03d9f-110">PARAMETERS</span></span>

### <span data-ttu-id="03d9f-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="03d9f-111">-Account</span></span>
<span data-ttu-id="03d9f-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="03d9f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="03d9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d9f-113">-DefaultProfile</span></span>
<span data-ttu-id="03d9f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="03d9f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03d9f-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="03d9f-115">-Path</span></span>
<span data-ttu-id="03d9f-116">Especifica o caminho do repositório data Lake da pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="03d9f-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="03d9f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d9f-117">CommonParameters</span></span>
<span data-ttu-id="03d9f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03d9f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d9f-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d9f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d9f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="03d9f-120">INPUTS</span></span>

### <span data-ttu-id="03d9f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="03d9f-121">System.String</span></span>

### <span data-ttu-id="03d9f-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="03d9f-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="03d9f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="03d9f-123">OUTPUTS</span></span>

### <span data-ttu-id="03d9f-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="03d9f-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="03d9f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="03d9f-125">NOTES</span></span>

## <span data-ttu-id="03d9f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="03d9f-126">RELATED LINKS</span></span>
