---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596787"
---
# <span data-ttu-id="007a4-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="007a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="007a4-102">SYNOPSIS</span></span>
<span data-ttu-id="007a4-103">Testa a existência de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="007a4-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="007a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="007a4-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="007a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="007a4-105">DESCRIPTION</span></span>
<span data-ttu-id="007a4-106">O cmdlet **Test-AzDataLakeStoreItem** testa a existência de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="007a4-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="007a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="007a4-107">EXAMPLES</span></span>

### <span data-ttu-id="007a4-108">Exemplo 1: testar um arquivo</span><span class="sxs-lookup"><span data-stu-id="007a4-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="007a4-109">Esse comando testa se o arquivo Test.csv existe na conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="007a4-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="007a4-110">OS</span><span class="sxs-lookup"><span data-stu-id="007a4-110">PARAMETERS</span></span>

### <span data-ttu-id="007a4-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="007a4-111">-Account</span></span>
<span data-ttu-id="007a4-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="007a4-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="007a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="007a4-113">-DefaultProfile</span></span>
<span data-ttu-id="007a4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="007a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="007a4-115">-Caminho</span><span class="sxs-lookup"><span data-stu-id="007a4-115">-Path</span></span>
<span data-ttu-id="007a4-116">Especifica o caminho do repositório data Lake do item a ser testado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="007a4-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="007a4-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="007a4-117">-PathType</span></span>
<span data-ttu-id="007a4-118">Especifica o tipo de item para testar.</span><span class="sxs-lookup"><span data-stu-id="007a4-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="007a4-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="007a4-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="007a4-120">Qualquer</span><span class="sxs-lookup"><span data-stu-id="007a4-120">Any</span></span> 
- <span data-ttu-id="007a4-121">Arquivos</span><span class="sxs-lookup"><span data-stu-id="007a4-121">File</span></span> 
- <span data-ttu-id="007a4-122">La</span><span class="sxs-lookup"><span data-stu-id="007a4-122">Folder</span></span>

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

### <span data-ttu-id="007a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="007a4-123">CommonParameters</span></span>
<span data-ttu-id="007a4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="007a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="007a4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="007a4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="007a4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="007a4-126">INPUTS</span></span>

### <span data-ttu-id="007a4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="007a4-127">System.String</span></span>

### <span data-ttu-id="007a4-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="007a4-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="007a4-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="007a4-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="007a4-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="007a4-130">OUTPUTS</span></span>

### <span data-ttu-id="007a4-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="007a4-131">System.Boolean</span></span>

## <span data-ttu-id="007a4-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="007a4-132">NOTES</span></span>

## <span data-ttu-id="007a4-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="007a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="007a4-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="007a4-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="007a4-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="007a4-137">Ingressar em AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="007a4-138">Mover-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="007a4-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="007a4-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


