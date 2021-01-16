---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3e06b4f1236863e208a167024e9d0562dc82ca89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257533"
---
# <span data-ttu-id="9dcf8-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="9dcf8-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="9dcf8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcf8-103">Define a política de máquinas virtuais por laboratório de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="9dcf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9dcf8-104">SYNTAX</span></span>

### <span data-ttu-id="9dcf8-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="9dcf8-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dcf8-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="9dcf8-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dcf8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9dcf8-107">DESCRIPTION</span></span>
<span data-ttu-id="9dcf8-108">O cmdlet **set-AzDtlVMsPerLabPolicy** define as máquinas virtuais por política de laboratório de um laboratório, que define o número total de máquinas virtuais permitidas em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="9dcf8-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="9dcf8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9dcf8-110">EXAMPLES</span></span>

## <span data-ttu-id="9dcf8-111">OS</span><span class="sxs-lookup"><span data-stu-id="9dcf8-111">PARAMETERS</span></span>

### <span data-ttu-id="9dcf8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dcf8-112">-DefaultProfile</span></span>
<span data-ttu-id="9dcf8-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9dcf8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dcf8-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="9dcf8-114">-Disable</span></span>
<span data-ttu-id="9dcf8-115">Indica que esse cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="9dcf8-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="9dcf8-116">-Enable</span></span>
<span data-ttu-id="9dcf8-117">Indica que esse cmdlet habilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="9dcf8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="9dcf8-118">-LabName</span></span>
<span data-ttu-id="9dcf8-119">Especifica o nome do laboratório para o qual esse cmdlet define as máquinas virtuais por política de laboratório.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="9dcf8-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="9dcf8-120">-MaxVMs</span></span>
<span data-ttu-id="9dcf8-121">Especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dcf8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dcf8-122">-ResourceGroupName</span></span>
<span data-ttu-id="9dcf8-123">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="9dcf8-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9dcf8-124">-Confirm</span></span>
<span data-ttu-id="9dcf8-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dcf8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dcf8-126">-WhatIf</span></span>
<span data-ttu-id="9dcf8-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dcf8-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dcf8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dcf8-129">CommonParameters</span></span>
<span data-ttu-id="9dcf8-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dcf8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dcf8-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dcf8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dcf8-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9dcf8-132">INPUTS</span></span>

### <span data-ttu-id="9dcf8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9dcf8-133">System.String</span></span>

## <span data-ttu-id="9dcf8-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9dcf8-134">OUTPUTS</span></span>

### <span data-ttu-id="9dcf8-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="9dcf8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="9dcf8-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9dcf8-136">NOTES</span></span>

## <span data-ttu-id="9dcf8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dcf8-137">RELATED LINKS</span></span>

[<span data-ttu-id="9dcf8-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="9dcf8-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


