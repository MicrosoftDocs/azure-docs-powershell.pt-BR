---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 48f9e2a91923fa123b54b5ebf09abbb7cd64a1dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115824"
---
# <span data-ttu-id="daff8-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="daff8-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="daff8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daff8-102">SYNOPSIS</span></span>
<span data-ttu-id="daff8-103">Define as máquinas virtuais por política de usuário de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="daff8-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="daff8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daff8-104">SYNTAX</span></span>

### <span data-ttu-id="daff8-105">Habilitar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="daff8-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daff8-106">Desativar</span><span class="sxs-lookup"><span data-stu-id="daff8-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daff8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="daff8-107">DESCRIPTION</span></span>
<span data-ttu-id="daff8-108">O cmdlet **Set-AzDtlVMsPerUserPolicy** define as máquinas virtuais por política de usuário de um laboratório, que define o número máximo de máquinas virtuais permitidas por usuário.</span><span class="sxs-lookup"><span data-stu-id="daff8-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="daff8-109">O cmdlet usa o grupo de recursos especificado e o nome do laboratório para definir a política.</span><span class="sxs-lookup"><span data-stu-id="daff8-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="daff8-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="daff8-110">EXAMPLES</span></span>

## <span data-ttu-id="daff8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daff8-111">PARAMETERS</span></span>

### <span data-ttu-id="daff8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daff8-112">-DefaultProfile</span></span>
<span data-ttu-id="daff8-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="daff8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daff8-114">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="daff8-114">-Disable</span></span>
<span data-ttu-id="daff8-115">Indica que esse cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="daff8-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="daff8-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="daff8-116">-Enable</span></span>
<span data-ttu-id="daff8-117">Indica que esse cmdlet habilita a política para o laboratório.</span><span class="sxs-lookup"><span data-stu-id="daff8-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="daff8-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="daff8-118">-LabName</span></span>
<span data-ttu-id="daff8-119">Especifica o nome do laboratório para o qual este cmdlet define as máquinas virtuais por política de usuário.</span><span class="sxs-lookup"><span data-stu-id="daff8-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="daff8-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="daff8-120">-MaxVMs</span></span>
<span data-ttu-id="daff8-121">Especifica o número máximo de máquinas virtuais que podem ser criadas no laboratório.</span><span class="sxs-lookup"><span data-stu-id="daff8-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="daff8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daff8-122">-ResourceGroupName</span></span>
<span data-ttu-id="daff8-123">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="daff8-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="daff8-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="daff8-124">-Confirm</span></span>
<span data-ttu-id="daff8-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daff8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daff8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daff8-126">-WhatIf</span></span>
<span data-ttu-id="daff8-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="daff8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daff8-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daff8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daff8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daff8-129">CommonParameters</span></span>
<span data-ttu-id="daff8-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daff8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daff8-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daff8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daff8-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="daff8-132">INPUTS</span></span>

### <span data-ttu-id="daff8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="daff8-133">System.String</span></span>

## <span data-ttu-id="daff8-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="daff8-134">OUTPUTS</span></span>

### <span data-ttu-id="daff8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="daff8-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="daff8-136">Notas</span><span class="sxs-lookup"><span data-stu-id="daff8-136">NOTES</span></span>

## <span data-ttu-id="daff8-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daff8-137">RELATED LINKS</span></span>

[<span data-ttu-id="daff8-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="daff8-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


