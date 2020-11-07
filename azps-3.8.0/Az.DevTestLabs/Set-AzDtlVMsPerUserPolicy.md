---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942384"
---
# <span data-ttu-id="3656e-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="3656e-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="3656e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3656e-102">SYNOPSIS</span></span>
<span data-ttu-id="3656e-103">Define a política de máquinas virtuais por usuário de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="3656e-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="3656e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3656e-104">SYNTAX</span></span>

### <span data-ttu-id="3656e-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="3656e-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3656e-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="3656e-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3656e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3656e-107">DESCRIPTION</span></span>
<span data-ttu-id="3656e-108">O cmdlet **set-AzDtlVMsPerUserPolicy** define a política de máquinas virtuais por usuário de um laboratório, que define o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="3656e-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="3656e-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="3656e-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="3656e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3656e-110">EXAMPLES</span></span>

## <span data-ttu-id="3656e-111">OS</span><span class="sxs-lookup"><span data-stu-id="3656e-111">PARAMETERS</span></span>

### <span data-ttu-id="3656e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3656e-112">-DefaultProfile</span></span>
<span data-ttu-id="3656e-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3656e-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3656e-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="3656e-114">-Disable</span></span>
<span data-ttu-id="3656e-115">Indica que esse cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="3656e-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="3656e-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="3656e-116">-Enable</span></span>
<span data-ttu-id="3656e-117">Indica que esse cmdlet habilita a política para o laboratório.</span><span class="sxs-lookup"><span data-stu-id="3656e-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="3656e-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="3656e-118">-LabName</span></span>
<span data-ttu-id="3656e-119">Especifica o nome do laboratório para o qual esse cmdlet define a política de máquinas virtuais por usuário.</span><span class="sxs-lookup"><span data-stu-id="3656e-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="3656e-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="3656e-120">-MaxVMs</span></span>
<span data-ttu-id="3656e-121">Especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="3656e-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="3656e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3656e-122">-ResourceGroupName</span></span>
<span data-ttu-id="3656e-123">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="3656e-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="3656e-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3656e-124">-Confirm</span></span>
<span data-ttu-id="3656e-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3656e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3656e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3656e-126">-WhatIf</span></span>
<span data-ttu-id="3656e-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3656e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3656e-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3656e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3656e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3656e-129">CommonParameters</span></span>
<span data-ttu-id="3656e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3656e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3656e-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3656e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3656e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3656e-132">INPUTS</span></span>

### <span data-ttu-id="3656e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3656e-133">System.String</span></span>

## <span data-ttu-id="3656e-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3656e-134">OUTPUTS</span></span>

### <span data-ttu-id="3656e-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="3656e-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="3656e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3656e-136">NOTES</span></span>

## <span data-ttu-id="3656e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3656e-137">RELATED LINKS</span></span>

[<span data-ttu-id="3656e-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="3656e-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


