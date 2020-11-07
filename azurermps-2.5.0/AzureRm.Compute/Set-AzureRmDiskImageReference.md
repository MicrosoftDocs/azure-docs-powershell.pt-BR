---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785962"
---
# <span data-ttu-id="2bc53-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="2bc53-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="2bc53-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2bc53-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc53-103">Define as propriedades de referência de imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="2bc53-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2bc53-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc53-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2bc53-105">DESCRIPTION</span></span>
<span data-ttu-id="2bc53-106">O cmdlet **set-AzureRmDiskImageReference** define as propriedades de referência de imagem em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="2bc53-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="2bc53-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2bc53-107">EXAMPLES</span></span>

### <span data-ttu-id="2bc53-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2bc53-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="2bc53-109">O primeiro comando cria um objeto de disco local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2bc53-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2bc53-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="2bc53-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="2bc53-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="2bc53-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="2bc53-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2bc53-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2bc53-113">OS</span><span class="sxs-lookup"><span data-stu-id="2bc53-113">PARAMETERS</span></span>

### <span data-ttu-id="2bc53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc53-114">-DefaultProfile</span></span>
<span data-ttu-id="2bc53-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc53-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc53-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="2bc53-116">-Disk</span></span>
<span data-ttu-id="2bc53-117">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="2bc53-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bc53-118">-ID</span><span class="sxs-lookup"><span data-stu-id="2bc53-118">-Id</span></span>
<span data-ttu-id="2bc53-119">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="2bc53-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="2bc53-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="2bc53-120">-Lun</span></span>
<span data-ttu-id="2bc53-121">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="2bc53-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="2bc53-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2bc53-122">-Confirm</span></span>
<span data-ttu-id="2bc53-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bc53-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc53-124">-WhatIf</span></span>
<span data-ttu-id="2bc53-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2bc53-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bc53-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2bc53-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc53-127">CommonParameters</span></span>
<span data-ttu-id="2bc53-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc53-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc53-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc53-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2bc53-130">INPUTS</span></span>

### <span data-ttu-id="2bc53-131">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="2bc53-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="2bc53-132">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2bc53-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2bc53-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2bc53-133">OUTPUTS</span></span>

### <span data-ttu-id="2bc53-134">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="2bc53-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="2bc53-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2bc53-135">NOTES</span></span>

## <span data-ttu-id="2bc53-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2bc53-136">RELATED LINKS</span></span>

