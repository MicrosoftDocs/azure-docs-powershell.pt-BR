---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 64cf2a14791796e2796f15e446e6ceb29b5b24cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602957"
---
# <span data-ttu-id="d62db-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="d62db-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="d62db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d62db-102">SYNOPSIS</span></span>
<span data-ttu-id="d62db-103">Obtém a lista de itens em uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d62db-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d62db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d62db-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d62db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d62db-105">DESCRIPTION</span></span>
<span data-ttu-id="d62db-106">O cmdlet **Get-AzureRmDataLakeStoreChildItem** Obtém a lista de itens em uma pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d62db-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d62db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d62db-107">EXAMPLES</span></span>

### <span data-ttu-id="d62db-108">Exemplo 1: obter os itens filhos para uma pasta</span><span class="sxs-lookup"><span data-stu-id="d62db-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="d62db-109">Esse comando obtém os itens filhos para a pasta myfiles.</span><span class="sxs-lookup"><span data-stu-id="d62db-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="d62db-110">OS</span><span class="sxs-lookup"><span data-stu-id="d62db-110">PARAMETERS</span></span>

### <span data-ttu-id="d62db-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d62db-111">-Account</span></span>
<span data-ttu-id="d62db-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d62db-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d62db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62db-113">-DefaultProfile</span></span>
<span data-ttu-id="d62db-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d62db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d62db-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d62db-115">-Path</span></span>
<span data-ttu-id="d62db-116">Especifica o caminho do repositório data Lake da pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="d62db-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d62db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62db-117">CommonParameters</span></span>
<span data-ttu-id="d62db-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62db-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62db-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62db-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d62db-120">INPUTS</span></span>

### <span data-ttu-id="d62db-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d62db-121">System.String</span></span>

### <span data-ttu-id="d62db-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d62db-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d62db-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d62db-123">OUTPUTS</span></span>

### <span data-ttu-id="d62db-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d62db-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d62db-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d62db-125">NOTES</span></span>

## <span data-ttu-id="d62db-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d62db-126">RELATED LINKS</span></span>
