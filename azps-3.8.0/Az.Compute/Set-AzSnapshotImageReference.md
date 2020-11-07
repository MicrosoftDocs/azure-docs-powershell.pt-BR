---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944890"
---
# <span data-ttu-id="500b1-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="500b1-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="500b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="500b1-102">SYNOPSIS</span></span>
<span data-ttu-id="500b1-103">Define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="500b1-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="500b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="500b1-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="500b1-105">DESCRIPTION</span></span>
<span data-ttu-id="500b1-106">O cmdlet **set-AzSnapshotImageReference** define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="500b1-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="500b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="500b1-107">EXAMPLES</span></span>

### <span data-ttu-id="500b1-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="500b1-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="500b1-109">O primeiro comando cria um objeto de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="500b1-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="500b1-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="500b1-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="500b1-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="500b1-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="500b1-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="500b1-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="500b1-113">OS</span><span class="sxs-lookup"><span data-stu-id="500b1-113">PARAMETERS</span></span>

### <span data-ttu-id="500b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500b1-114">-DefaultProfile</span></span>
<span data-ttu-id="500b1-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="500b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="500b1-116">-ID</span><span class="sxs-lookup"><span data-stu-id="500b1-116">-Id</span></span>
<span data-ttu-id="500b1-117">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="500b1-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="500b1-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="500b1-118">-Lun</span></span>
<span data-ttu-id="500b1-119">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="500b1-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="500b1-120">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="500b1-120">-Snapshot</span></span>
<span data-ttu-id="500b1-121">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="500b1-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="500b1-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="500b1-122">-Confirm</span></span>
<span data-ttu-id="500b1-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500b1-124">-WhatIf</span></span>
<span data-ttu-id="500b1-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="500b1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="500b1-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="500b1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500b1-127">CommonParameters</span></span>
<span data-ttu-id="500b1-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500b1-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="500b1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500b1-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="500b1-130">INPUTS</span></span>

### <span data-ttu-id="500b1-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="500b1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="500b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="500b1-132">System.String</span></span>

### <span data-ttu-id="500b1-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="500b1-133">System.Int32</span></span>

## <span data-ttu-id="500b1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="500b1-134">OUTPUTS</span></span>

### <span data-ttu-id="500b1-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="500b1-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="500b1-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="500b1-136">NOTES</span></span>

## <span data-ttu-id="500b1-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="500b1-137">RELATED LINKS</span></span>
