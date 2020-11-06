---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: 963e6f4621276eda4fdf598d571f2c2171dbc4f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431709"
---
# <span data-ttu-id="777a0-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="777a0-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="777a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="777a0-102">SYNOPSIS</span></span>
<span data-ttu-id="777a0-103">Define as propriedades de referência de imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="777a0-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="777a0-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <Disk> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="777a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="777a0-105">DESCRIPTION</span></span>
<span data-ttu-id="777a0-106">O cmdlet **set-AzureRmDiskImageReference** define as propriedades de referência de imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="777a0-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="777a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="777a0-107">EXAMPLES</span></span>

### <span data-ttu-id="777a0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="777a0-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="777a0-109">O primeiro comando cria um objeto de disco local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="777a0-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="777a0-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="777a0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="777a0-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="777a0-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="777a0-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="777a0-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="777a0-113">OS</span><span class="sxs-lookup"><span data-stu-id="777a0-113">PARAMETERS</span></span>

### <span data-ttu-id="777a0-114">-Disco</span><span class="sxs-lookup"><span data-stu-id="777a0-114">-Disk</span></span>
<span data-ttu-id="777a0-115">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="777a0-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="777a0-116">-ID</span><span class="sxs-lookup"><span data-stu-id="777a0-116">-Id</span></span>
<span data-ttu-id="777a0-117">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="777a0-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="777a0-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="777a0-118">-Lun</span></span>
<span data-ttu-id="777a0-119">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="777a0-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="777a0-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="777a0-120">-Confirm</span></span>
<span data-ttu-id="777a0-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="777a0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="777a0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="777a0-122">-WhatIf</span></span>
<span data-ttu-id="777a0-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="777a0-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="777a0-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="777a0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="777a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777a0-125">CommonParameters</span></span>
<span data-ttu-id="777a0-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="777a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777a0-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="777a0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777a0-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="777a0-128">INPUTS</span></span>

### <span data-ttu-id="777a0-129">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="777a0-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="777a0-130">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="777a0-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="777a0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="777a0-131">OUTPUTS</span></span>

### <span data-ttu-id="777a0-132">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="777a0-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="777a0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="777a0-133">NOTES</span></span>

## <span data-ttu-id="777a0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="777a0-134">RELATED LINKS</span></span>

