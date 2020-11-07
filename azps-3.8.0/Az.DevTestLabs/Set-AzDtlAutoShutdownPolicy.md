---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b8c6965034b741ddd281bb81c9748a25d7038be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942386"
---
# <span data-ttu-id="9e902-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="9e902-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="9e902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e902-102">SYNOPSIS</span></span>
<span data-ttu-id="9e902-103">Define a política de desligamento automático de um laboratório DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="9e902-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="9e902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e902-104">SYNTAX</span></span>

### <span data-ttu-id="9e902-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e902-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e902-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="9e902-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e902-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e902-107">DESCRIPTION</span></span>
<span data-ttu-id="9e902-108">O cmdlet **set-AzDtlAutoShutdownPolicy** define a política de desligamento automático de um laboratório, que automaticamente desliga todas as máquinas virtuais do laboratório em um horário especificado do dia.</span><span class="sxs-lookup"><span data-stu-id="9e902-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="9e902-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="9e902-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="9e902-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e902-110">EXAMPLES</span></span>

## <span data-ttu-id="9e902-111">OS</span><span class="sxs-lookup"><span data-stu-id="9e902-111">PARAMETERS</span></span>

### <span data-ttu-id="9e902-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e902-112">-DefaultProfile</span></span>
<span data-ttu-id="9e902-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9e902-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e902-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="9e902-114">-Disable</span></span>
<span data-ttu-id="9e902-115">Indica que o cmdlet desabilita a política do laboratório.</span><span class="sxs-lookup"><span data-stu-id="9e902-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="9e902-116">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="9e902-116">-Enable</span></span>
<span data-ttu-id="9e902-117">Indica que o cmdlet habilita a política no laboratório.</span><span class="sxs-lookup"><span data-stu-id="9e902-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="9e902-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="9e902-118">-LabName</span></span>
<span data-ttu-id="9e902-119">Especifica o nome do laboratório para o qual esse cmdlet define a política de desligamento automático.</span><span class="sxs-lookup"><span data-stu-id="9e902-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="9e902-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e902-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e902-121">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="9e902-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="9e902-122">-Time</span><span class="sxs-lookup"><span data-stu-id="9e902-122">-Time</span></span>
<span data-ttu-id="9e902-123">Especifica o tempo, como um objeto **DateTime** , para quando as máquinas virtuais no laboratório devem desligar.</span><span class="sxs-lookup"><span data-stu-id="9e902-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e902-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e902-124">-Confirm</span></span>
<span data-ttu-id="9e902-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e902-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e902-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e902-126">-WhatIf</span></span>
<span data-ttu-id="9e902-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e902-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e902-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e902-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e902-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e902-129">CommonParameters</span></span>
<span data-ttu-id="9e902-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e902-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e902-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e902-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e902-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e902-132">INPUTS</span></span>

### <span data-ttu-id="9e902-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9e902-133">System.String</span></span>

## <span data-ttu-id="9e902-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e902-134">OUTPUTS</span></span>

### <span data-ttu-id="9e902-135">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="9e902-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="9e902-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e902-136">NOTES</span></span>

## <span data-ttu-id="9e902-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e902-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e902-138">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="9e902-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


