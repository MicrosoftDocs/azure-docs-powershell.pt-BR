---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3433d6bf5d3886978b75024e34c873e38230212b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891869"
---
# <span data-ttu-id="e4e9a-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e4e9a-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e4e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e9a-103">Cria um objeto de configuração para o patch automático em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e4e9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4e9a-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="e4e9a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4e9a-105">DESCRIPTION</span></span>
<span data-ttu-id="e4e9a-106">O cmdlet **New-AzVMSqlServerAutoPatchingConfig** cria um objeto de configuração para o patch automático em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e4e9a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-107">EXAMPLES</span></span>

### <span data-ttu-id="e4e9a-108">Exemplo 1: Criar um objeto de configuração para configurar o patch automático</span><span class="sxs-lookup"><span data-stu-id="e4e9a-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e4e9a-109">Este comando cria um objeto de configuração para correção.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e4e9a-110">O comando especifica o dia da semana e define a janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e4e9a-111">Essa configuração habilita o patch que usa esses valores.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e4e9a-112">O comando armazena o resultado na variável $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e4e9a-113">Você pode especificar esse item de configuração para outros cmdlets, como o Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e4e9a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-114">PARAMETERS</span></span>

### <span data-ttu-id="e4e9a-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e4e9a-115">-DayOfWeek</span></span>
<span data-ttu-id="e4e9a-116">Especifica o dia da semana em que as atualizações devem ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="e4e9a-117">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e4e9a-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e4e9a-118">Domingo</span><span class="sxs-lookup"><span data-stu-id="e4e9a-118">Sunday</span></span>
- <span data-ttu-id="e4e9a-119">Segunda-feira</span><span class="sxs-lookup"><span data-stu-id="e4e9a-119">Monday</span></span>
- <span data-ttu-id="e4e9a-120">Terça-feira</span><span class="sxs-lookup"><span data-stu-id="e4e9a-120">Tuesday</span></span>
- <span data-ttu-id="e4e9a-121">Quarta-feira</span><span class="sxs-lookup"><span data-stu-id="e4e9a-121">Wednesday</span></span>
- <span data-ttu-id="e4e9a-122">Quinta-feira</span><span class="sxs-lookup"><span data-stu-id="e4e9a-122">Thursday</span></span>
- <span data-ttu-id="e4e9a-123">Sexta-feira</span><span class="sxs-lookup"><span data-stu-id="e4e9a-123">Friday</span></span>
- <span data-ttu-id="e4e9a-124">Sábado</span><span class="sxs-lookup"><span data-stu-id="e4e9a-124">Saturday</span></span>
- <span data-ttu-id="e4e9a-125">Todos os dias</span><span class="sxs-lookup"><span data-stu-id="e4e9a-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9a-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="e4e9a-126">-Enable</span></span>
<span data-ttu-id="e4e9a-127">Indica que a correção automatizada para a máquina virtual está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e4e9a-128">Se você habilitar o patch automatizado, o cmdlet colocará o Windows Update no modo interativo.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e4e9a-129">Se você desabilitar o patch automático, as configurações do Windows Update não mudarão.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9a-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e4e9a-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e4e9a-131">Especifica a duração, em minutos, da janela de manutenção.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e4e9a-132">A correção automatizada evita a execução de uma ação que pode afetar a disponibilidade de uma máquina virtual fora dessa janela.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e4e9a-133">Especifique um múltiplo de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9a-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e4e9a-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e4e9a-135">Especifica a hora do dia em que a janela de manutenção é iniciada.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e4e9a-136">Este tempo define quando as atualizações começam a ser instaladas.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9a-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e4e9a-137">-PatchCategory</span></span>
<span data-ttu-id="e4e9a-138">Especifica se as atualizações importantes devem ser incluídas.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e9a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e9a-139">CommonParameters</span></span>
<span data-ttu-id="e4e9a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e9a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e9a-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4e9a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e9a-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-142">INPUTS</span></span>

### <span data-ttu-id="e4e9a-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e4e9a-143">None</span></span>

## <span data-ttu-id="e4e9a-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-144">OUTPUTS</span></span>

### <span data-ttu-id="e4e9a-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e4e9a-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="e4e9a-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4e9a-146">NOTES</span></span>

## <span data-ttu-id="e4e9a-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4e9a-147">RELATED LINKS</span></span>

[<span data-ttu-id="e4e9a-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e4e9a-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e4e9a-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e4e9a-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


