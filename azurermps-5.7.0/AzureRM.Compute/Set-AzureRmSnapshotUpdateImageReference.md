---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateImageReference.md
ms.openlocfilehash: fa6b3e16fd137453229232405d31cd7665ccd18e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427606"
---
# <span data-ttu-id="a74d0-101">Set-AzureRmSnapshotUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="a74d0-101">Set-AzureRmSnapshotUpdateImageReference</span></span>

## <span data-ttu-id="a74d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a74d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a74d0-103">Define as propriedades de referência de imagem em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a74d0-103">Sets the image reference properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a74d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a74d0-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateImageReference [-SnapshotUpdate] <SnapshotUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a74d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a74d0-105">DESCRIPTION</span></span>
<span data-ttu-id="a74d0-106">O cmdlet **set-AzureRmSnapshotUpdateImageReference** define as propriedades de referência de imagem em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a74d0-106">The **Set-AzureRmSnapshotUpdateImageReference** cmdlet sets the image reference properties on a snapshot update object.</span></span>

## <span data-ttu-id="a74d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a74d0-107">EXAMPLES</span></span>

### <span data-ttu-id="a74d0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a74d0-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateImageReference -Snapshot $snapshotupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="a74d0-109">O primeiro comando cria um objeto de atualização de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a74d0-109">The first command creates a local snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a74d0-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="a74d0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a74d0-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto de atualização do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a74d0-111">The second command sets the image id and the logical unit number 0 for the snapshot update object.</span></span>
<span data-ttu-id="a74d0-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a74d0-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a74d0-113">OS</span><span class="sxs-lookup"><span data-stu-id="a74d0-113">PARAMETERS</span></span>

### <span data-ttu-id="a74d0-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a74d0-114">-Id</span></span>
<span data-ttu-id="a74d0-115">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="a74d0-115">Specifies the ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a74d0-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="a74d0-116">-Lun</span></span>
<span data-ttu-id="a74d0-117">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="a74d0-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a74d0-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a74d0-118">-SnapshotUpdate</span></span>
<span data-ttu-id="a74d0-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="a74d0-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a74d0-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a74d0-120">-Confirm</span></span>
<span data-ttu-id="a74d0-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a74d0-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a74d0-122">-WhatIf</span></span>
<span data-ttu-id="a74d0-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a74d0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a74d0-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a74d0-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74d0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74d0-125">CommonParameters</span></span>
<span data-ttu-id="a74d0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74d0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74d0-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74d0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74d0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a74d0-128">INPUTS</span></span>

### <span data-ttu-id="a74d0-129">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a74d0-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="a74d0-130">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a74d0-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a74d0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a74d0-131">OUTPUTS</span></span>

### <span data-ttu-id="a74d0-132">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="a74d0-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="a74d0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a74d0-133">NOTES</span></span>

## <span data-ttu-id="a74d0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a74d0-134">RELATED LINKS</span></span>

