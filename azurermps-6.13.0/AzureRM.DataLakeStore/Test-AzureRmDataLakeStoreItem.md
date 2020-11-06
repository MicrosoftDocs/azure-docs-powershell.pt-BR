---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433258"
---
# <span data-ttu-id="95f73-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="95f73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95f73-102">SYNOPSIS</span></span>
<span data-ttu-id="95f73-103">Testa a existência de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95f73-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95f73-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f73-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95f73-105">DESCRIPTION</span></span>
<span data-ttu-id="95f73-106">O cmdlet **Test-AzureRmDataLakeStoreItem** testa a existência de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95f73-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95f73-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95f73-107">EXAMPLES</span></span>

### <span data-ttu-id="95f73-108">Exemplo 1: testar um arquivo</span><span class="sxs-lookup"><span data-stu-id="95f73-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="95f73-109">Esse comando testa se o arquivo Test.csv existe na conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="95f73-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="95f73-110">OS</span><span class="sxs-lookup"><span data-stu-id="95f73-110">PARAMETERS</span></span>

### <span data-ttu-id="95f73-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="95f73-111">-Account</span></span>
<span data-ttu-id="95f73-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="95f73-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="95f73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f73-113">-DefaultProfile</span></span>
<span data-ttu-id="95f73-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95f73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f73-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="95f73-115">-Path</span></span>
<span data-ttu-id="95f73-116">Especifica o caminho do repositório data Lake do item a ser testado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="95f73-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="95f73-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="95f73-117">-PathType</span></span>
<span data-ttu-id="95f73-118">Especifica o tipo de item para testar.</span><span class="sxs-lookup"><span data-stu-id="95f73-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="95f73-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="95f73-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="95f73-120">Qualquer</span><span class="sxs-lookup"><span data-stu-id="95f73-120">Any</span></span> 
- <span data-ttu-id="95f73-121">Arquivos</span><span class="sxs-lookup"><span data-stu-id="95f73-121">File</span></span> 
- <span data-ttu-id="95f73-122">La</span><span class="sxs-lookup"><span data-stu-id="95f73-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95f73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f73-123">CommonParameters</span></span>
<span data-ttu-id="95f73-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95f73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f73-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f73-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f73-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95f73-126">INPUTS</span></span>

### <span data-ttu-id="95f73-127">System. String</span><span class="sxs-lookup"><span data-stu-id="95f73-127">System.String</span></span>

### <span data-ttu-id="95f73-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="95f73-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="95f73-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="95f73-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="95f73-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95f73-130">OUTPUTS</span></span>

### <span data-ttu-id="95f73-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95f73-131">System.Boolean</span></span>

## <span data-ttu-id="95f73-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95f73-132">NOTES</span></span>

## <span data-ttu-id="95f73-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95f73-133">RELATED LINKS</span></span>

[<span data-ttu-id="95f73-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95f73-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95f73-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95f73-137">Ingressar em AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95f73-138">Mover-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95f73-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95f73-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


