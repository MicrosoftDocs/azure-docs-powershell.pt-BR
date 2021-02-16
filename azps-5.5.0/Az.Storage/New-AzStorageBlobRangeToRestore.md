---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116335"
---
# <span data-ttu-id="47b7d-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="47b7d-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="47b7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="47b7d-103">Cria um objeto de Intervalo de Blob para restaurar uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47b7d-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="47b7d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47b7d-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b7d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="47b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="47b7d-106">O cmdlet **New-AzStorageBrangeRangeToRestore** cria um objeto de intervalo blob, que pode ser usado em Restore-AzStorageBrangeRange.</span><span class="sxs-lookup"><span data-stu-id="47b7d-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="47b7d-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="47b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="47b7d-108">Exemplo 1: cria um intervalo de blob para restaurar</span><span class="sxs-lookup"><span data-stu-id="47b7d-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="47b7d-109">Esse comando cria um intervalo de blob para restaurar, que começa no contêiner1/blob1 (incluir) e termina no contêiner2/blob2 (excluir).</span><span class="sxs-lookup"><span data-stu-id="47b7d-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="47b7d-110">Exemplo 2: cria um intervalo de blob que será restaurado do primeiro blob em ordem alfabética para um blob específico (excluir)</span><span class="sxs-lookup"><span data-stu-id="47b7d-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="47b7d-111">Esse comando cria um intervalo de blob que será restaurado do primeiro blob da ordem alfabética para um contêiner de blob específico2/blob2 (excluir)</span><span class="sxs-lookup"><span data-stu-id="47b7d-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="47b7d-112">Exemplo 3: cria um intervalo de blob que será restaurado de um blob específico (incluir) até o último blob em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="47b7d-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="47b7d-113">Esse comando cria um intervalo de blob que será restaurado de um contêiner de blob1/blob1 específico (incluir) até o último blob em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="47b7d-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="47b7d-114">Exemplo 4: cria um intervalo de blobs que restaurará todos os blobs</span><span class="sxs-lookup"><span data-stu-id="47b7d-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="47b7d-115">Esse comando cria um intervalo de blobs que restaurará todos os blobs.</span><span class="sxs-lookup"><span data-stu-id="47b7d-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="47b7d-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47b7d-116">PARAMETERS</span></span>

### <span data-ttu-id="47b7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b7d-117">-DefaultProfile</span></span>
<span data-ttu-id="47b7d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47b7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b7d-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="47b7d-119">-EndRange</span></span>
<span data-ttu-id="47b7d-120">Especifique o intervalo final de restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="47b7d-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="47b7d-121">O intervalo final será excluído na restauração de blobs.</span><span class="sxs-lookup"><span data-stu-id="47b7d-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="47b7d-122">De defini-lo como um strng vazio para restaurar até o fim.</span><span class="sxs-lookup"><span data-stu-id="47b7d-122">Set it as empty strng to restore to the end.</span></span>

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

### <span data-ttu-id="47b7d-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="47b7d-123">-StartRange</span></span>
<span data-ttu-id="47b7d-124">Especifique o intervalo inicial de restauração de blob.</span><span class="sxs-lookup"><span data-stu-id="47b7d-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="47b7d-125">O intervalo inicial será incluído na restauração de blobs.</span><span class="sxs-lookup"><span data-stu-id="47b7d-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="47b7d-126">De defini-la como cadeia de caracteres vazia para restaurar do começo.</span><span class="sxs-lookup"><span data-stu-id="47b7d-126">Set it as empty string to restore from begining.</span></span>

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

### <span data-ttu-id="47b7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b7d-127">CommonParameters</span></span>
<span data-ttu-id="47b7d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b7d-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b7d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b7d-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="47b7d-130">INPUTS</span></span>

### <span data-ttu-id="47b7d-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="47b7d-131">None</span></span>

## <span data-ttu-id="47b7d-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="47b7d-132">OUTPUTS</span></span>

### <span data-ttu-id="47b7d-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBstoreRestoreRange</span><span class="sxs-lookup"><span data-stu-id="47b7d-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="47b7d-134">Notas</span><span class="sxs-lookup"><span data-stu-id="47b7d-134">NOTES</span></span>

## <span data-ttu-id="47b7d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47b7d-135">RELATED LINKS</span></span>
