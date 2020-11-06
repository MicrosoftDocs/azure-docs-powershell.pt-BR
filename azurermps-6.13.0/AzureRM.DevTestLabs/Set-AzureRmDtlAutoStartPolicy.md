---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 8cc571a9ba906ecc5556d920503712ef1bb3587a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430950"
---
# <span data-ttu-id="d5c90-101">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d5c90-101">Set-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="d5c90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5c90-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c90-103">Define a política de início automático de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="d5c90-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5c90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5c90-104">SYNTAX</span></span>

### <span data-ttu-id="d5c90-105">Habilitar (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5c90-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c90-106">Desabilita</span><span class="sxs-lookup"><span data-stu-id="d5c90-106">Disable</span></span>
```
Set-AzureRmDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5c90-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5c90-107">DESCRIPTION</span></span>
<span data-ttu-id="d5c90-108">O cmdlet **set-AzureRmDtlAutoStartPolicy** define a política de início automático de um laboratório, que permite que as máquinas virtuais de laboratório sejam agendadas para início automático.</span><span class="sxs-lookup"><span data-stu-id="d5c90-108">The **Set-AzureRmDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="d5c90-109">O cmdlet usa o grupo de recursos e o nome do laboratório especificado para definir a política.</span><span class="sxs-lookup"><span data-stu-id="d5c90-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d5c90-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5c90-110">EXAMPLES</span></span>

## <span data-ttu-id="d5c90-111">OS</span><span class="sxs-lookup"><span data-stu-id="d5c90-111">PARAMETERS</span></span>

### <span data-ttu-id="d5c90-112">-Dias</span><span class="sxs-lookup"><span data-stu-id="d5c90-112">-Days</span></span>
<span data-ttu-id="d5c90-113">Especifica, como uma matriz, os dias da semana para quando as máquinas virtuais do laboratório devem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="d5c90-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="d5c90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c90-114">-DefaultProfile</span></span>
<span data-ttu-id="d5c90-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d5c90-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5c90-116">-Disable</span><span class="sxs-lookup"><span data-stu-id="d5c90-116">-Disable</span></span>
<span data-ttu-id="d5c90-117">Indica que esse cmdlet desabilita a política para as máquinas virtuais no laboratório.</span><span class="sxs-lookup"><span data-stu-id="d5c90-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="d5c90-118">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="d5c90-118">-Enable</span></span>
<span data-ttu-id="d5c90-119">Indica que esse cmdlet habilita a política para as máquinas virtuais no laboratório.</span><span class="sxs-lookup"><span data-stu-id="d5c90-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="d5c90-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="d5c90-120">-LabName</span></span>
<span data-ttu-id="d5c90-121">Especifica o nome do laboratório para o qual esse cmdlet define a política de início automático.</span><span class="sxs-lookup"><span data-stu-id="d5c90-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="d5c90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c90-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5c90-123">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="d5c90-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d5c90-124">-Time</span><span class="sxs-lookup"><span data-stu-id="d5c90-124">-Time</span></span>
<span data-ttu-id="d5c90-125">Especifica a hora em que as máquinas virtuais do laboratório devem ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="d5c90-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="d5c90-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5c90-126">-Confirm</span></span>
<span data-ttu-id="d5c90-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5c90-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c90-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c90-128">-WhatIf</span></span>
<span data-ttu-id="d5c90-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5c90-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c90-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5c90-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c90-131">CommonParameters</span></span>
<span data-ttu-id="d5c90-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5c90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c90-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5c90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c90-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5c90-134">INPUTS</span></span>

### <span data-ttu-id="d5c90-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d5c90-135">System.String</span></span>

## <span data-ttu-id="d5c90-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5c90-136">OUTPUTS</span></span>

### <span data-ttu-id="d5c90-137">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="d5c90-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="d5c90-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5c90-138">NOTES</span></span>

## <span data-ttu-id="d5c90-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5c90-139">RELATED LINKS</span></span>

[<span data-ttu-id="d5c90-140">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="d5c90-140">Get-AzureRmDtlAutoStartPolicy</span></span>](./Get-AzureRmDtlAutoStartPolicy.md)


