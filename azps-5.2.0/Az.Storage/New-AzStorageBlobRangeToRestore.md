---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256959"
---
# <span data-ttu-id="ff1c1-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="ff1c1-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="ff1c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff1c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff1c1-103">Cria um objeto de intervalo de BLOB para restaurar uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="ff1c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff1c1-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff1c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff1c1-105">DESCRIPTION</span></span>
<span data-ttu-id="ff1c1-106">O cmdlet **New-AzStorageBlobRangeToRestore** cria um objeto de intervalo de BLOB, que pode ser usado em Restore-AzStorageBlobRange.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="ff1c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff1c1-107">EXAMPLES</span></span>

### <span data-ttu-id="ff1c1-108">Exemplo 1: cria um intervalo de BLOB para restaurar</span><span class="sxs-lookup"><span data-stu-id="ff1c1-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="ff1c1-109">Esse comando cria um intervalo de BLOB para restaurar, que começa em Container1/blob1 (include) e termina em container2/blob2 (excluir).</span><span class="sxs-lookup"><span data-stu-id="ff1c1-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="ff1c1-110">Exemplo 2: cria um intervalo de BLOB que será restaurado do primeiro blob em ordem alfabética, para um blob específico (excluir)</span><span class="sxs-lookup"><span data-stu-id="ff1c1-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="ff1c1-111">Esse comando cria um intervalo de BLOB que será restaurado do primeiro BLOB da ordem alfabética, para um blob específico container2/blob2 (excluir)</span><span class="sxs-lookup"><span data-stu-id="ff1c1-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="ff1c1-112">Exemplo 3: cria um intervalo de BLOB que será restaurado de um blob específico (include) até o último blob em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="ff1c1-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="ff1c1-113">Esse comando cria um intervalo de BLOB que será restaurado de um blob Container1/blob1 (include) específico para o último blob em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="ff1c1-114">Exemplo 4: cria um intervalo de BLOBs que restaurará todos os BLOBs</span><span class="sxs-lookup"><span data-stu-id="ff1c1-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="ff1c1-115">Esse comando cria um intervalo de BLOB que restaurará todos os BLOBs.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="ff1c1-116">OS</span><span class="sxs-lookup"><span data-stu-id="ff1c1-116">PARAMETERS</span></span>

### <span data-ttu-id="ff1c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff1c1-117">-DefaultProfile</span></span>
<span data-ttu-id="ff1c1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff1c1-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="ff1c1-119">-EndRange</span></span>
<span data-ttu-id="ff1c1-120">Especifique o intervalo final da restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="ff1c1-121">O intervalo final será excluído nos blobs de restauração.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="ff1c1-122">Defina-o como strng vazio para restaurar para o fim.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1c1-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="ff1c1-123">-StartRange</span></span>
<span data-ttu-id="ff1c1-124">Especifique o intervalo inicial da restauração de BLOB.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="ff1c1-125">O intervalo inicial será incluído nos blobs de restauração.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="ff1c1-126">Defina-o como uma cadeia de caracteres vazia para restaurar do início.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff1c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff1c1-127">CommonParameters</span></span>
<span data-ttu-id="ff1c1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff1c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff1c1-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff1c1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff1c1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff1c1-130">INPUTS</span></span>

### <span data-ttu-id="ff1c1-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ff1c1-131">None</span></span>

## <span data-ttu-id="ff1c1-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff1c1-132">OUTPUTS</span></span>

### <span data-ttu-id="ff1c1-133">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="ff1c1-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="ff1c1-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff1c1-134">NOTES</span></span>

## <span data-ttu-id="ff1c1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff1c1-135">RELATED LINKS</span></span>
