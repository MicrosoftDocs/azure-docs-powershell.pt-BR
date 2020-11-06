---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426788"
---
# <span data-ttu-id="4b6ef-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="4b6ef-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="4b6ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b6ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4b6ef-103">Define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b6ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b6ef-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b6ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b6ef-105">DESCRIPTION</span></span>
<span data-ttu-id="4b6ef-106">O cmdlet **set-AzureRmSnapshotImageReference** define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="4b6ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b6ef-107">EXAMPLES</span></span>

### <span data-ttu-id="4b6ef-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b6ef-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="4b6ef-109">O primeiro comando cria um objeto de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="4b6ef-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="4b6ef-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="4b6ef-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="4b6ef-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4b6ef-113">OS</span><span class="sxs-lookup"><span data-stu-id="4b6ef-113">PARAMETERS</span></span>

### <span data-ttu-id="4b6ef-114">-ID</span><span class="sxs-lookup"><span data-stu-id="4b6ef-114">-Id</span></span>
<span data-ttu-id="4b6ef-115">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="4b6ef-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="4b6ef-116">-Lun</span></span>
<span data-ttu-id="4b6ef-117">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="4b6ef-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="4b6ef-118">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="4b6ef-118">-Snapshot</span></span>
<span data-ttu-id="4b6ef-119">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b6ef-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b6ef-120">-Confirm</span></span>
<span data-ttu-id="4b6ef-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b6ef-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b6ef-122">-WhatIf</span></span>
<span data-ttu-id="4b6ef-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b6ef-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b6ef-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b6ef-125">CommonParameters</span></span>
<span data-ttu-id="4b6ef-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b6ef-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b6ef-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b6ef-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b6ef-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b6ef-128">INPUTS</span></span>

### <span data-ttu-id="4b6ef-129">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="4b6ef-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="4b6ef-130">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4b6ef-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4b6ef-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b6ef-131">OUTPUTS</span></span>

### <span data-ttu-id="4b6ef-132">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="4b6ef-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="4b6ef-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b6ef-133">NOTES</span></span>

## <span data-ttu-id="4b6ef-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b6ef-134">RELATED LINKS</span></span>

