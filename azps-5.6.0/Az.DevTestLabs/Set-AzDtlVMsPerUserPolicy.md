---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 629ed4d9bc8eeb01f41bb857868f4206afcc9b0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892968"
---
# <span data-ttu-id="f5dbc-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f5dbc-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="f5dbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dbc-103">Define as máquinas virtuais por política de usuário de um laboratório em Laboratórios DevTest.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="f5dbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5dbc-104">SYNTAX</span></span>

### <span data-ttu-id="f5dbc-105">Habilitar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5dbc-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dbc-106">Desabilitar</span><span class="sxs-lookup"><span data-stu-id="f5dbc-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5dbc-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5dbc-107">DESCRIPTION</span></span>
<span data-ttu-id="f5dbc-108">O cmdlet **Set-AzDtlVMsPerUserPolicy** define as máquinas virtuais por política de usuário de um laboratório, que define o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="f5dbc-109">O cmdlet usa o grupo de recursos especificado e o nome do laboratório para definir a política.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="f5dbc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-110">EXAMPLES</span></span>

## <span data-ttu-id="f5dbc-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-111">PARAMETERS</span></span>

### <span data-ttu-id="f5dbc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5dbc-112">-DefaultProfile</span></span>
<span data-ttu-id="f5dbc-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f5dbc-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5dbc-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="f5dbc-114">-Disable</span></span>
<span data-ttu-id="f5dbc-115">Indica que esse cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="f5dbc-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="f5dbc-116">-Enable</span></span>
<span data-ttu-id="f5dbc-117">Indica que esse cmdlet habilita a política para o laboratório.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="f5dbc-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="f5dbc-118">-LabName</span></span>
<span data-ttu-id="f5dbc-119">Especifica o nome do laboratório para o qual este cmdlet define as máquinas virtuais por política de usuário.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="f5dbc-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="f5dbc-120">-MaxVMs</span></span>
<span data-ttu-id="f5dbc-121">Especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="f5dbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5dbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5dbc-123">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f5dbc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5dbc-124">-Confirm</span></span>
<span data-ttu-id="f5dbc-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5dbc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5dbc-126">-WhatIf</span></span>
<span data-ttu-id="f5dbc-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5dbc-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5dbc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dbc-129">CommonParameters</span></span>
<span data-ttu-id="f5dbc-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5dbc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dbc-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5dbc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dbc-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-132">INPUTS</span></span>

### <span data-ttu-id="f5dbc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f5dbc-133">System.String</span></span>

## <span data-ttu-id="f5dbc-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-134">OUTPUTS</span></span>

### <span data-ttu-id="f5dbc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f5dbc-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="f5dbc-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5dbc-136">NOTES</span></span>

## <span data-ttu-id="f5dbc-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5dbc-137">RELATED LINKS</span></span>

[<span data-ttu-id="f5dbc-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="f5dbc-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


