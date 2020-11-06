---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 5d5ca3f06ec76f45a8bb33aa5d4b810283ffce97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429557"
---
# <span data-ttu-id="ecd6a-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd6a-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="ecd6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd6a-103">Define a política de tamanhos de máquinas virtuais permitidos de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecd6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecd6a-104">SYNTAX</span></span>

### <span data-ttu-id="ecd6a-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecd6a-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd6a-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="ecd6a-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd6a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecd6a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecd6a-108">O cmdlet **set-AzureRmDtlAllowedVMSizesPolicy** define a política de tamanhos de máquinas virtuais permitidos, que especifica uma lista de tamanhos de máquinas virtuais permitidos em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="ecd6a-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ecd6a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-110">EXAMPLES</span></span>

## <span data-ttu-id="ecd6a-111">OS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-111">PARAMETERS</span></span>

### <span data-ttu-id="ecd6a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd6a-112">-DefaultProfile</span></span>
<span data-ttu-id="ecd6a-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ecd6a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecd6a-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="ecd6a-114">-Disable</span></span>
<span data-ttu-id="ecd6a-115">Indica que esse cmdlet desabilita a política.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="ecd6a-116">-Enable</span></span>
<span data-ttu-id="ecd6a-117">Indica que esse cmdlet habilita a política.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="ecd6a-118">-LabName</span></span>
<span data-ttu-id="ecd6a-119">Especifica o nome do laboratório para o qual esse cmdlet define a política de tamanhos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="ecd6a-121">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="ecd6a-122">-VmSizes</span></span>
<span data-ttu-id="ecd6a-123">Especifica, como uma matriz de cadeia de caracteres, a lista de tamanhos de máquinas virtuais permitidos no laboratório.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecd6a-124">-Confirm</span></span>
<span data-ttu-id="ecd6a-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd6a-126">-WhatIf</span></span>
<span data-ttu-id="ecd6a-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd6a-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd6a-129">CommonParameters</span></span>
<span data-ttu-id="ecd6a-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd6a-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd6a-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecd6a-132">INPUTS</span></span>

### <span data-ttu-id="ecd6a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd6a-133">System.String</span></span>

## <span data-ttu-id="ecd6a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecd6a-134">OUTPUTS</span></span>

### <span data-ttu-id="ecd6a-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd6a-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ecd6a-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecd6a-136">NOTES</span></span>

## <span data-ttu-id="ecd6a-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecd6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="ecd6a-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd6a-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)

