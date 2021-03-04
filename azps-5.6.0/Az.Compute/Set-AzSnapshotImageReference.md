---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 6746bc96f7c1a14d617f3147676556be7402b71c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892654"
---
# <span data-ttu-id="8e80e-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="8e80e-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="8e80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e80e-102">SYNOPSIS</span></span>
<span data-ttu-id="8e80e-103">Define as propriedades de referência da imagem em um objeto instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8e80e-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="8e80e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8e80e-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e80e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8e80e-105">DESCRIPTION</span></span>
<span data-ttu-id="8e80e-106">O cmdlet **Set-AzSnapshotImageReference** define as propriedades de referência da imagem em um objeto instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8e80e-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="8e80e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e80e-107">EXAMPLES</span></span>

### <span data-ttu-id="8e80e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e80e-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="8e80e-109">O primeiro comando cria um objeto instantâneo local com tamanho de 10 GB Premium_LRS de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e80e-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="8e80e-110">Ele também define o tipo de sistema operacional do Windows.</span><span class="sxs-lookup"><span data-stu-id="8e80e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="8e80e-111">O segundo comando define a ID da imagem e o número da unidade lógica 0 para o objeto instantâneo.</span><span class="sxs-lookup"><span data-stu-id="8e80e-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="8e80e-112">O último comando pega o objeto instantâneo e cria um instantâneo com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="8e80e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8e80e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8e80e-113">PARAMETERS</span></span>

### <span data-ttu-id="8e80e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e80e-114">-DefaultProfile</span></span>
<span data-ttu-id="8e80e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8e80e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e80e-116">-Id</span><span class="sxs-lookup"><span data-stu-id="8e80e-116">-Id</span></span>
<span data-ttu-id="8e80e-117">Especifica a ID.</span><span class="sxs-lookup"><span data-stu-id="8e80e-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="8e80e-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="8e80e-118">-Lun</span></span>
<span data-ttu-id="8e80e-119">Especifica o número da unidade lógica (LUN).</span><span class="sxs-lookup"><span data-stu-id="8e80e-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="8e80e-120">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="8e80e-120">-Snapshot</span></span>
<span data-ttu-id="8e80e-121">Especifica um objeto instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="8e80e-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="8e80e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e80e-122">-Confirm</span></span>
<span data-ttu-id="8e80e-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e80e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e80e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e80e-124">-WhatIf</span></span>
<span data-ttu-id="8e80e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e80e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e80e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e80e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e80e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e80e-127">CommonParameters</span></span>
<span data-ttu-id="8e80e-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e80e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e80e-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e80e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e80e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e80e-130">INPUTS</span></span>

### <span data-ttu-id="8e80e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8e80e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="8e80e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8e80e-132">System.String</span></span>

### <span data-ttu-id="8e80e-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="8e80e-133">System.Int32</span></span>

## <span data-ttu-id="8e80e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8e80e-134">OUTPUTS</span></span>

### <span data-ttu-id="8e80e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="8e80e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="8e80e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="8e80e-136">NOTES</span></span>

## <span data-ttu-id="8e80e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e80e-137">RELATED LINKS</span></span>
