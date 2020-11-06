---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610837"
---
# <span data-ttu-id="da177-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="da177-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="da177-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da177-102">SYNOPSIS</span></span>
<span data-ttu-id="da177-103">Define as propriedades de referência de imagem em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="da177-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da177-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da177-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da177-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da177-105">DESCRIPTION</span></span>
<span data-ttu-id="da177-106">O cmdlet **set-AzureRmDiskUpdateImageReference** define as propriedades de referência de imagem em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="da177-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="da177-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da177-107">EXAMPLES</span></span>

### <span data-ttu-id="da177-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da177-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="da177-109">O primeiro comando cria um objeto de atualização de disco local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="da177-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="da177-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="da177-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="da177-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="da177-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="da177-112">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="da177-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="da177-113">OS</span><span class="sxs-lookup"><span data-stu-id="da177-113">PARAMETERS</span></span>

### <span data-ttu-id="da177-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da177-114">-DefaultProfile</span></span>
<span data-ttu-id="da177-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da177-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da177-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="da177-116">-DiskUpdate</span></span>
<span data-ttu-id="da177-117">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="da177-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da177-118">-ID</span><span class="sxs-lookup"><span data-stu-id="da177-118">-Id</span></span>
<span data-ttu-id="da177-119">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="da177-119">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da177-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="da177-120">-Lun</span></span>
<span data-ttu-id="da177-121">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="da177-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da177-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da177-122">-Confirm</span></span>
<span data-ttu-id="da177-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da177-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da177-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da177-124">-WhatIf</span></span>
<span data-ttu-id="da177-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da177-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da177-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da177-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da177-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da177-127">CommonParameters</span></span>
<span data-ttu-id="da177-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da177-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da177-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da177-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da177-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da177-130">INPUTS</span></span>

### <span data-ttu-id="da177-131">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="da177-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="da177-132">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="da177-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="da177-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da177-133">OUTPUTS</span></span>

### <span data-ttu-id="da177-134">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="da177-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="da177-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da177-135">NOTES</span></span>

## <span data-ttu-id="da177-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da177-136">RELATED LINKS</span></span>

