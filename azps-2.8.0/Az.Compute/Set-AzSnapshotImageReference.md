---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 390e00273cb23b5d6b922bc7904a935d802206fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597242"
---
# <span data-ttu-id="fc2c3-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="fc2c3-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="fc2c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2c3-103">Define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="fc2c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc2c3-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2c3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="fc2c3-106">O cmdlet **set-AzSnapshotImageReference** define as propriedades de referência de imagem em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="fc2c3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc2c3-107">EXAMPLES</span></span>

### <span data-ttu-id="fc2c3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc2c3-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="fc2c3-109">O primeiro comando cria um objeto de instantâneo local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="fc2c3-110">Ele também define o tipo de sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="fc2c3-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto do instantâneo.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="fc2c3-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fc2c3-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fc2c3-113">OS</span><span class="sxs-lookup"><span data-stu-id="fc2c3-113">PARAMETERS</span></span>

### <span data-ttu-id="fc2c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2c3-114">-DefaultProfile</span></span>
<span data-ttu-id="fc2c3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc2c3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="fc2c3-116">-Id</span></span>
<span data-ttu-id="fc2c3-117">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="fc2c3-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="fc2c3-118">-Lun</span></span>
<span data-ttu-id="fc2c3-119">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="fc2c3-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="fc2c3-120">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="fc2c3-120">-Snapshot</span></span>
<span data-ttu-id="fc2c3-121">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="fc2c3-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc2c3-122">-Confirm</span></span>
<span data-ttu-id="fc2c3-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2c3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2c3-124">-WhatIf</span></span>
<span data-ttu-id="fc2c3-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc2c3-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2c3-127">CommonParameters</span></span>
<span data-ttu-id="fc2c3-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc2c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2c3-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc2c3-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2c3-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc2c3-130">INPUTS</span></span>

### <span data-ttu-id="fc2c3-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc2c3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="fc2c3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fc2c3-132">System.String</span></span>

### <span data-ttu-id="fc2c3-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fc2c3-133">System.Int32</span></span>

## <span data-ttu-id="fc2c3-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc2c3-134">OUTPUTS</span></span>

### <span data-ttu-id="fc2c3-135">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fc2c3-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="fc2c3-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc2c3-136">NOTES</span></span>

## <span data-ttu-id="fc2c3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc2c3-137">RELATED LINKS</span></span>
