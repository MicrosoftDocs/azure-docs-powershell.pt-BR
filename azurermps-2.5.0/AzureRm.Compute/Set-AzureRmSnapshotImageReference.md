---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotimagereference
schema: 2.0.0
ms.openlocfilehash: d3ad489ae1e61b1e2543f7ef75fae2fd93e33a03
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785358"
---
# <span data-ttu-id="bc0ec-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="bc0ec-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="bc0ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="bc0ec-103">Define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc0ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc0ec-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc0ec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc0ec-105">DESCRIPTION</span></span>
<span data-ttu-id="bc0ec-106">O cmdlet **set-AzureRmSnapshotImageReference** define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="bc0ec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc0ec-107">EXAMPLES</span></span>

### <span data-ttu-id="bc0ec-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc0ec-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="bc0ec-109">O primeiro comando cria um objeto de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="bc0ec-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="bc0ec-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="bc0ec-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="bc0ec-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="bc0ec-113">OS</span><span class="sxs-lookup"><span data-stu-id="bc0ec-113">PARAMETERS</span></span>

### <span data-ttu-id="bc0ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc0ec-114">-DefaultProfile</span></span>
<span data-ttu-id="bc0ec-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc0ec-116">-ID</span><span class="sxs-lookup"><span data-stu-id="bc0ec-116">-Id</span></span>
<span data-ttu-id="bc0ec-117">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="bc0ec-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="bc0ec-118">-Lun</span></span>
<span data-ttu-id="bc0ec-119">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="bc0ec-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="bc0ec-120">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="bc0ec-120">-Snapshot</span></span>
<span data-ttu-id="bc0ec-121">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc0ec-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc0ec-122">-Confirm</span></span>
<span data-ttu-id="bc0ec-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc0ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc0ec-124">-WhatIf</span></span>
<span data-ttu-id="bc0ec-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc0ec-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc0ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc0ec-127">CommonParameters</span></span>
<span data-ttu-id="bc0ec-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc0ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc0ec-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc0ec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc0ec-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc0ec-130">INPUTS</span></span>

### <span data-ttu-id="bc0ec-131">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="bc0ec-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="bc0ec-132">System. String System. Nullable ' 1 [System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bc0ec-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bc0ec-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc0ec-133">OUTPUTS</span></span>

### <span data-ttu-id="bc0ec-134">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="bc0ec-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="bc0ec-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc0ec-135">NOTES</span></span>

## <span data-ttu-id="bc0ec-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc0ec-136">RELATED LINKS</span></span>

