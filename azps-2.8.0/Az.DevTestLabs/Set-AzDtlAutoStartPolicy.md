---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: c751335f05f0e6ac9df5acb585dc5eb651d957a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596604"
---
# <span data-ttu-id="93bcc-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="93bcc-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="93bcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="93bcc-103">Define a política de início automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="93bcc-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="93bcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93bcc-104">SYNTAX</span></span>

### <span data-ttu-id="93bcc-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="93bcc-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93bcc-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="93bcc-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93bcc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93bcc-107">DESCRIPTION</span></span>
<span data-ttu-id="93bcc-108">O cmdlet **set-AzDtlAutoStartPolicy** define a política de início automático de um laboratório, que permite que as máquinas virtuais de laboratório sejam agendadas para início automático.</span><span class="sxs-lookup"><span data-stu-id="93bcc-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="93bcc-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="93bcc-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="93bcc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93bcc-110">EXAMPLES</span></span>

## <span data-ttu-id="93bcc-111">OS</span><span class="sxs-lookup"><span data-stu-id="93bcc-111">PARAMETERS</span></span>

### <span data-ttu-id="93bcc-112">-Dias</span><span class="sxs-lookup"><span data-stu-id="93bcc-112">-Days</span></span>
<span data-ttu-id="93bcc-113">Especifica, como uma matriz, os dias da semana para quando as máquinas virtuais do laboratório devem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="93bcc-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bcc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bcc-114">-DefaultProfile</span></span>
<span data-ttu-id="93bcc-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="93bcc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93bcc-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="93bcc-116">-Disable</span></span>
<span data-ttu-id="93bcc-117">Indica que esse cmdlet desabilita a política para as máquinas virtuais no laboratório.</span><span class="sxs-lookup"><span data-stu-id="93bcc-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="93bcc-118">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="93bcc-118">-Enable</span></span>
<span data-ttu-id="93bcc-119">Indica que esse cmdlet habilita a política para as máquinas virtuais no laboratório.</span><span class="sxs-lookup"><span data-stu-id="93bcc-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="93bcc-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="93bcc-120">-LabName</span></span>
<span data-ttu-id="93bcc-121">Especifica o nome do laboratório para o qual esse cmdlet define a política de início automático.</span><span class="sxs-lookup"><span data-stu-id="93bcc-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="93bcc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bcc-122">-ResourceGroupName</span></span>
<span data-ttu-id="93bcc-123">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="93bcc-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="93bcc-124">-Time</span><span class="sxs-lookup"><span data-stu-id="93bcc-124">-Time</span></span>
<span data-ttu-id="93bcc-125">Especifica a hora em que as máquinas virtuais do laboratório devem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="93bcc-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="93bcc-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="93bcc-126">-Confirm</span></span>
<span data-ttu-id="93bcc-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93bcc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93bcc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bcc-128">-WhatIf</span></span>
<span data-ttu-id="93bcc-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93bcc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93bcc-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93bcc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93bcc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bcc-131">CommonParameters</span></span>
<span data-ttu-id="93bcc-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93bcc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bcc-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93bcc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bcc-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93bcc-134">INPUTS</span></span>

### <span data-ttu-id="93bcc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="93bcc-135">System.String</span></span>

## <span data-ttu-id="93bcc-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93bcc-136">OUTPUTS</span></span>

### <span data-ttu-id="93bcc-137">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="93bcc-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="93bcc-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93bcc-138">NOTES</span></span>

## <span data-ttu-id="93bcc-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93bcc-139">RELATED LINKS</span></span>

[<span data-ttu-id="93bcc-140">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="93bcc-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


